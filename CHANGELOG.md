# @tammergard/tsconfig

## 3.0.2

### Patch Changes

- 8b99306: Use `devEngines` instead of `engines` for the Node version requirement, so it applies to development only and no longer constrains consumers of the package.

## 3.0.1

### Patch Changes

- 1bbad77: Align project configuration with other `@tammergard/*` packages: sort
  `package.json` keys, declare `engines.node >= 24`, switch release workflow to
  npm trusted publishing, and update the changesets schema URL to match the
  actually installed version.

## 3.0.0

### Major Changes

- 76bc604: Enable additional strict type-checking rules and drop redundant flag.
  - Enable `noImplicitOverride`, `noImplicitReturns`, and
    `noUncheckedSideEffectImports`. These may surface new type errors in
    consumer projects.
  - Remove `forceConsistentCasingInFileNames` since it is the default since
    TypeScript 5.0 (and this package now requires TypeScript 6+).

- f0e652a: Split base and DOM configs, and drop TypeScript 5 support.
  - The base config (`@tammergard/tsconfig`) is now environment-agnostic and no
    longer includes `dom`/`dom.iterable` in `lib` or `jsx`. Browser/React projects
    must extend `@tammergard/tsconfig/dom` instead to keep DOM types and JSX.
  - `peerDependencies.typescript` is now `"6"` only. TypeScript 5 is no longer
    supported.

## 2.10.0

### Minor Changes

- b0befe6: Allow TS 6

## 2.9.0

### Minor Changes

- 82cfc9b: Enable erasableSyntaxOnly option.

## 2.8.0

### Minor Changes

- ddd3e18: Set moduleDetection to force.

## 2.7.0

### Minor Changes

- d58a4e2: Bump target and lib to es2022.

## 2.6.0

### Minor Changes

- 402993c: Enable `noErrorTruncation`.

## 2.5.0

### Minor Changes

- 2891af8: Enable verbatimModuleSyntax.

## 2.4.1

### Patch Changes

- a92694d: Publish with provenance.

## 2.4.0

### Minor Changes

- f733fb6: Re-enable esModuleInterop.

## 2.3.0

### Minor Changes

- 02d3aa1: Disable esModuleInterop and enable allowSyntheticDefaultImports for better accuracy.

## 2.2.0

### Minor Changes

- 3a27d5f: Update usage instructions

## 2.1.0

### Minor Changes

- 9e0f907: Turn on noUncheckedIndexedAccess rule.
