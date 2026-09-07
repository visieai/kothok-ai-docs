# Connect your store

There are four ways to bring your products in. Pick one. A store can use only one at
a time, and picking a new one replaces the old one.

Start with **Website**. It is the only way that asks no technical question. If it
does not work, we tell you which of the others to use.

## The four ways

| Way | Use it when | What you give us | Review answers? |
|---|---|---|---|
| **Website** | You have a normal online shop | Your web address | Yes |
| **File** | You can export your products as a CSV | A CSV file | No |
| **Feed** | Your shop already publishes a product feed | The feed address | Yes |
| **Push** | Your shop is custom built, or the others do not fit | Nothing — we give your developer a token | No |

!!! note "Review answers"
    Only **Website** and **Feed** can answer review questions, because reviews are
    read off your product pages. **File** and **Push** stores get product search
    but no review answers. If review answers matter to you, use Website or Feed.

## Website

You give us your store's web address. We read your product pages the way a
shopper's browser does. Nothing is written to your site, and nothing changes on it.

We show you one of your products first. Check the name and price. If they are
right, we bring in the rest.

!!! info "If you are on Shopify"
    We read Shopify stores by looking at the pages, not through a Shopify app.
    That means sizes and stock are read as best we can from the page, not taken
    directly from Shopify. If you need exact stock, ask your developer about
    **Push**. A direct Shopify connection is on the [roadmap](../roadmap.md).

## File

Export your products as a CSV from your shop admin and send it. Limits:

- The file must be `.csv`, `.tsv`, or `.txt`.
- Up to 5 MB. Save a spreadsheet as CSV first. For a bigger list, use Feed or Push.

We read the file and show you how many rows we found, how many we skipped and why,
and the first few products as they will look. Check the skipped rows — that is when
to catch a wrong column, before a shopper sees it.

The column names we look for are in [Feed & CSV columns](../developer/feed-csv-columns.md).

## Feed

If your shop already publishes a product feed at a web address that does not change
(a Google Merchant feed works as it is), give us that address once. We read it each
time a sync runs.

## Push

For custom-built shops, or shops where prices change often. Your developer sends
products to us over an API. See the [Push API](../developer/push-api.md).

## After you connect

We bring your products in. This runs in the background. Then you run the
[go-live checklist](go-live-checklist.md) with us.
