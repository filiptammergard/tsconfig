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
pnpm install @tammergard/tsconfig --dev
```

## Usage

Register the config in your `tsconfig.json`:

```json
{
	"extends": "@tammergard/tsconfig/tsconfig.json"
}
```

You can add additional options in your project, which will override the option
in `@tammergard/tsconfig` if it's defined there.

```json
{
	"extends": "@tammergard/tsconfig/tsconfig.json",
	"compilerOptions": {
		"strict": false,
		"baseUrl": "./src"
	}
}
```

## License

MIT
