---
"emdash": patch
"@emdash-cms/admin": patch
---

fix(admin/media): stabilize Load More callback and surface total count (#1272)

Stabilized the `onLoadMore` handler in `MediaPage` with `useCallback` to match the proven `ContentList` pattern, preventing cursor pagination from getting stuck after 100 items. Added `total` to `MediaListResponse` so the admin displays "Showing X of Y" and users can see when additional pages remain.
