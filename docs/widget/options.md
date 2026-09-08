# Widget options

These are the `data-*` attributes you can add to the widget's `<script>` tag. Every
one is optional and has a default, so you can add only the ones you need. For
settings you would rather change without editing code, use the dashboard — see
[Customize the widget](install.md).

## Required

| Attribute | What it does |
|---|---|
| `data-public-key` | Your public key, from the dashboard. The widget needs this to work. |

## Appearance

| Attribute | What it does |
|---|---|
| `data-title` | Title in the header (paid plans) |
| `data-subtitle` | Small line under the title |
| `data-logo` | Logo image address (paid plans) |
| `data-color` | Main colour |
| `data-position` | `bottom-right` (default) or `bottom-left` |
| `data-placeholder` | Grey text in the message box |

## Behaviour

| Attribute | What it does |
|---|---|
| `data-greeting` | The first message shown |
| `data-open` | `true` opens the chat when the page loads |
| `data-landing` | Which screen opens first: `chat`, `home`, or `messages` |
| `data-promo` | `false` turns off the pop-up bubble |
| `data-promo-title` | Title of the pop-up bubble |
| `data-promo-text` | Text of the pop-up bubble |

## Home screen

| Attribute | What it does |
|---|---|
| `data-home` | Show or hide the home screen |
| `data-home-heading` | Heading on the home screen |
| `data-cta` | The main button text on the home screen |
| `data-home-links` | Up to five quick links, as `Label\|https://url` separated by `;` |
| `data-tabs` | Show or hide the bottom navigation |
| `data-history` | Show or hide the visitor's past conversations |

## Feedback and advanced

| Attribute | What it does |
|---|---|
| `data-feedback` | Show a rating card at the end of a chat |
| `data-fonts` | Turn off web fonts (for strict security policies) |
| `data-sync-tabs` | Keep the chat in sync across browser tabs |
| `data-debug` | Print debug messages to the browser console |

## Example

```html
<script
  src="https://static.kothok.ai/js/widgets.js"
  data-public-key="YOUR_PUBLIC_KEY"
  data-title="Ask us anything"
  data-color="#0f766e"
  data-position="bottom-left"
  data-greeting="Hi! Looking for something?"
  data-home-links="Shipping|https://example.com/shipping;Returns|https://example.com/returns"
  async>
</script>
```

## Notes

* Title and logo are only shown on paid plans. See [Branding & "Powered by"](branding.md).
* The `data-logo` address must start with `https://` or be an embedded image. Other
  addresses are ignored for safety.
