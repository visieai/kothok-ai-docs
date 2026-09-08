# Website widget

The website widget is the chat box that appears in the corner of your site. It is the
main way visitors talk to your assistant, and the only channel that shows product
cards and tappable meeting times.

## Add it to your site

Paste this one line into your website, just before the closing `</body>` tag:

```html
<script
  src="https://static.kothok.ai/js/widgets.js"
  data-public-key="YOUR_PUBLIC_KEY"
  async>
</script>
```

Get your **public key** from the dashboard. It is safe to put in your page — it is
not a password.

Once the code is live, the chat button appears on your site. That is all it takes.

Step-by-step, with every option explained, is in [Install the widget](../widget/install.md).

## What it can show

- **Answers** to questions, from your [knowledge base](../knowledge-base/overview.md).
- **Product cards** — photo, price, stock, and a link — if you
  [sell products](../selling/overview.md).
- **Meeting times** as tappable buttons, if you have
  [connected a calendar](../appointments/connect-calendar.md).
- **A human's replies**, when someone on your team
  [takes over the chat](../conversations/live-agent.md).

## Make it match your brand

You can change the title, colour, logo, position, greeting, and more. Some branding
options are part of paid plans. See [Customize the widget](../widget/install.md) and
[Plans & billing](../billing/plans.md).

## Good to know

- The widget will not clash with your website's design. It is sealed off, so your
  styles cannot leak in and its styles cannot leak out.
- It works on modern browsers, including Safari 12 and newer.
