# Developer guide overview

There are two integration tasks.

1. **Add the chat widget** to the site, so visitors can chat.
2. **Send a product catalogue**, so the assistant can search and show products.

Either order works, but the widget has nothing to search until products are in.

## Add the chat widget

The widget is one `<script>` tag placed before the closing `</body>` tag. You can
change its look with `data-*` attributes.

- [Install the widget](../widget/install.md) — the snippet and where it goes.
- [Widget options](../widget/options.md) — the full list of `data-*` attributes.

## Send a product catalogue

There are four ways to send products in, including an HTTP API.

- [Import methods](import-methods.md) — pick how products get in.
- [Product API (Push)](push-api.md) — send products over HTTP.
- [Product fields](product-fields.md) — the fields on a product.
- [File & feed columns](feed-csv-columns.md) — the column names we read.
- [Test the setup](testing.md) — checks before you go live.
