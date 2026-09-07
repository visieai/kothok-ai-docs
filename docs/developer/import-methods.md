# Import methods

Four ways to get products in. Pick one. A store can use only one at a time, and
picking a new one replaces the old one.

| Way | Use it when | Your work |
|---|---|---|
| **Website** | It is a normal online shop | None. The owner does it from the dashboard. |
| **File** | Products can be saved as a CSV | None. The owner does it from the dashboard. |
| **Feed** | The shop already publishes a product feed | Give us the feed address once. |
| **Push** | The shop is custom built, or the other three do not fit | An API call. See the [Push API](push-api.md). |

If Website or File works, you are not needed. Point the owner at the dashboard.

## Website

We read the store's own web pages. No API and no work from you. The owner runs it
from the dashboard.

## File

The owner uploads a CSV, TSV, or TXT file (up to 5 MB) from the dashboard. The
column names we read are in [Feed & CSV columns](feed-csv-columns.md).

## Feed

The shop publishes a CSV or XML feed at a web address that does not change. A Google
Merchant feed works as it is.

Give that address to the dashboard once, and we read it each time a sync runs.

The column names we look for are in [Feed & CSV columns](feed-csv-columns.md). If
your feed uses other names, rename them or use Push instead.

!!! warning "A feed is not read on a timer yet"
    A feed is read only when a sync runs, and a sync is started from the dashboard.
    If prices change often, use Push, which updates the moment you call it.

## Push

Your system sends products to us over an API. Use this if the shop is custom built,
or if prices change often and you want to send updates as they happen.

Push updates the database and the search index in the same call, so there is no sync
step. Full detail is in the [Push API](push-api.md).
