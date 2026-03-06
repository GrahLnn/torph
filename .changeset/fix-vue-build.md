---
"torph": patch
---

Fix Vue build failing to resolve `torph` package entry. Replaced `.vue` SFC with compiled `defineComponent` so tsup can bundle it directly, and simplified the Vue tsup config to a single build step with proper type generation.
