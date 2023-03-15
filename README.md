# calculator2

## init package and git

```console
git init
npm init -y
```

## add ts as dev dependency

```console
npm install --save-dev typescript
```

Add tsconfig.json to compile Typescript
```json
{
  "compilerOptions": {
    "target": "es5",
    "module": "commonjs",
    "declaration": true,
    "outDir": "./lib",
    "strict": true
  },
  "include": ["src"],
  "exclude": ["node_modules", "**/__tests__/*"]
}
```
Add a build script to package.json
```json
"build" : "tsc"
```

## code

Create a src folder in the root and add index.ts file.


## .gitignore
```
node_modules
/lib
```

## include only build files in the package
Add the files property in package.json
```json
"files": ["lib/**/*"]
```

## Prepare to publish
Add prepare script to package.json. It will run before package is packed and published.
```json
"prepare" : "npm run build"
```

## publish
```npm publish```
