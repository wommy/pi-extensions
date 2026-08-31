---
"@narumitw/pi-usage": patch
---

Stop reading a captured extension context's model from timer and microtask callbacks after session replacement or reload, so a stale context no longer throws an uncaught exception that exits Pi.
