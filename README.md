# How to Setup a TypeScript Node.js Project ?

Step by step guide to setup the TypeScript project. 

## Getting Started

### Prequisites

* Node and npm should be pre installed in your machine
* You should be familiar with Node and the npm ecosystem
* You should have a code editor installed (VS code)


### Initial Setupe

``` 
mkdir test-project
cd test
npm init -y
```
### Install TypeScript
```
npm install typescript --save-dev
```
### npm install typescript --save-dev
```
npm install @types/node --save-dev
```

###  Create a `tsconfig.json`
```
npx tsc --init --rootDir src --outDir build \
--esModuleInterop --resolveJsonModule --lib es6 \
--module commonjs --allowJs true --noImplicitAny true
```
### We're set to run our first TypeScript file.

```
mkdir src
touch src/index.ts
```


#### write some code.

```
console.log("I am running ....");
```
and run `npx tsc` command in the root of the project. This will create `index.js` file inside build folder.

### ts-node nodemon (Cold Reloading)
Install `ts-node nodemon` package  as dev. depandancy. 

```
npm install --save-dev ts-node nodemon
```

Also, create `nodemon.json` confing file in root of the project.

```
{
    "watch": ["src"],
    "ext": ".ts,.js",
    "ignore": [],
    "exec": "ts-node ./src/index.ts"
}
```

Add `"start:dev": "nodemon"` in `package.json` file in script to run and test in dev. env.

Now, you can run `npm run start:dev`  command.

### Production Ready
Finally, you can add `"start": "npm run build && node build/index.js"` line in `package.json`, So, that you can build and run your project by `npm run start` command