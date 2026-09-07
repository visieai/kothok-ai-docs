# FAQ

## About the assistant

**Will it recommend a competitor's product?**
No. It only ever sees your catalogue.

**What happens if it does not understand?**
It says it did not find a match. It does not guess.

**Can I turn it off?**
Yes, at any time. Your store can be disconnected and the assistant goes back to
answering only your general questions.

**Does it change my website?**
No. We read your product pages the way a shopper's browser does. Nothing is written
to your site.

**Do you store my product photos?**
No. The cards load photos straight from your own site, so if you change a photo it
follows along.

## Setting up

**What do you need to start?**
Just your store's web address. See [How onboarding works](getting-started/overview.md).

**Can I use more than one product source at once?**
No. A store uses one source at a time. Switching to a new one replaces the old one.
We cannot join two lists together.

**My site cannot be read automatically. What now?**
Export your products as a CSV and upload it, or use a feed or the Push API. See
[Connect your store](getting-started/connect-your-store.md).

**Does it answer review questions?**
Only for Website and Feed stores, because reviews are read off your product pages.
File and Push stores get product search but no review answers.

## Prices and stock

**Why is the assistant quoting an old price?**
It does not refresh on its own. Press **Sync** after a price change, or ask us to
run a daily sync for you. See
[Keeping your catalogue current](getting-started/keeping-current.md).

**Can it show a sale as "was / now"?**
Not yet. A sale price becomes part of a price range instead. Tell us before a
campaign. See [What it will not do](assistant/limitations.md).

**Can it tell a shopper where their order is?**
No. Order tracking is not built.

## For developers

**Which import method should I use?**
Website or File if you can — they need no code. Feed if the shop already publishes
one. Push for custom shops or fast-changing prices. See
[Import methods](developer/import-methods.md).

**Is there a Shopify or WooCommerce app?**
Not yet. A Shopify store is read by crawling its pages today. For exact stock, use
[Push](developer/push-api.md).

**Why did my push return `200` but some products are missing?**
Check the `failed` count in the response, not just the HTTP status. See the
[Push API](developer/push-api.md).
