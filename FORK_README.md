# Fork Changes

Personal fork of [elecwhat](https://github.com/piec/elecwhat), frozen at v1.12.1.

## Why Fork

This is a WhatsApp client tied to a personal account — the code needs to be trustworthy. The AUR package (`elecwhat-bin`) downloads a prebuilt binary, which is not ideal for something with access to personal messages. This fork exists to:

- **Build from source** via a custom PKGBUILD (`rd-elecwhat`), so the code can be reviewed before running.
- **Freeze at a known-good version** — no upstream updates are pulled in automatically. AUR/pacman updates won't change this package.
- **Use system Electron** (`electron36`) instead of the bundled one.

The upstream feature additions (shortcuts, etc.) are unnecessary — basic WhatsApp browsing with `notify-send` notifications is sufficient.

## Changes

- `elecwhat.sh` - Launch script that uses system `electron36` instead of the bundled Electron.
