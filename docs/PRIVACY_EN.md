# QuotaDock beta privacy information

This describes beta 0.6.10 as of October 16, 2026. QuotaDock has no own account registration, advertising, analytics SDK or usage-collection server. Provider sign-in and queries communicate with the official services, whose policies also apply. [한국어](PRIVACY.md)

## Local storage

App preferences contain hashed account identifiers, plans, quota readings and timestamps, exposed benefit metadata, subscription dates and short date-evidence excerpts, manually entered prices/notes, reminders, settings and CLI paths. Raw emails and organization IDs used for identification are hashed during the query rather than stored in app preferences.

Successful quota history is bounded to 90 days and 30,000 observations. Persisted alert lists retain the latest 60 events. Deduplication state, latest snapshots, saved reset schedules and subscription notes do not share that 90-day automatic deletion rule.

## Sign-in sessions

Provider-specific app-owned WebKit profiles can persist cookies, website storage and caches. Passwords are entered into official web pages; QuotaDock does not read login-form values or send them to its own server. Chrome cookies are not imported. Official CLIs may refresh authentication and manage their own caches/logs. Disconnecting in QuotaDock is not CLI logout.

## Optional token collection

Enabling collection reads bounded portions of local Codex/Claude JSONL files and Grok Build usage/summary metadata. Codex/Claude files can contain conversations alongside usage records. The parser retains numeric metadata, timestamps and identifiers needed for deduplication, not conversation text, and uploads none of those logs. Results and file fingerprints stay in memory until collection is disabled or the app quits. Multiple local accounts and projects can be aggregated together.

## Exports and feedback

JSON backups are unencrypted and contain account identifiers, dates, prices and usage history. Do not attach backups to public issues. Exported backups omit web evidence excerpts. ICS exports can be imported into another calendar at your choice.

Feedback is voluntary and is never sent automatically. GitHub issues are public. Do not include emails, account IDs, tokens, cookies, billing details, conversations, original logs or backups. The feedback host's privacy policy also applies.

## Disconnecting and deletion

Disconnecting keeps historical readings, saved schedules and notes. Deleting the app does not erase all preferences or web sessions. This beta has no single control to remove all local state and web profiles. Sign out in each official app-owned web window and manage CLI authentication in the CLI.

To erase app preferences, quit the app and, at your own choice, run `defaults delete local.quotadock.app` in Terminal. This deletes app settings and saved quota/subscription history; privately back up first if you need recovery. It does not delete WebKit profiles or CLI authentication/logs. Macs that used the older QuotaPilot prototype can reimport that older preference domain and need separate cleanup guidance.
