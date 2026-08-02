# CUBL-Mail — Cuandu mail source blocklist (mirror)

Automated mirror of the CUBL-Mail blocklist published at
**<https://ftp.cuandu.org/pub/cuandu/cubl-mail/>** — that page is the
canonical, freshest copy. This mirror updates hourly and may lag it
slightly; in exchange, the commit history doubles as a changelog of
listings.

- [`ips.txt`](ips.txt) — the list: IPv4 addresses and IPv6 /64 networks
  from which we observed spam within the last 90 days. Entries expire
  automatically 90 days after they were last seen.
- [`README.txt`](README.txt) — the canonical documentation (format,
  freshness, delisting).

Raw URL for automated consumption via GitHub:

    https://raw.githubusercontent.com/cuandu/cubl-mail/main/ips.txt

## Delisting

Write to **cubl-mail-delist@cuandu.ch** — issues are disabled on this
repository; the mailbox is the delisting channel.

## License

[CC BY 4.0](LICENSE) — attribute as "CUBL-Mail (cuandu.ch)".
