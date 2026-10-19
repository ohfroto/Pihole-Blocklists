# Pihole-Blocklists

Curated Pi-hole lists, maintained by hand -- not auto-updating feeds like Hagezi or StevenBlack. Each file here tracks something specific (a documented threat, or one device's exceptions) rather than a broad category, with its sourcing or purpose written into the file's own header comment.

Subscribe to a list in Pi-hole: Settings -> Lists -> Add, using that file's raw URL (`https://raw.githubusercontent.com/ohfroto/Pihole-Blocklists/main/<file>`), setting **Type** to match the file (Block or Allow -- see each entry below).

**Format note on Allow-type lists**: Pi-hole only recognises the ABP exception syntax (`@@||domain^`) for these -- plain `||domain^` lines are silently ignored, and a bare domain with no `@@||...^` wrapper only matches that exact host, not its subdomains. Confirmed empirically, not just from docs.

## Lists

- **[adfection-discover-tech.txt](adfection-discover-tech.txt)** (Block) -- Discover-Tech / Candiru, following Citizen Lab's 2026-10-15 "AdFection" report on zero-click mercenary spyware delivered through targeted ad-bidding. See the file's header for full sourcing, what's complete (the ad-platform domains) and what explicitly isn't (the report names only a handful of ~305 total spyware-validator domains).
- **[work-laptop-allowlist.txt](work-laptop-allowlist.txt)** (Allow) -- exceptions for one device's work tools (Google Analytics/Tag Manager, Microsoft Teams, Slack, Time Doctor, Joplin/OneDrive sync, a handful of affiliate networks, and client-testing tools). Subscribed scoped to a single Pi-hole group containing only that device, via the list's own `groups` field -- every other device keeps full blocking. See the file's header for the full list and why each entry's there.
- **[global-allowlist.txt](global-allowlist.txt)** (Allow) -- exceptions that apply to every device, for personal (not work-specific) use. Subscribed scoped to the Default group, which every client belongs to. First entry: Quidco cashback tracking.
