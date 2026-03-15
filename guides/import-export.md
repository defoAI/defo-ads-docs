# Import & Export Guide

This guide covers how to import campaigns from your connected advertising platforms into Defo Ads, and how to export campaigns from Defo Ads to those platforms. It also covers CSV-based import and export for offline editing.

> **How to access Import / Export:**
> Go to **Sync** in the sidebar, then click **Open Import / Export** at the bottom of the Sync page. You can also navigate directly to `/import-export`.

---

## Importing Campaigns from Platforms

### Platform Selection

1. Navigate to **Campaigns > Import**.
2. Select the platform you want to import from (e.g., Google Ads or Microsoft Advertising).
3. Only platforms you have connected will appear in the list. See [Connections](../premium/integrations.md) to connect a platform.

### Campaign Preview

Before importing, Defo Ads shows a preview of what will be imported:

- A list of all campaigns found on the selected platform.
- Each campaign shows its name, type, status, and the number of ad groups, keywords, and ads it contains.
- Review the preview to understand what will be brought into Defo Ads.

### Selective Import

You do not have to import everything. You can choose specific campaigns:

1. In the import preview, use the checkboxes to select or deselect individual campaigns.
2. By default, all campaigns are selected.
3. Deselect any campaigns you do not want to import.
4. Click **Import Selected** to begin the import.

![Import Campaign Selection](../images/sync-import-campaign-selection.png)

### What Gets Imported

The import pulls the full campaign hierarchy for each selected campaign:

| Entity | Details |
|--------|---------|
| **Campaigns** | Name, type, status, budget, bidding strategy, targeting settings |
| **Ad Groups** | Name, status, default bid |
| **Keywords** | Text, match type, bid, status (including negative keywords) |
| **Ads** | Headlines, descriptions, display URLs, final URLs, status |

---

## Exporting Campaigns to Platforms

### Platform Selection

1. Navigate to **Campaigns > Export**.
2. Select the target platform you want to export to.
3. Choose which campaigns to export.

### Validation Before Export

Before exporting, Defo Ads runs platform compatibility checks:

- **Campaign type compatibility** — Verifies the campaign type is supported on the target platform. For example, Shopping campaigns require a linked Merchant Center account on Google Ads.
- **Required fields** — Checks that all required fields for the target platform are filled in (e.g., final URLs on ads, budget on campaigns).
- **Character limits** — Validates that ad copy (headlines, descriptions) meets the target platform's character limits.
- **Keyword restrictions** — Checks for keyword match types or formats not supported on the target platform.

If validation finds issues, they are displayed before the export begins. You can fix them and retry, or proceed with the valid entities only.

![Export Validation Warnings](../images/export-validation-warnings.png)

### Export Progress Tracking

During export, Defo Ads shows:

- A progress bar indicating the percentage of entities exported.
- A real-time log of which entities have been successfully pushed.
- Any errors or warnings that occurred during export.

After the export completes, a summary shows the total number of campaigns, ad groups, keywords, and ads successfully exported.

![Export Campaign Selection](../images/sync-export-campaign-selection.png)

---

## Platform-Specific Notes

### Google Ads

- All campaign types supported by Defo Ads (Search, Display, Video, Shopping, Performance Max) can be exported to Google Ads.
- Performance Max campaigns require asset groups, which are validated before export.
- Shopping campaigns require a linked Google Merchant Center account.

### Microsoft Advertising

- **Display campaigns** are automatically converted to **Audience campaigns** during export, as Microsoft Advertising does not have a Display campaign type.
- **Broad match negative keywords** are automatically converted to **phrase match**, since Microsoft Advertising does not support broad match for negative keywords.
- Video and Shopping campaign types may have limited support depending on your Microsoft Advertising account configuration.

---

## CSV Import & Export

Defo Ads supports CSV-based import and export in a format compatible with **Google Ads Editor**.

### CSV Export

1. Navigate to **Campaigns > Export**.
2. Select **CSV** as the export format.
3. Choose the campaigns you want to export.
4. Click **Export to CSV**.
5. A CSV file will be downloaded to your computer.

The exported CSV follows the Google Ads Editor format, making it easy to open in Google Ads Editor or any spreadsheet application for offline review and editing.

### CSV Import

1. Navigate to **Campaigns > Import**.
2. Select **CSV** as the import source.
3. Upload your CSV file. The file must follow the Google Ads Editor compatible format.
4. Defo Ads will parse the file and show a preview of the campaigns, ad groups, keywords, and ads found.
5. Review the preview and click **Import** to bring the data into Defo Ads.

![CSV Import Dialog](../images/import-csv-dialog.png)

### CSV Format Requirements

- The CSV must follow the **Google Ads Editor** column format.
- Required columns vary by entity type (campaign, ad group, keyword, ad).
- Encoding must be UTF-8.
- The first row must contain column headers.

> **Tip:** The easiest way to get a correctly formatted CSV is to export from Defo Ads first, edit the file, and then re-import it.

---

## Related

- [Connections](../premium/integrations.md) — Connect your ad platforms
- [Sync](../premium/sync.md) — Keep platforms in sync after import/export
