# @tammergard/tsconfig

A sharable TSconfig with personal preferences.

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

Register the config in your `tsconfig.json`:

```json
{
	"extends": "@tammergard/tsconfig"
}
```

You can add additional options in your project, which will override the option
in `@tammergard/tsconfig` if it's defined there.

```json
{
	"extends": "@tammergard/tsconfig",
	"compilerOptions": {
		"strict": false,
		"baseUrl": "./src"
	}
}
```

## License

MIT
