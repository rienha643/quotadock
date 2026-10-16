# QuotaDock getting started 0.6.10

QuotaDock brings AI quota limits, renewal dates and saved reset schedules together on macOS. This free beta targets Apple Silicon Macs running macOS 14 or later. [한국어 안내](QUICK_START.md)

## Install

To update, quit QuotaDock and replace the app in Applications. Existing provider connections and local records are retained.

Extract the ZIP and move `QuotaDock.app` to Applications. Quit any running older version before replacing it. This beta is ad-hoc signed; it has no Developer ID signature or Apple notarization. A downloaded copy may be blocked on another Mac.

Only if you trust the source and have verified the release's SHA-256, follow [Apple's instructions](https://support.apple.com/en-us/102445) for an app from an unidentified developer. After attempting to open it, your Mac may offer Open Anyway under System Settings → Privacy & Security. Managed Macs may prohibit this. Stop if macOS reports damage or malware. Do not disable Gatekeeper globally or remove quarantine attributes to get past a warning. Internet-download first launch on another Mac still needs beta validation.

## Connect your tools

Install and sign in to the official Codex CLI, Claude Code or Grok Build for the services you use. On first launch, QuotaDock may discover installed Codex and Claude CLIs and attempt a read-only query. Open Settings to connect tools, disconnect unused providers or choose a nonstandard CLI path. Web subscriptions without the corresponding installed CLI cannot start automatic quota tracking.

The beta focuses on personal subscriptions and adapter-supported responses. Claude Pro/Max personal accounts and Grok Build shared subscription quotas are supported paths; API-key accounts, business accounts and every plan are not guaranteed. Disconnecting in QuotaDock does not sign you out or cancel the provider subscription.

Codex refreshes every five minutes; Claude and Grok every fifteen minutes. Failed queries back off, sleep/offline pauses queries, and manual refresh has a fifteen-second cooldown. Previous successful values remain visible after failure.

## Customize the menu bar

Choose periods and quotas in Settings. You can show session, weekly or model-specific quotas such as Fable. Only successfully queried connected providers appear; the QuotaDock icon appears when none are connected. Percentages mean remaining allowance. Missing data is not zero. The popup includes stale/failure status and the observation time; no tilde prefix is used.

Choose Korean, English or System under Language. Closing the dashboard keeps the menu bar running. Use Command-1 to reopen the dashboard and the app or popup menu to quit.

## Review subscriptions

Open Subscriptions → Connect subscription dates, sign in on the official website, then confirm that the web account matches the connected CLI account. Dates save when you confirm. Browser logins are not copied from Chrome. This is an on-demand web read, not an unattended daily billing sync. Prices and auto-renewal status are manual notes; date typing is not offered.

Verified paid weekly reset observations stay on this Mac after disconnecting. Set a review reminder to reconsider subscribing. Expired reset observations are not projected into a new weekly schedule. Cancel, pay or resubscribe directly with the provider. A saved reset is historical evidence, not proof of access or guaranteed savings. Comparisons use calendar days for date-only billing evidence and hide differences larger than the quota period.

## Benefits and notifications

Codex benefits come from supported official quota responses. Read Claude reset passes from Benefits → Check reset passes and confirm the matching account. That read is separate from CLI quota refresh. Grok reset-pass inventory is unsupported. QuotaDock never consumes a reset pass.

Quota recovery alerts distinguish scheduled and early recovery when observations allow it. After a long gap they report observed recovery without claiming its time or cause. Provider-wide resets cannot be identified from these responses. Billing reviews use saved dates at three and one days before renewal.

Enable macOS notifications in Settings and try the five-second test. Focus, per-app notification settings and screen-sharing settings may hide banners. Delivery confirmation is not confirmation that you saw a banner. In-app review alerts remain available separately.

## Local history and portability

Local token collection is optional in History → Tokens. Enabling it starts a bounded scan. Restarting does not automatically rescan; use Refresh token records. Figures cover inspected local tool logs, not all web/mobile/device usage or subscription quota deductions. Partial totals can grow as previously unscanned files are included, even without new consumption.

Export schedules as ICS or local history/settings as JSON. The backup is unencrypted and includes account identifiers, dates, prices and usage observations. Never post it publicly. It excludes login credentials, conversations, original token logs and CLI paths. Restoration keeps conflicting local notes and imports missing web evidence only when dates agree. Reconnect tools and grant notification permission separately on another Mac.

[Privacy](PRIVACY_EN.md) · [Feedback](FEEDBACK_EN.md)

## Fixed in 0.6.10

Grok can omit the percentage field at zero usage after a weekly reset. QuotaDock now displays 100% remaining only for a verified unified billing response with a complete, valid current period. Explicit null and incomplete periods remain unknown.
