# Developer guide overview

This guide is for the developer connecting a shop to the Kothok assistant.

There are two jobs:

1. **Get the products in**, so the assistant knows what the shop sells.
2. **Put the widget on the site**, so shoppers can ask.

Either order works, but the widget is not much use until the products are in.

## Do you even need a developer?

Two of the four import methods need no code:

- **Website** — the owner does it from the dashboard.
- **File** — the owner uploads a CSV from the dashboard.

If one of those fits, point the owner at the dashboard and you are done. You are
needed for the other two:

- **Feed** — give us the feed address once. See [Import methods](import-methods.md).
- **Push** — an API integration. See the [Push API](push-api.md).

## The rest of this guide

- [Import methods](import-methods.md) — pick how products get in.
- [Push API](push-api.md) — send products over an API.
- [Product fields](product-fields.md) — the fields on a product, and the four to
  get right.
- [Feed & CSV columns](feed-csv-columns.md) — the column names we read.
- [Install the widget](widget.md) — the script tag and its options.
- [Test the setup](testing.md) — six checks before shoppers arrive.

## Things to know up front

These affect what you build, so read them before you start.

- **A store uses one import method at a time.** Picking a new one replaces the old.
  You cannot join two catalogues.
- **Nothing re-reads a feed on its own yet.** A feed is read when a sync runs, and a
  sync is started from the dashboard, not on a timer. If prices change often, use
  Push, which is live as soon as you call it.
- **Reviews are read only off the product page.** Website and Feed stores get review
  answers. Push and File stores do not. There is no way to send us reviews yet.
- **There is no Shopify or WooCommerce API adapter.** A Shopify shop is read by
  crawling the pages, which guesses at sizes and stock. For exact stock, use Push.
- **There is no order tracking.** No endpoint, no field. Do not build anything that
  assumes it.
