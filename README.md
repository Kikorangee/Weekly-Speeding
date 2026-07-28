# Speeding Monitor — Top 10% Manager Summary

This version adds a dedicated manager-action summary and a one-click,
summary-only PDF export to the supplied MyGeotab Speeding Monitor.

## Summary logic

- Only vehicles with at least one speeding event are included in the ranking.
- A vehicle appears when it is at or above the 90th-percentile threshold for:
  - number of events;
  - total speeding time;
  - maximum speed; or
  - average speed over the limit.
- `Flagged For` names every measure that caused inclusion.
- Rows are ordered by number of qualifying measures, then total speeding time.
- Existing warning and critical flags remain visible.

## PDF

The **Download Summary PDF** button creates a landscape report containing only
the top-decile manager summary. It includes the database, selected date range,
generation time, recommendation context and a safety disclaimer.

The export uses jsPDF and jsPDF AutoTable from public CDNs, so the browser must
be able to reach those CDN URLs.

## Install

1. Open MyGeotab.
2. Go to **Administration → System Settings → Add-Ins**.
3. Replace the existing Speeding Monitor configuration with the contents of
   `speeding-monitor-embedded-config.json`.
4. Save and hard-refresh with `Ctrl+Shift+R`.

The standalone `speeding-monitor.html` is also included for inspection and
external hosting.
