# Troubleshooting

## No logs appear

- Confirm logging is enabled in **MailSentra > Settings**.
- Confirm the site is sending through WordPress `wp_mail()`; mail sent outside that path may not be observed.
- Check that the WordPress database is available and that the MailSentra database table exists.

## A log remains Pending

The attempt may still be running, or WordPress may not have called a result hook MailSentra observes. Check the mail provider and site logs for more detail.

## A log says Sent by site, but the message did not arrive

That status reflects the result reported by WordPress; it is not inbox delivery confirmation. Check the recipient's spam folder and your SMTP or email provider's delivery and bounce logs.

## Some message details are missing

The active logging mode may omit those fields. Privacy-focused and Custom settings affect new logs only. Older entries may not have capture-state information.

## Pro reports are unavailable

Confirm that Freemius recognizes an eligible Pro license. Also check that optional features such as WooCommerce Email Activity are enabled in Pro Settings.

## Retention cleanup has not run

WP-Cron needs site traffic unless you have configured a system cron. Cleanup works in bounded batches, so a large backlog may take several runs to clear.