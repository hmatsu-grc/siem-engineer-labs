# Splunk Search Basics

## Objective

Review foundational Splunk Search & Reporting functionality including search behavior, time range selection, timeline analysis, search modes, and query construction.

---

## Search Fundamentals

Reviewed core Splunk search behaviors and syntax rules.

### Traps & Tips

Important search behaviors identified during lab exercises:

- Field names are case-sensitive
- Field values are not case-sensitive
- Wildcards are supported using `*`
- Boolean operators supported:
  - `AND`
  - `OR`
  - `NOT`

---

## Time Range Selection

Splunk supports multiple methods for selecting searchable event time ranges.

### Presets

Common preset time ranges include:
- Today
- Last 24 hours
- Last week
- Last month
- Last year

---

### Relative Time

Relative time searches include:
- beginning of the hour
- X minutes ago
- X hours ago
- X days ago
- X weeks ago

---

### Real-Time Search

Real-time search allows live monitoring of incoming events as they occur.

Common use cases include:
- live event monitoring
- alert observation
- active investigation visibility

---

### Date Range

Allows searching between fixed calendar dates.

Example:

```text
00:00:00 DD/MM/YYYY → 24:00:00 DD/MM/YYYY
```

---

### Date & Time Range

Allows precise filtering using both date and time values.

Useful for:
- narrowing investigation windows
- forensic analysis
- incident review

---

## Timeline Visualization

Splunk automatically generates a timeline showing event distribution over time.

Timeline analysis helps:
- identify event spikes
- detect unusual activity
- isolate suspicious time periods
- focus investigations on specific event windows

---

## Search Modes

Reviewed available Splunk search modes.

| Mode | Purpose |
|---|---|
| Fast Mode | Reduced processing for faster searches |
| Smart Mode | Balanced performance and field extraction |
| Verbose Mode | Full event and field extraction |

Smart Mode was primarily used during lab exercises.

---

## Search Bar

Reviewed Splunk Search & Reporting query functionality.

Searches can combine:
- wildcards
- searchable fields
- Boolean operators
- event filtering logic

---

## Fields Panel

Reviewed searchable event fields and extracted metadata available within Search & Reporting.

Field analysis included:
- field names
- field values
- field frequency
- searchable metadata

---

## Search History

Reviewed Splunk Search History functionality for recalling previously executed searches.

---

## Notes

Performed foundational Splunk search exercises using Windows Event Log data ingested through a local Universal Forwarder configuration.

---

## References

- https://docs.splunk.com/Documentation/Splunk
