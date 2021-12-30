## Typescript
Typescript is a superset of javascript. It's power lays within its scalability and tooling capabilities.

Install   
```npm install typescript```

Run typescript compiler   
```npx tsc (--noEmit --watch)```

Example config:
```
{
  "compilerOptions": {
    "jsx": "vue",
    "jsxFactory": "tsx",
    "types": [ "intern" ],
    "lib": [
      "dom",
      "es5",
      "es2015.core",
      "es2015.iterable",
      "es2015.promise",
      "es2015.symbol",
      "es2015.symbol.wellknown",
      "es2015.proxy"
    ]
  },
  "include": [
    "./src/**/*.ts",
    "./src/**/*.tsx",
    "./tests/**/*.ts",
    "./tests/**/*.tsx"
  ]
}
```

Usually, a tsconfig.js is created within a project to configure the typescript compiler. 
The lib config property allows specific type subsets to be enabled to tailor the compiler’s output for a particular environment. For example, if a project will be running in a legacy environment that’s known to have a polyfill for  Array.prototype.include, then “es2016.array.include” could be added to the lib property to let the compiler know that this method (but not other ES2016 library methods) will be available. If code will be running in a browser, then “dom” should be added to lib to tell the compiler that global DOM resources will be available.
