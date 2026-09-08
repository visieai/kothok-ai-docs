# Install the widget

The widget is the chat box that appears in the corner of your website. Installing it
means pasting one line of code into your site.

## Prerequisites

- Access to edit your website's HTML, or a developer who can paste one line for you.
- Your **public key**, found on the **Installation** page in the dashboard.

## Get your snippet

1. In the dashboard, open the **Installation** page.
2. Copy the script snippet shown there. It already includes your public key.

The snippet looks like this:

```html
<script
  src="https://static.kothok.ai/js/widgets.js"
  data-public-key="YOUR_PUBLIC_KEY"
  async>
</script>
```

Always copy the snippet from the dashboard rather than typing it, so the key is
correct.

!!! note
    Your public key is safe to place in your page. It is not a password.

## Add it to your site

1. Open your website's HTML.
2. Paste the snippet just before the closing `</body>` tag.
3. Save and publish your site.

**Result:** the chat button appears in the corner of your site within a few seconds.

## Confirm it is working

The Installation page shows a **Setup status** card. It confirms three things:

1. **Knowledge added** — you have trained the assistant.
2. **Widget customized** — you have set a greeting.
3. **Script installed** — the widget has run on your site at least once.

Open your site, send the assistant a message, then check that **Script installed**
turns green.

## Next steps

- [Customize the widget](../widget/install.md) — change its colour, title, and more.
- [Train your assistant](../knowledge-base/overview.md) — if you have not yet.
