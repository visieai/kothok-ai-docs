# Developer guide

This page points developers to the technical parts of the documentation. Kothok AI
needs very little code — most setup happens in the dashboard — but two tasks may
reach a developer.

## Add the chat widget to a site

The widget is one `<script>` tag pasted before the closing `</body>` tag. You can
change its look with `data-*` attributes.

* [Install the widget](../getting-started/install-widget.md) — the snippet and where
  it goes.
* [Widget options](../widget/options.md) — the full list of `data-*` attributes.

## Connect a product catalogue (online stores)

If the business is an online store, the assistant can show products in chat. There
are four ways to send products in, including a product API. All of it is in the
store section:

* [How products get in (import methods)](../selling/import-methods.md)
* [Product API (Push)](../selling/push-api.md)
* [Product fields](../selling/product-fields.md)
* [File & feed columns](../selling/feed-csv-columns.md)
* [Test the setup](../selling/testing.md)

## What is not available

* **No order-tracking API.** The assistant cannot look up order status. Do not build
  anything that depends on it.
* **No Shopify or WooCommerce app.** Online stores are read from the website, a file,
  a feed, or the product API. See [How products get in](../selling/import-methods.md).
