# Install the widget

The widget is the chat box shoppers use on the website. It is one script tag.

## The script tag

Add this just before the closing `</body>` tag on your site:

```html
<script
  src="https://YOUR-WIDGET-HOST/widgets.min.js"
  data-public-key="THE_SHOPS_PUBLIC_KEY">
</script>
```

Get the script address and the public key from the dashboard.

!!! info "The public key is not a secret"
    It is meant to sit in the page source. It is not the same as the ingest token
    used by the [Push API](push-api.md), which must be kept private.

Product cards need no setup. Once the store has products, the assistant shows them.

## Options

You can add any of these attributes to the script tag. Each one has a default, so
you can skip them all.

| Attribute | What it does |
|---|---|
| `data-title` | Title in the header |
| `data-subtitle` | Small line under the title |
| `data-color` | Main colour |
| `data-logo` | Logo image address |
| `data-position` | `bottom-right` (default) or `bottom-left` |
| `data-greeting` | First message |
| `data-placeholder` | Grey text in the input box |
| `data-open` | `true` opens it when the page loads |
| `data-promo` | `false` turns off the pop-up bubble |

Example with a few set:

```html
<script
  src="https://YOUR-WIDGET-HOST/widgets.min.js"
  data-public-key="THE_SHOPS_PUBLIC_KEY"
  data-title="Ask us anything"
  data-color="#0f766e"
  data-position="bottom-left"
  data-greeting="Hi! Looking for something?">
</script>
```

## Good to know

- **It will not clash with your site's styles.** The widget draws itself inside a
  shadow DOM. Your CSS cannot get in, and its CSS cannot get out.
- **It works on Safari 12 and newer.**
- **Product cards appear only on the website.** On WhatsApp and Messenger the same
  products are written out as text. See [Where it works](../assistant/channels.md).

## Next

Run the [six checks](testing.md) before letting shoppers in.
