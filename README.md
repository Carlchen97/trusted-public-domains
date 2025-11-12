# Trusted Public Domains

A curated allowlist for **official government domains** and **trusted public institutions** (universities, public broadcasters, international organizations, etc.) intended for use with **AdGuard Home**.

- **Source**: `data/domains.txt` — one domain per line, ASCII/punycode only (no protocols/paths).
- **Artifacts**:
  - `dist/domains.txt` — normalized, deduplicated, sorted
  - `dist/adguard-allowlist.txt` — AdGuard rules (`@@||domain^`)

## Who qualifies
- Government portals, ministries, agencies, regulators
- Public service institutions (universities, public hospitals, national libraries, public broadcasters)
- International/public bodies (e.g., `europa.eu`, `who.int`, `un.org`)

## Contribute (no git skills needed)
- Use the **web form** (GitHub Pages) or open an **Issue** with title `allow: example.gov` and optionally explain why.
- A bot creates a Pull Request to add the domain after basic validation.

## AdGuard Home usage
1. Open **Filters → Allowlist** in AdGuard Home.
2. Paste the content of `dist/adguard-allowlist.txt` (or import the file).
3. Save changes and optionally flush DNS cache.

## Format rules
- Domain or hostname only (e.g., `gov.uk`, `bund.de`, `who.int`). No URLs, no IPs.
- One entry per line; subdomains must be listed separately if desired.
- ASCII only (use punycode for internationalized domains).

## License
MIT (see `LICENSE`).
