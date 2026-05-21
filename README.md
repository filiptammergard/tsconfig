# @tammergard/tsconfig

A sharable TypeScript config with personal preferences. Requires TypeScript 6 or later.

## Installation

```bash
# npm
npm install --save-dev @tammergard/tsconfig

# pnpm
pnpm add -D @tammergard/tsconfig

# bun
bun add -d @tammergard/tsconfig
```

## Usage

The base config is environment-agnostic. For browser/React projects, extend
the DOM variant instead, which adds `lib.dom` and `jsx`.

```json
{
	"extends": "@tammergard/tsconfig"
}
```

```json
{
	"extends": "@tammergard/tsconfig/dom"
}
```

You can add additional options in your project, which will override the option
in `@tammergard/tsconfig` if it's defined there.

```json
{
	"extends": "@tammergard/tsconfig",
	"compilerOptions": {
		"outDir": "./dist",
		"paths": {
			"~/*": ["./src/*"]
		}
	}
}
```

## Enabled options

The most opinionated choices in the base config:

- `strict`
- `exactOptionalPropertyTypes`
- `noFallthroughCasesInSwitch`
- `noImplicitOverride`
- `noImplicitReturns`
- `noUncheckedIndexedAccess`
- `noUncheckedSideEffectImports`
- `erasableSyntaxOnly`
- `verbatimModuleSyntax`
- `isolatedModules`
- `moduleResolution: "bundler"`
- `module: "esnext"`
- `target: "es2022"`
- `lib: ["es2022"]`
- `noEmit`
- `skipLibCheck`
- `noErrorTruncation`

The DOM variant additionally enables `jsx: "react-jsx"` and adds `dom` and
`dom.iterable` to `lib`.

See [`tsconfig.json`](./tsconfig.json) and
[`tsconfig.dom.json`](./tsconfig.dom.json) for the full list.

## License

MIT
