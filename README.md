# Mobile terminal modifier evidence

Captures from owned Herdr test sessions in Google Chrome 154 at 390 × 844 with touch enabled. No running user terminals were captured.

- `sticky-kitty-phone.png`: Ctrl, Alt and Shift held at the same time.
- `input-hint-phone.png`: guidance for direct TUI input and the editable input line.
- `modifier-bytes.log`: received bytes for all seven modifier combinations in legacy and Kitty PTYs, followed by paste, IME, focus and state-reset checks.

The implementation is on [`feat/mobile-sticky-modifiers`](https://github.com/nickadminroot/herdr-web-ui/tree/feat/mobile-sticky-modifiers). Browser/PTY checks run with `bun scripts/sticky-modifiers-regression.ts` after building.

The installed fork was also checked over LAN and Tailscale HTTPS in mobile Chrome against an owned Neovim instance: seven modified-arrow mappings, ordinary text entry, and held Ctrl+[ to leave insert mode. The user tested direct terminal input on a physical phone.
