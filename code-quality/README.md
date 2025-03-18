# Quality Assurance
This directory contains configurations and tools to ensure code quality in your projects.

## Code Quality

### [Biome(Ultracite)](https://biomejs.dev/guides/getting-started/)
**Biome** is a fast formatter for JavaScript, TypeScript, JSX, TSX, JSON, CSS and GraphQL that scores 97% compatibility with Prettier, saving CI and developer time. It's perfect to use in your project like React, Next.js and Solid.js
**Ultracite** is a robust linting configuration for modern TypeScript apps, built on Biome. It is incredibly opinionated and strict, enforcing the maximum amount of type safety and code quality.

#### Installation
`bun add --dev --exact @biomejs/biome`

#### Initialization
`bunx biome init`
or
`bunx ultracite init`
this will create `biome.json`
replace it with `./configs/biome.json`


#### useful resources
- [Migrate from ESLint and Prettier](https://biomejs.dev/guides/migrate-eslint-prettier/) 
	```
	biome migrate eslint --write
	biome migrate prettier --write
	```
- [Rules](https://biomejs.dev/linter/rules/)
- [Reporter](https://biomejs.dev/reference/reporters/)
- [VCS (Version Control System) integration]()
- [IDE Extension](https://biomejs.dev/guides/editors/first-party-extensions/)
- [Githook](https://biomejs.dev/recipes/git-hooks/)
- [CI](https://biomejs.dev/recipes/continuous-integration/)
---
**scripts (Don't forget to remove comments. it's for instruction purpose)**
```
{
	...
	"format:check": "bunx biome format", // check format
	"format:fix": "bunx biome format --write", // apply safe fix for format
	"lint:check": "bunx biome lint", // check lint
	"lint:fix": "bunx biome lint --write", // apply safe fix for lint
	"biome:fix": "bunx biome check --write",
	"biome:report": "biome check --reporter=summary"
	...
}
```
---

### [Million](https://million.dev/)
>Million Lint is a VSCode extension that speeds up your website!
>Your React app is slow. Million Lint surfaces problematic code and automatically suggests ways to improve it.
>Million Lint works with any React app (Next.js, Vite, Webpack, etc.) – get started in minutes!

⚠️ as of 13/3/2025 turbopack local dev doesn't work with million

- **installation**
  `bunx million@latest`

---

### [React Scan](https://github.com/aidenybai/react-scan#readme)
>automatically detects performance issues in your React app.
- **installation**
  ```
	# to check your local app
	npx react-scan@0.0.36 http://localhost:3000		
	```
	or via cdn
	```
	<script src="https://unpkg.com/react-scan/dist/auto.global.js"></script>
	```
	example script to use react-scan in your next.js app
	```
	"scan": "next dev & npx react-scan@latest localhost:3000"
	```

---

### `ts.config.json`



---

### [CSpell](https://cspell.org/)

- **File**: `cspell.yaml`

---

### [Lefthook](https://lefthook.dev/intro.html)
- **File**: `lefthook.yml`
Disable lefthook in CI

#### useful resources
- [examples](https://lefthook.dev/examples/index.html)
- [Tips](https://lefthook.dev/usage/tips.html)

##### Tips
When using NPM package lefthook set CI=true in your CI (if it does not set automatically). When CI=true is set lefthook NPM package won't install the hooks in the postinstall script.

---



---

## Commit messages
### [git-cz]()
### [Commitlint](https://commitlint.js.org/)
