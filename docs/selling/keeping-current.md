# Keeping your catalogue current

This is the most important thing to understand after you go live.

## The assistant does not refresh on its own

The assistant knows your products exactly as they were the last time your list was
brought in. Change a price, and it keeps quoting the old one until someone presses
**Sync**.

So after you change prices, add products, or something sells out, the list must be
brought in again.

## Two ways to handle it

Pick one before you go live.

- **Press Sync yourself** whenever you change prices, add products, or sell out.
- **Ask us to run it for you** at an agreed time each day.

## What Sync does

Sync brings your product list in again from your website, feed, or file, and
updates prices, stock, and any new or removed products.

- A sync runs in the background. You can keep working while it runs.
- Pressing Sync twice does nothing bad.
- Review answers are refreshed in a separate step after the products, so they may
  arrive a little later.

!!! note "Push stores are different"
    If your developer uses [Push](push-api.md), there is no Sync step.
    Products are updated the moment they are sent. The Sync button does nothing for
    a Push store.

## Coming soon

Automatic refreshing is the next thing we are building. When it is ready, the
assistant will refresh on a schedule and this manual step goes away. See the
[roadmap](../roadmap.md).
