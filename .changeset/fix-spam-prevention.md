---
"torph": patch
---

Fix animation spam when text changes rapidly

- Merge transform and opacity into a single animation keyframe for enter/persist to prevent flash on interruption
- Capture computed opacity when detaching exiting elements so interrupted fade-outs resume correctly
- Reuse existing DOM elements for persistent segments instead of recreating them
