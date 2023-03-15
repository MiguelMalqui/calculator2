# calculator2

## init package and git

```git init```
```npm init -y```

## add ts as dev dependency

```npm install --save-dev typescript```

```
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

## code

Create a src folder in the root and add index.ts file.
Add a build script to package.json

## .gitignore
```
node_modules
/lib
```

## include only build files in the package
Add the files property in package.json
```"files": ["lib/**/*"]```

## add prepare script
prepare will run before package is packed and published. Add to package.json
```"prepare" : "npm run build"```

## publish
```npm publish```
