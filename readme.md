# TypeScript Project
> Package containing scripts and configs that HT2 Labs need for TypeScript projects.

### Usage
1. Install with `npm i -D @ht2-labs/typescript-project`.
1. Create a "tsconfig.json" file in the root of your repository using the [example TS config](#ts-config-example).
1. Create a "tslint.json" file in the root of your repository using the [example TSLint config](#tslint-config-example).
1. Add a `lint` script to your `package.json` file using `node ./node_modules/tslint/bin/tslint`.
1. Add a `build` script to your `package.json` file using `node ./node_modules/typescript/bin/tsc`.

### TS Config Example
```json
{
  "extends": "./node_modules/@ht2-labs/typescript-project/configs/tsconfig.json",
  "compilerOptions": {
    "target": "es5",
    "rootDir": "src",
    "outDir": "dist",
    "lib": ["es2015", "es2016", "dom"],
    "typeRoots": ["./@types", "./node_modules/@types"],
    "sourceMap": true,
    "declaration": true,
    "noUnusedLocals": false
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
