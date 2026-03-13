# CLAUDE.md

This repository stores Surge and Shadowrocket configuration files plus reusable rule lists published from the repository root.

## Repository Structure

- `*.conf` — user-specific client configs (Shadowrocket/Surge) with sections: `[General]`, `[Proxy]`, `[Proxy Group]`, `[Rule]`, `[Host]`
- `*.list` — shared rule sets consumed by config files via raw GitHub URLs
- `*.sgmodule` — Surge module files
- `*.yaml` — ClashMeta/Mihomo configuration
- `*-singbox.json` — sing-box configuration

## Rule Lists

| File | Purpose |
|------|---------|
| `LAN.list` | Local/private network ranges → DIRECT |
| `SYSTEM.list` | Apple/system services → DIRECT |
| `ANDROID.list` | Android services → DIRECT |
| `proxy.list` | General proxy domains |
| `proxy-google.list` | Google services → VPN |
| `proxy-youtube.list` | YouTube → VPN |
| `proxy-geoip.list` | GeoIP-based proxy rules |
| `telegram.list` | Telegram → VPN |
| `whatsapp.list` | WhatsApp → VPN |
| `roblox.list` | Roblox → VPN |
| `v2raytun-proxy.list` | v2rayTun proxy rules |

## User Configs

`hunter44x.conf`, `jazz.conf`, `alexeev.conf`, `bychkov.conf`, `kketoeva.conf`, `kutsenko.conf`, `lebedeva.conf`, `losinskiy.conf`, `okkaiot.conf`, `ros.conf`, `tkach.conf`, `vika.conf`

Each user config shares the same structure with user-specific proxy server entries.

## Editing Guidelines

- Preserve existing section order and formatting in `*.conf` files unless a change explicitly requires restructuring.
- Keep rule ordering stable: LAN/system-direct rules before proxy rules.
- Add new list entries as one rule per line; keep comments concise and avoid duplicate domains or CIDRs.
- Do not rename published rule files or change raw GitHub paths unless the task explicitly includes that migration.
- Prefer small, surgical edits — several config files share the same structure with user-specific variations.
- After edits, sanity-check touched files for section continuity, valid comma-separated rule syntax, and accidental duplicate entries.

## No Automated Tests

There is no test suite. Manual validation: check section continuity, valid rule syntax, no duplicate entries.
