# What it will not do

Worth knowing before you start, so nothing surprises you later. These are known
limits, not bugs. Some are on the [roadmap](../roadmap.md).

## It will never make up a product

If you do not sell it, the assistant says so instead of offering something close.
We would rather it says "we do not have that" than send a shopper to a page that
does not exist.

## It cannot track orders

Order tracking is not built. "Where is my order?" is not a question the assistant
can answer. There is no order status, no tracking number, nothing that reads your
order system.

## It does not show a discount as a discount

If your product list carries both a normal price and a sale price, the assistant
treats them as a price range. A product at 3000 on sale for 1500 shows as something
like "1500 to 3000."

It never says "was 3000, now 1500," and it never marks anything as on sale.

**Tell us before you start a campaign** so we can check how your prices will read.

## It does not update itself yet

The assistant knows your products as they were at the last sync. You press **Sync**
after you change prices or stock. See
[Keeping your catalogue current](keeping-current.md).

## No exact stock on some Shopify stores

A Shopify store read through the website has its sizes and stock read from the page,
which is a best guess, not an exact figure. For exact stock, use
[Push](push-api.md).

## Common questions

**Will it recommend a competitor's product?** No. It only ever sees your catalogue.

**What if it does not understand?** It says it did not find a match. It does not
guess.

**Can I stop it?** Yes, at any time. Your store can be disconnected and the
assistant goes back to answering only your general questions.

**Does it change my website?** No. We read your product pages the way a shopper's
browser does. Nothing is written to your site.

**Do you store my product photos?** No. The cards load photos straight from your own
site, so if you change a photo it follows along.
