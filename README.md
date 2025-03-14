# Google Ads MCC Label Assignment Script

This Google Ads Script automates the process of assigning labels to multiple client accounts within a Manager (MCC) account using data provided in a Google Sheet. It verifies the existence of labels at the MCC level, creates labels if necessary, and applies them to the specified accounts.

---

## Features

- **Batch Label Assignment:** Efficiently assigns labels to multiple accounts based on a Google Sheet.
- **Automated Label Management:** Automatically verifies or creates labels at the MCC level.
- **Reporting:** Generates execution logs and optionally sends an email report.
- **Data Validation:** Checks and validates Customer IDs (CIDs) and label data to prevent errors.

---

## Installation

Follow these steps to set up and use the script:

1. **Set Up Google Sheet:**
   - Create or use an existing Google Sheet.
   - Ensure it has columns for Customer IDs (CIDs) and Labels (default: CID in Column C, Label in Column I).

2. **Open Google Ads Scripts:**
   - Sign in to your MCC account at [ads.google.com](https://ads.google.com).
   - Navigate to Tools & Settings → Bulk Actions → Scripts.

3. **Create a New Script:**
   - Click the '+' button to create a new script.
   - Delete any default code present.

4. **Paste the Script:**
   - Copy and paste the provided MCC Label Assignment script into the editor.

5. **Configure the Script:**
   Update the `CONFIG` section with your specifics:

   ```javascript
   const CONFIG = {
     SPREADSHEET_URL: 'your-google-sheet-url', // URL of your Google Sheet
     SHEET_NAME: 'Master Sheet', // Sheet name containing data
     CID_COLUMN: 3, // Column for Customer IDs (C by default)
     LABEL_COLUMN: 9, // Column for Labels (I by default)
     EMAIL_REPORT: true, // Set to true if email report is desired
     REPORT_EMAIL_ADDRESS: 'your-email@example.com', // Email for reports
   };
   ```

6. **Authorize and Run the Script:**
   - Click "Authorize" to grant required permissions.
   - Click "Run" to execute.

7. **Scheduling (Optional):**
   - Set a schedule (e.g., daily or weekly) to automate label assignments.

---

## Reporting

The script logs each operation clearly, noting successes, errors, or skipped rows. Logs are viewable within the Google Ads interface and optionally emailed as a detailed report.

---

## Troubleshooting

- **Label Issues:** Confirm labels are accurately named in your sheet and match existing labels in MCC.
- **CID Issues:** Ensure CIDs are correctly formatted as 10-digit IDs.
- **Permissions:** Confirm the script has sufficient permissions to access your Google Sheet and Google Ads account.

---

## Support

Contact your Google Ads representative or script developer for additional assistance or customizations.

