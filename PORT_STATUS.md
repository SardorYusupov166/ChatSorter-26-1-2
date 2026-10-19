# Port status: ChatSorter 1.4.5 → Minecraft 26.2

This is an alpha source port. The first Java 25 CI compile found one reference to the removed `Options.hideGui` field; it has been changed to `Minecraft.gui.hud.isHidden()`. The workspace cannot run Gradle locally because it has Java 17 and no Gradle installation. A corrected CI compile and a Minecraft launch test are still pending.

The branch uses 26.2 Mojang names and the modern ChatComponent hooks. Minecraft 26.2 screen access is routed through `Minecraft.gui`; chat HUD access uses `Minecraft.gui.hud`. It contains no old `ChatHudMixin` / `ChatHudAccess` Yarn sources and does not hide stale source files with compiler excludes. A GitHub Actions workflow compiles with Java 25 and retains the build log for review.

Ported core: category routing, independent filters with an All toggle, search, unread DM count, chat positioning/resizing, timestamped right-click copy, keyword alert settings, notification history, and diagnostics.

Remaining parity work before calling this a full 1.4.5 alternative: durable per-server chat archive and restore, repeat collapsing, the full multi-action copy/context menu, and independent system-audio playback. A successful corrected Java 25 compile and a Minecraft launch test are still required to validate 26.2 APIs and Mixin targets.
