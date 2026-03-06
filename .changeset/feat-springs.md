---
"torph": patch
---

Add spring-based easing support

- New `spring()` helper that converts physics parameters (stiffness, damping, mass) into a CSS `linear()` easing and computed duration
- The `ease` option now accepts a `SpringParams` object in addition to CSS easing strings
- Add `MorphController` class for managing instance lifecycle and config changes
- Framework components (React, Svelte, Vue) now use `MorphController` to automatically recreate instances when options change
- Cap fade durations at 150ms so opacity transitions stay snappy with longer spring durations
- Export `spring`, `SpringParams`, and `SpringResult` types
