# TobiAkiode catalogue relay

This directory exposes a validated public copy of the product catalogue already published by `tobiakiode.com`.

- Source of truth: FluentCart on `https://tobiakiode.com/shop/`
- Upstream feed: `https://tobiakiode.com/wp-content/uploads/tobiakiode-fluentcart-tiktok-catalog.csv`
- Refresh cadence: every 15 minutes, with no commit when the validated content is unchanged
- Consumer cadence: TikTok Catalog Manager imports hourly
- Failure mode: the last validated file remains available when the upstream request or validation fails

The workflow rejects empty catalogues, duplicate or blank SKUs, missing required fields, non-HTTPS product/image links, invalid GBP price formatting, and unexpectedly large catalogues.
