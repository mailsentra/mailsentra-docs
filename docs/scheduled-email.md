# Scheduled Email

The Pro Scheduled Email report has two views:

- **Observed Email Attempts** groups logged email attempts that occurred during WP-Cron or Action Scheduler callbacks. Manual sends appear in Email Logs instead.
- **Scheduled Jobs** lists upcoming or due WP-Cron events and pending Action Scheduler actions visible to the site.

The report only observes scheduled callbacks that call `wp_mail()`. It does not guarantee that a job will run. WP-Cron generally needs site traffic unless a system cron is configured. A due job is waiting for its scheduler; it is not proof that execution succeeded.

Times are displayed in the site's timezone. Action Scheduler details are available only when the corresponding action ID was captured and the scheduler is available.