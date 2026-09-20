# Install the widget

The widget is the chat box on your website. Installing it is one script tag.

## Prerequisites

- Access to edit your website's HTML.
- Your **public key**, from the **Installation** page in the dashboard.

## Add the snippet

Paste this just before the closing `</body>` tag:

```html
<script
  src="https://static.kothok.ai/js/widgets.js"
  data-public-key="YOUR_PUBLIC_KEY"
  async>
</script>
```

Copy the snippet from the **Installation** page in the dashboard so the key is
correct. The public key is safe to place in your page; it is not a password.

**Result:** the chat button appears on your site within a few seconds.

## Set options

Add `data-*` attributes to the same script tag to set the greeting, home screen, and
behaviour:

```html
<script
  src="https://static.kothok.ai/js/widgets.js"
  data-public-key="YOUR_PUBLIC_KEY"
  data-greeting="Hi! How can we help?"
  async>
</script>
```

Each attribute is optional and has a default. See [Widget options](options.md) for
the full list. You can also set the greeting and other basics from the dashboard,
which apply without editing the page again.

## Good to know

* The widget is sealed off from your site's design, so your styles and its styles do
  not clash.
* It works on modern browsers, including Safari 12 and newer.
