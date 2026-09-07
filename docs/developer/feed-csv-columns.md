# Feed & CSV columns

If you send a Feed or a File (CSV), we look for these column names. The first name
found in each row wins.

| What we need | Names we accept |
|---|---|
| id | `id`, `sku`, `variant_sku`, `handle` |
| title | `title`, `name` |
| description | `description`, `body_(html)` |
| link | `link`, `url`, `product_url` |
| brand | `brand`, `vendor` |
| type | `product_type`, `type`, `google_product_category` |
| tags | `tags` |
| price | `price`, `variant_price`, `regular_price` |
| sale price | `sale_price`, `variant_compare_at_price` |
| in stock | `availability`, `stock_status` |
| currency | `currency`, `price_currency` |
| quantity | `quantity`, `variant_inventory_qty`, `stock_quantity` |
| image | `image_link`, `image`, `image_src` |
| more images | `additional_image_link`, `additional_image_links` |

## What is required

Only **title** and **link** are needed. A row without both is skipped, because it is
usually a header or an extra line for a size or colour.

## File limits

A file must be `.csv`, `.tsv`, or `.txt`, up to 5 MB. Save spreadsheets as CSV
first. Over 5 MB, use a Feed or [Push](push-api.md).

## One thing to watch: sale price

If a row has both a normal price and a sale price, the two become the ends of a
range. A product at 3000 on sale for 1500 is stored as 1500 to 3000.

It is never shown as "was 3000, now 1500," and nothing is marked as on sale. Keep
that in mind during a campaign. See [What it will not do](../assistant/limitations.md).
