=== GSheet SFTP Sync ===
Contributors: olivierbigras
Donate link: https://olivierbigras.com
Plugin URI: https://olivierbigras.com
Tags: google sheets, sftp, sync, automation, csv, export
Requires at least: 5.0
Tested up to: 6.4
Stable tag: 1.1.0
Requires PHP: 7.4
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Automatically receive Google Sheets exports and upload them to your SFTP server. Perfect for daily automated syncs.

== Description ==

GSheet SFTP Sync allows you to automatically export Google Sheets and upload them to any SFTP server. This is perfect for:

* Daily inventory updates from Google Sheets
* Automated data feeds for e-commerce
* Syncing spreadsheet data to your server
* Backing up Google Sheets to your own server

**Features:**

* **Easy Setup** – Configure everything from the WordPress admin
* **Secure API** – Auto-generated API keys protect your endpoint
* **REST API Endpoint** – Receives files from Google Apps Script
* **SFTP Upload** – Automatically uploads to your SFTP server
* **Activity Logs** – Track all uploads and errors
* **Pre-built Script** – Copy-paste Google Apps Script included
* **100% Free** – No paid services required

**How It Works:**

1. Install and activate the plugin
2. Configure your SFTP credentials in Settings
3. Copy the provided Google Apps Script to your Sheet
4. Set up a daily trigger in Google Apps Script
5. Your sheet automatically syncs to your SFTP server

== Installation ==

1. Upload the `gsheet-sftp-sync` folder to `/wp-content/plugins/`
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Go to Settings → GSheet SFTP Sync
4. Enter your SFTP server credentials
5. Click "Test SFTP Connection" to verify
6. Copy the Google Apps Script from the settings page
7. Paste into your Google Sheet (Extensions → Apps Script)
8. Run `setupTrigger()` to enable daily exports

== Frequently Asked Questions ==

= What SFTP libraries are supported? =

The plugin supports both the PHP ssh2 extension and phpseclib. If neither is available, you can install phpseclib via Composer.

= Is this really 100% free? =

Yes! This solution uses Google Apps Script (free) and your existing SFTP server. No third-party paid services required.

= Can I export as XLSX instead of CSV? =

Yes! Change `EXPORT_FORMAT: 'csv'` to `EXPORT_FORMAT: 'xlsx'` in the Google Apps Script configuration.

= How do I change the export schedule? =

In the Google Apps Script, change `SCHEDULE: 'daily'` to `SCHEDULE: 'hourly'` for hourly exports, or modify `DAILY_HOUR` to change the time.

= Is the API secure? =

Yes. All requests require a valid API key. The key is auto-generated on activation and can be regenerated anytime.

= Can I use this with multiple Google Sheets? =

Yes! Each Google Sheet can have its own Apps Script. They can all point to the same WordPress endpoint.

== Screenshots ==

1. Settings page with SFTP configuration
2. API endpoint and key display
3. Activity logs showing successful uploads
4. Google Apps Script code generator

== Changelog ==

= 1.1.0 =
* Added Export Settings section in admin
* New schedule options: Daily or Hourly
* New filename mode: Dated (unique files) or Overwrite (same file each time)
* Configurable base filename and export format (CSV/XLSX)
* Apps Script now auto-configured with plugin settings
* Improved SFTP error messages for debugging

= 1.0.0 =
* Initial release
* SFTP upload via ssh2 or phpseclib
* REST API endpoint for receiving files
* Admin settings page
* Activity logging
* Google Apps Script generator

== Upgrade Notice ==

= 1.1.0 =
New export settings! Configure schedule, filename mode, and format directly in the plugin.

= 1.0.0 =
Initial release of GSheet SFTP Sync.
