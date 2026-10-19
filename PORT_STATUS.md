# Port status: ChatSorter 1.4.5 → Minecraft 26.1.2

This is an alpha source port. It is not compile-verified or game-tested in this workspace: the available environment has Java 17 and no Gradle installation, while Minecraft 26.1.2 requires Java 25.

The branch uses 26.1.2 Mojang names and the modern ChatComponent hooks. It contains no old `ChatHudMixin` / `ChatHudAccess` Yarn sources and does not hide stale source files with compiler excludes. A GitHub Actions workflow is included to compile with Java 25 and retain the first build log for review.

Ported core: category routing, independent filters with an All toggle, search, unread DM count, chat positioning/resizing, timestamped right-click copy, keyword alert settings, notification history, and diagnostics.

Remaining parity work before calling this a full 1.4.5 alternative: durable per-server chat archive and restore, repeat collapsing, the full multi-action copy/context menu, and independent system-audio playback. The first Java 25 compile and a Minecraft launch test are also required to validate 26.1.2 APIs and Mixin targets.
