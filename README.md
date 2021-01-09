# How to create a React Typescript SPA

Minimum setup, steps required to build React Typescript Single Page app with webpack

Step by step

- Initialise a new project `npm init -y`
- create folder src `mkdir src`
- install webpack `npm i -D webpack webpack-cli`
- install typescript `npm i -D typescript`
- initialise typescript `tsc --init`

configure tsconfig.json to be like this:
```json
{
  "compilerOptions": {
    "target": "ES2020",                       /* Specify ECMAScript target version: 'ES3' (default), 'ES5', 'ES2015', 'ES2016', 'ES2017', 'ES2018', 'ES2019', 'ES2020', or 'ESNEXT'. */
    "module": "commonjs",                     /* Specify module code generation: 'none', 'commonjs', 'amd', 'system', 'umd', 'es2015', 'es2020', or 'ESNext'. */
    "strict": true,                           /* Enable all strict type-checking options. */
    "esModuleInterop": true,                  /* Enables emit interoperability between CommonJS and ES Modules via creation of namespace objects for all imports. Implies 'allowSyntheticDefaultImports'. */
    "skipLibCheck": true                     /* Skip type checking of declaration files. */
  }
}
```

Typescript will only be used by @babel/preset-typescript to js code from ts code to the latest ES2020 format, actual transpilation to browser compatible formats will be done by @babel/preset-env and babel-loader and webpack

- install babel dependencies

