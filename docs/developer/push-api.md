# Push API

Use Push when the shop is custom built, or when prices change often and you want to
send updates as they happen. Products sent by Push can be found straight away —
there is no sync step.

## Step 1: get a token

The shop owner does this from the dashboard while logged in. It calls:

```
POST /stores/push/token
```

You get back:

```json
{ "connection_id": 42, "token": "42.xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" }
```

!!! warning "The token is shown once"
    It cannot be read again. Save it somewhere safe. Calling the endpoint again
    gives you a new token and the old one stops working straight away — that is how
    you replace a token that has leaked.

The token looks like `<connection_id>.<secret>`. The number in front is not secret,
but do not split the token or use that number yourself. Send the whole string.

## Step 2: send products

```
POST /stores/push
X-Ingest-Token: 42.xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Content-Type: application/json
```

```json
{
  "products": [
    {
      "external_id": "SKU-1001",
      "title": "Trail Runner 3 Waterproof",
      "url": "https://shop.example.com/products/trail-runner-3",
      "description": "Waterproof trail shoe with a grip outsole.",
      "brand": "Northpeak",
      "product_type": "Running shoes",
      "tags": ["waterproof", "trail"],
      "price_min": "2850.00",
      "price_max": "3200.00",
      "currency": "BDT",
      "in_stock": true,
      "inventory": 24,
      "variants": [
        { "sku": "SKU-1001-42", "size": "42", "color": "black",
          "price": "2850.00", "inventory": 11 }
      ],
      "images": ["https://cdn.example.com/trail-runner-3.jpg"]
    }
  ]
}
```

Use the `X-Ingest-Token` header, not `Authorization`. This is a password for a
program, not for a person, and it is kept separate on purpose.

The full list of fields is in [Product fields](product-fields.md).

## What comes back

```json
{ "connection_id": 42, "imported": 499, "failed": 1,
  "errors": ["SKU-1077: DataError"] }
```

!!! danger "Check `failed`, not just the HTTP status"
    A request can come back `200` with some products refused. One bad product does
    not throw away the rest — we try the batch again one product at a time and keep
    the good ones. Only the first 10 errors are listed, so `failed` is the real
    count.

`401` means the token was missing, wrong, badly formed, or the shop was
disconnected. All four give the same answer on purpose, so nobody can learn anything
by guessing.

## Rules that matter

**500 products per request, at most.** Split a bigger catalogue into batches. The
body is also capped at 5 MB.

**Sending the same product twice is safe.** Products are matched on `external_id`.
Sending one again updates it instead of making a copy. So it is safe to retry a
request that timed out.

**A push only covers what is in it.** Products you leave out are left alone, not
deleted. Sending one product does not remove the other 999. To take a product out of
search, send it with `"in_stock": false`.

**Products can be found straight away.** A push writes the database and the search
index in the same call. There is no sync step for Push — the Sync button does
nothing on a Push store.

## Next

Test the setup with the [six checks](testing.md).
