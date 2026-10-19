# Pihole-Blocklists

Curated Pi-hole blocklists, maintained by hand -- not auto-updating feeds like Hagezi or StevenBlack. Each file here tracks a specific, documented threat or tracker rather than a broad category, with its sourcing written into the file's own header comment.

Subscribe to a list in Pi-hole: Settings -> Lists -> Add, using that file's raw URL (`https://raw.githubusercontent.com/ohfroto/Pihole-Blocklists/main/<file>`).

## Lists

- **[adfection-discover-tech.txt](adfection-discover-tech.txt)** -- Discover-Tech / Candiru, following Citizen Lab's 2026-10-15 "AdFection" report on zero-click mercenary spyware delivered through targeted ad-bidding. See the file's header for full sourcing, what's complete (the ad-platform domains) and what explicitly isn't (the report names only a handful of ~305 total spyware-validator domains).
