# Casino Data

Central data source for the **Casino Affiliate Table** WordPress plugin. Every site running the plugin fetches `casinos.json` from this repository — edit it here once and all sites update.

## Updating offers

1. Open `casinos.json` → click the pencil icon (**Edit**) → make your changes → **Commit changes**.
2. Sites pick the change up automatically within the plugin's cache window (default 30 minutes). For an instant refresh on a site: **Settings → Casino Affiliate Table → Flush Cache Now**.

## Connecting a WordPress site

1. Open `casinos.json` in this repo → click **Raw** → copy the URL (looks like `https://raw.githubusercontent.com/Kami126/casino-data/main/casinos.json`).
2. On the site: **Settings → Casino Affiliate Table → Casinos JSON URL** → paste → Save.

If this file is ever unreachable, the plugin automatically falls back to the copy bundled inside it — the table never disappears.

## Field reference

| Field | Meaning |
|---|---|
| `name` | Casino name shown in the table |
| `logo_url` | Full image URL, or a bare filename (e.g. `spinjo.svg`) resolved against the plugin's bundled `assets/logos/` |
| `bonus` | Welcome bonus text |
| `features` | Comma-separated feature list |
| `cta_text` | Button label (defaults to "العب الآن" if empty) |
| `cta_url` | Affiliate link |
| `payment_methods` | Comma-separated (Visa, Mastercard, Skrill, Neteller, Bitcoin, PayPal, Ethereum, USDT, Litecoin, Ripple, Apple Pay, Google Pay, EcoPayz, Paysafecard, Bank Transfer) |
| `accepts_players` | Text; `{country}` is replaced with the visitor's country when geo-detection is enabled |
| `enabled` | `true` / `false` — only `true` rows are shown |
| `priority` | Number; lower appears first |
