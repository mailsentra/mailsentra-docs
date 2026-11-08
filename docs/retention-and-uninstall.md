# Retention and Uninstall

Configure retention in **MailSentra > Settings**.

- **Retention period** removes logs older than the configured number of days. Set it to `0` to disable age-based deletion.
- **Maximum log entries** removes the oldest logs when the configured row count is exceeded. Set it to `0` to disable the row limit.

Cleanup runs through WP-Cron when the site receives traffic. Each run removes up to 500 rows and aims to stop starting database work after about two seconds; an individual query may take longer. Follow-up runs continue cleanup in batches. A system cron can be used if the site does not receive regular traffic.

The **Delete logs when the plugin is uninstalled** setting controls whether MailSentra drops its log table during uninstall. Deactivation alone retains logs.