# Creating and Managing Splunk Reports

## Objective

Create, save, manage, and review Splunk reports for monitoring Windows security events and recurring investigative searches.

---

## Report Overview

Splunk reports are saved search results that allow analysts to quickly access frequently used queries without rewriting them manually.

Reports can be:
- scheduled to run automatically
- executed manually on demand
- shared across analysts and teams

---

## Exercise: Failed Login Detection Report

Created a report to identify failed Windows login attempts involving administrative accounts.

---

## Search Query

Executed the following SPL query:

```spl
source="WinEventLog:*" index="main" EventCode=4625 AND accountname=Admin
```

### Purpose

Searches for failed Windows logon attempts associated with administrative accounts.

### Notes

Windows Event ID:

```text
4625
```

represents a failed logon attempt.

Depending on the dataset, the account field may appear as:
- `accountname`
- `Nom_du_compte`

---

## Running the Search

Executed the SPL query within:

```text
Search & Reporting
```

Reviewed returned Windows security events prior to report creation.

---

## Saving the Search as a Report

Saved the search using:

```text
Save As → Report
```

Configured:
- report title
- report description
- report visibility settings

---

## Viewing the Report

Opened the saved report using:

```text
View
```

Verified:
- saved query execution
- searchable event visibility
- report functionality

---

## Managing Existing Reports

Reviewed Splunk report management functionality.

Navigation path:

```text
Search & Reporting → Reports
```

---

## Editing Reports

Reviewed available report modification options including:
- modifying SPL queries
- changing schedules
- updating report titles
- updating descriptions
- deleting reports

---

## SOC Analyst Use Cases

Splunk reports are useful for monitoring recurring security events such as:
- failed login attempts
- brute-force activity
- suspicious IP activity
- malware alerts
- unauthorized access attempts

Saving frequently used queries as reports help analysts:
- investigate incidents faster
- standardize recurring searches
- automate monitoring workflows
- improve SOC visibility

---

## Notes

Performed report creation and management exercises using locally ingested Windows Event Log data within a Splunk Enterprise lab environment.

---

## References

- [Create and Edit Reports](https://help.splunk.com/en/splunk-enterprise/create-dashboards-and-reports/reporting-manual/9.1/report-management/create-and-edit-reports)
