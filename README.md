# @tammergard/tsconfig

[![npm version](https://img.shields.io/npm/v/@tammergard/tsconfig.svg)](https://www.npmjs.com/package/@tammergard/tsconfig)

A sharable TSconfig with personal preferences.

## Requirements

TypeScript 6 or later.

## Installation

Install this package as a dev dependency.

```bash
# npm
npm install @tammergard/tsconfig --save-dev

# yarn
yarn add @tammergard/tsconfig --dev

# pnpm
pnpm add @tammergard/tsconfig --save-dev
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
- `noUncheckedIndexedAccess`
- `erasableSyntaxOnly`
- `verbatimModuleSyntax`
- `isolatedModules`
- `forceConsistentCasingInFileNames`
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
