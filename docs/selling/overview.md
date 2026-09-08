# Selling products (for online stores)

This section is a complete guide for **online stores**. If you sell products and you
want the assistant to help shoppers find and buy them, everything you need is here —
from connecting your store to going live and keeping it up to date.

You do not need to read the rest of the site to follow this section. It stands on its
own. (You can still use the general features too, like [answering questions](../knowledge-base/overview.md).)

## What the shopping assistant does

A shopper types the way they talk:

> "waterproof running shoes under 3000 taka, size 42"

The assistant reads your product list and replies with a short line, then shows the
matching products as cards — photo, price, whether it is in stock, and a link
straight to the product page.

It also answers questions about how good a product is, using your real customer
reviews. If your reviews say the sizing runs small, that is what it tells the
shopper. It does not make up an opinion.

## What it will not do

Worth knowing before you start. Full detail is in [What it will not do](limitations.md).

- **It never makes up a product.** If you do not sell it, it says so.
- **It cannot track orders.** "Where is my order?" is not answered yet.
- **It does not show a discount as a discount.** A sale price becomes part of a price
  range, not a "was / now" label.
- **It does not refresh on its own yet.** You press **Sync** after a price or stock
  change. See [Keeping your catalogue current](keeping-current.md).

## The path to going live

1. **[Connect your store](connect-your-store.md).** Give us your web address, a file,
   a feed, or use the API.
2. **We bring your products in.** This runs in the background.
3. **[Run the go-live checklist](go-live-checklist.md)** to make sure prices, links,
   and answers are right.
4. **[Add the chat box to your site](../widget/install.md).**
5. **[Keep your catalogue current](keeping-current.md)** with Sync.

## For your developer

If you have a developer, the technical details — the four import methods, the product
API, the file and feed columns, and testing — are in this same section:

- [How products get in (import methods)](import-methods.md)
- [Product API (Push)](push-api.md)
- [Product fields](product-fields.md)
- [File & feed columns](feed-csv-columns.md)
- [Test the setup](testing.md)
