# TypeScript Project
> Package containing scripts and configs that HT2 Labs need for TypeScript projects.

### Usage
1. Install with `npm i -D -E @ht2-labs/typescript-project@latest`.
1. Create a "tsconfig.json" file in the root of your repository using the [example TS config](#ts-config-example).
1. Create a "tslint.json" file in the root of your repository using the [example TSLint config](#tslint-config-example).
1. Add a `lint` script to your `package.json` file using `tslint`.
1. Add a `build` script to your `package.json` file using `tsc`.
1. Add `/dist` to your `.gitignore` file.
1. Create a `src` folder in the root of your repository for all TypeScript source code.

### TS Config Example
```json
{
  "extends": "./node_modules/@ht2-labs/typescript-project/configs/tsconfig.json",
  "compilerOptions": {
    "rootDir": "src",
    "outDir": "dist",
    "typeRoots": ["./@types", "./node_modules/@types"],
  },
  "includes": ["src/**/*"],
  "exclude": ["node_modules", "dist/**/*"]
}
```

### TSLint Config Example
```json
{
  "extends": [
    "./node_modules/@ht2-labs/typescript-project/configs/tslint.json"
  ]
}
```
