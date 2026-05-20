---
"@tammergard/tsconfig": major
---

Split base and DOM configs, and drop TypeScript 5 support.

- The base config (`@tammergard/tsconfig`) is now environment-agnostic and no
  longer includes `dom`/`dom.iterable` in `lib` or `jsx`. Browser/React projects
  must extend `@tammergard/tsconfig/dom` instead to keep DOM types and JSX.
- `peerDependencies.typescript` is now `"6"` only. TypeScript 5 is no longer
  supported.
