# Pairing fixes

- Custom pairing code is exactly 8 alphanumeric characters: `TEAM810B` and is displayed as `TEAM-810B`.
- Pairing uses the canonical `Chrome` browser profile instead of a custom `Edge` label.
- The bot waits for the WhatsApp socket to be ready before requesting the pairing code.
- Credential saving is registered before pairing starts.
- Pairing errors are propagated instead of silently creating a stale/invalid code.
- Telegram and WhatsApp `.pair` handlers use the exact result returned by the current pairing request instead of reading a shared stale code after a fixed 4-second delay.
- Baileys is pinned to the version in the lockfile (`7.0.0-rc13`) instead of the moving `latest` tag.
- Removed an unreachable duplicate return in the Telegram pairing handler.
