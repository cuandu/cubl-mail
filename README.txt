CUBL-Mail - Cuandu mail source blocklist
========================================

https://ftp.cuandu.org/pub/cuandu/cubl-mail/ips.txt

What this is
------------
The file ips.txt contains a list of IPv4 addresses and IPv6 networks
from which we have observed spam within the last 90 days. Listings
are based solely on what our own production mail filtering observed,
not on third-party feeds. The exact listing criteria are deliberately
not published so that they remain robust against evasion.

Why we publish it
-----------------
We publish this list because we believe sharing this information
with the community might be helpful - especially since we have
observed that some of these spam sources are missed by other,
similar threat intelligence lists.

Format
------
One entry per line: an IPv4 address, or an IPv6 network in CIDR
notation (IPv6 sources are aggregated to their /64). Each entry
carries a comment with the date the source was last seen. Lines
starting with # are comments. The file is directly usable as an
rspamd map, a pf table file, or a Postfix CIDR source.

Freshness and expiry
--------------------
The list is regenerated hourly. Entries expire automatically 90 days
after the source was last observed; there is nothing to request for
routine aging out. The "Generated:" header line carries the time of
the last rebuild - if it is more than a few hours old, something on
our side is broken and the list should be considered stale.

Mirror
------
An automated mirror with version history - the commit log doubles as
a changelog of listings - is available at:

    https://github.com/cuandu/cubl-mail

This page remains the canonical source; the mirror updates hourly and
may lag it slightly.

Delisting
---------
If your address is listed and you believe this is in error, or you
have fixed the underlying problem (compromised host, open relay,
hijacked account), write to:

    cubl-mail-delist@cuandu.ch

Include the IP address and, if you can, what happened. Delisting
requests are reviewed by a human; verified requests are honored
promptly and the entry is additionally excluded from re-listing while
the underlying observations age out.

License
-------
The list and this documentation are licensed under the Creative
Commons Attribution 4.0 International license (CC BY 4.0):

    https://creativecommons.org/licenses/by/4.0/

You may copy, redistribute and adapt the data for any purpose,
including commercially, provided you give appropriate credit -
"CUBL-Mail (cuandu.ch)" with a link to this page is sufficient.

Terms
-----
The list is provided as-is, without warranty of any kind. It reflects
what one mail operator observed; use it as one signal among several,
at your own judgment and risk.
