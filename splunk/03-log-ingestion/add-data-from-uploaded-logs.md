# Add Data from Uploaded Logs

## Objective

Upload and analyze log files in Splunk.

---

## Upload Workflow

### Open Add Data

Navigated to:

```text
Settings → Add Data
```

Selected:

```text
Upload
```

---

### Upload Log File

1. Selected the log file for upload
2. Clicked Next
3. Reviewed how Splunk parsed the uploaded data
4. Continued if parsing configuration appeared correct

---

### Configure Host and Index

1. Selected host field value (if required)
2. Selected destination index
3. Reviewed upload configuration
4. Completed the process and started searching

---

## Verification

Verified:
- Uploaded log data became searchable
- Events appeared within Splunk Search & Reporting
- Uploaded logs were indexed successfully

Performed a basic search to confirm event visibility.

---

## Notes

Splunk automatically parsed uploaded log data prior to indexing and analysis.
