# serveryapper-hardware
Sends alerts via [Mailgun](https://www.npmjs.com/package/mailgun-js) when [conkie-stats](https://www.npmjs.com/package/conkie-stats) reports dangerous hardware stats.

## ENV
All are required:
* `MAILGUN_API_KEY` e.g. key-randomfj2930fj3jpjawf903
* `MAILGUN_DOMAIN` e.g. yourdomain.com
* `SEND_EMAILS_FROM` e.g. Your Trusty Server <noreply@yourdomain.com>
* `SEND_EMAILS_TO` e.g. Admin <your.name@popularmailhost.com>
* `MIN_MESSAGE_INTERVAL` Minimum amount of time in minutes after sending a warning or danger message to then send a recovery message for the same stat. Intended to prevent lots of emails when a stat wavers back and forth around a threshold. Recommended: 60.
* `MEMORY_WARN` 0-1 % of total RAM + swap use over which to warn
* `MEMORY_DANGER` more severe warning
* `DISK_WARN` 0-1 % of disk use (for any volume) over which to warn
* `DISK_DANGER` more severe warning
* `TEMP_WARN` temperature in Celsius over which to warn
* `TEMP_DANGER` more severe warning
* `POLL_FREQ` Interval in ms at which conkie-stats checks for new stats

## Contributing
Contributions are welcome. A minimal approach was taken, but if you wish to use this and also wish to have more functionality or customization than currently exists, I'd love to pull your additions.
