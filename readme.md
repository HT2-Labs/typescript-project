# TypeScript Project
> Package containing scripts and configs that Learning Pool need for TypeScript projects.

### Usage
1. Install with `npm i -DE @ht2-labs/typescript-project@latest`.
1. Create a "tsconfig.json" file in the root of your repository using the [example TS config](#ts-config-example).
1. Add a `eslintConfig` property in your `package.json` file using the [example ESLint config](#eslint-config-example).
1. Add a `lint` script to your `package.json` file using `eslint`.
1. Add a `build` script to your `package.json` file using `tsc`.
1. Add `dist` to your `.gitignore` file.
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
  "include": ["src/**/*"],
  "exclude": ["node_modules", "dist/**/*"]
}
```

### ESLint Config Example
```json
{
  "extends": [
    "@ht2-labs/typescript-project/eslint"
  ]
}
```
