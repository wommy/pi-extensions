---
"@narumitw/pi-github-pr": patch
---

Survive a stale extension ctx in delayed status callbacks. The pull request expiry timer and the
branch watcher both hold a captured ctx, which goes stale after session replacement or reload; the
status writes and session-manager reads they make are now guarded so a stale ctx stops the work
quietly instead of exiting the agent with an uncaught exception.
