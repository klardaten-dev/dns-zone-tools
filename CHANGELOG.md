# Changelog

## 1.0.1
- **Reformat Code** (Ctrl+Alt+L) for zone files: owner, TTL, class, type and record data are lined up in columns, one grid
  for the whole file. Spaces or tabs follow what the file already uses. A few very long owner names (DKIM selectors) don't
  widen the grid, and a TTL or class used only by a few records (often just `IN` on the SOA) doesn't get a column of its own.
  Continuation lines of multi-line records move with the data, so a hand-aligned SOA keeps its shape. Only whitespace
  changes: record data and comments stay as they are, trailing whitespace is removed. Checked on 1,427 zone files from
  BIND, Knot, NSD, ldns and PowerDNS: dnspython reads every formatted file as exactly the same zone.
- `named.root`, `root.hints`, `named.ca`, `db.local`, `db.127`, `db.0`, `db.255`, `db.empty`, `db.root`, `db.cache` open
  as zone files.

## 1.0.0
First release: highlighting, record data validation for 70+ record types, missing-trailing-dot detection with quick
fixes, zone checks (CNAME conflicts, alias/IP targets, glue, out-of-zone data, TTLs, duplicates), SPF/DMARC checks,
SRV/TLSA/CAA naming, DNSSEC parameter hints, "Update SOA serial" intention, completion, navigation, documentation, folding.
