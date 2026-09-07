# Test the setup

Run these six checks before letting shoppers in. They catch the mistakes that are
easy to miss.

1. **Bring products in.** Push two or three products, or connect the feed and run one
   sync.
2. **Check the numbers.** `imported` should match what you sent, and `failed` should
   be `0`. For a feed, the product count in the dashboard should look right.
3. **Find a product by name.** Open the site and ask for one product by name. It
   should come back as a card.
4. **Check a budget.** Ask again with a budget under its price. It should not come
   back.
5. **Click the card.** It should open the correct product page.
6. **Push the same batch again.** The product count must stay the same.

## Why step 6 matters

Step 6 is the one people skip. A broken `external_id` shows up there and nowhere
else — until one day the catalogue has doubled and nobody noticed. If the count
grows when you send the same products again, your `external_id` is changing between
sends. See [Product fields](product-fields.md).

## Also worth checking

- **Say no.** Ask for something the shop does not sell. The assistant should say it
  has nothing like that, not offer something else.
- **Currency.** Make sure prices show in the money you expect.

These match the owner's [go-live checklist](../getting-started/go-live-checklist.md).
Run both.
