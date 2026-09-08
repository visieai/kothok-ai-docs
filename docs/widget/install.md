# Customize the widget

The widget is the chat box on your website. You can change how it looks and behaves
so it fits your brand. This page explains the two ways to customize it. The full
option list is in [Widget options](options.md), and brand controls are in
[Branding & "Powered by"](branding.md).

## Two ways to customize

You can change the widget in two places. They work together.

1. **Dashboard settings.** Change the greeting, position, title, logo, placeholder
   text, and quick links on the **Installation** or **Settings** page. These are
   saved for you and apply everywhere, even to sites already running the widget.
2. **Script attributes.** Add `data-*` attributes to the widget's `<script>` tag for
   options you set once in the page code. See [Widget options](options.md).

If a setting exists in both places, the dashboard value wins.

## Set it up from the dashboard

1. Open the **Installation** (or **Settings**) page in the dashboard.
2. Change any of these:
    * **Greeting** — the first message visitors see.
    * **Position** — which side the chat button sits on.
    * **Title** and **logo** — the header of the chat box (paid plans).
    * **Placeholder** — the grey text in the message box.
    * **Quick links** — up to five shortcut links on the home screen.
3. Save.

**Result:** the change appears on your site, including sites already running the
widget.

## Set it up in the page code

Add attributes to the script tag, like this:

```html
<script
  src="https://static.kothok.ai/js/widgets.js"
  data-public-key="YOUR_PUBLIC_KEY"
  data-title="Ask us anything"
  data-color="#0f766e"
  data-greeting="Hi! How can we help?"
  async>
</script>
```

Each attribute is optional and has a sensible default. See the full list in
[Widget options](options.md).

## Good to know

* The widget is sealed off from your site's design, so your styles and its styles do
  not clash.
* It works on modern browsers, including Safari 12 and newer.
* Some brand options depend on your plan. See [Branding & "Powered by"](branding.md).
