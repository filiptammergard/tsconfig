---
"@tammergard/tsconfig": major
---

Enable additional strict type-checking rules and drop redundant flag.

- Enable `noImplicitOverride`, `noImplicitReturns`, and
  `noUncheckedSideEffectImports`. These may surface new type errors in
  consumer projects.
- Remove `forceConsistentCasingInFileNames` since it is the default since
  TypeScript 5.0 (and this package now requires TypeScript 6+).
