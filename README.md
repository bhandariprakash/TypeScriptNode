# How to Setup a TypeScript Node.js Project ?

Step by step guide to setup the TypeScript project

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
and run `npx tsc` command in the root of the project. This will create `index.js` fine inside build folder.
