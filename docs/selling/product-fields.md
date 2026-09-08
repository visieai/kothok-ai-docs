# Product fields

These are the fields on a product sent through the [Push API](push-api.md).

## Required fields

An empty value is refused.

| Field | Type | Notes |
|---|---|---|
| `external_id` | text, 1–255 | Your own id. See below. |
| `title` | text | What the shopper sees on the card. |
| `url` | text | The page the card links to. |

## Optional fields

| Field | Type | Notes |
|---|---|---|
| `description` | text | Used for matching, so it is worth sending. |
| `brand` | text | |
| `product_type` | text | e.g. "Running shoes" |
| `tags` | list of text | |
| `price_min` | decimal | Send as text so it does not get rounded. |
| `price_max` | decimal | Same as `price_min` if there is only one price. |
| `currency` | 3 letters | e.g. `BDT`, `USD` |
| `in_stock` | true/false | `true` if you leave it out. |
| `inventory` | whole number | |
| `variants` | list of objects | `{sku, size, color, price, inventory}` |
| `images` | list of web addresses | Addresses only, never the image itself. |

## Four things to get right

**`external_id` must never change.** It is how we know a product is the same one as
last time. Use your own product id or SKU. Do not use anything that changes when the
product is edited, such as a name turned into a slug. If it changes, you get copies
instead of updates.

**Send prices as text.** Use `"2850.00"`, not `2850.00`. Prices are kept to two
decimal places, and sending them as numbers can round them wrong. This is money, so
it is worth the extra quotes.

**Prices are a range.** If a product has one price, put the same value in `price_min`
and `price_max`. If sizes or colours cost different amounts, put the real lowest and
highest. Shoppers filter on this, so a wrong range means the product does not show up
in searches it should.

**Images are addresses on your own server.** We never keep the image itself. So if
you change a photo on your side, the card changes too, with no push needed.
