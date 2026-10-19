# ChatSorter 1.4.5 — Minecraft 26.2

Separate client-side Fabric build of ChatSorter, adapted from the 1.4.5 feature set for Minecraft 26.2. The Minecraft 1.21.11 project remains a separate line.

## Ported in this alpha source

- Chat categories: General, DMs, Spy, Console, and All.
- Independent category filters; All toggles the complete category set.
- Search across retained vanilla chat messages, unread DM count, and chat position/resize controls.
- Right-click copy with the original message time, keyword alert settings, session diagnostics, and notification history.
- 26.2 Mojang-name GUI/chat hooks and visible-message filtering.

Some 1.4.5 internals still need porting and verification, including durable per-server chat archive/restore, repeat collapsing, richer multi-option copy/context actions, and independent system-audio playback. This is source for an alpha port, not a tested release JAR.

## Build

Requires Java 25 and Gradle 9.8.1 or newer. The configured target is Minecraft 26.2, Fabric Loader 0.19.3, Fabric API 0.161.0+26.2, and Fabric Loom 1.18.2. The 26.2 GUI changes are adapted: screen management now goes through `Minecraft.gui`, and chat access through `Minecraft.gui.hud`.

Run `gradle build`; the distributable JAR is created in `build/libs/`. The GitHub Actions workflow runs compilation with Java 25 and uploads the build log and JAR on success.
