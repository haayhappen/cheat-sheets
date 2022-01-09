## Typescript
Typescript is a superset of javascript. It's power lays within its scalability and tooling capabilities.

Install   
```npm install typescript```

Run typescript compiler   
```npx tsc (--noEmit --watch)```

### Config:
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

### Types
Types are the banner feature of TypeScript. The TS compiler determines a type for every value (variable, function argument, return value, etc.) in a program, and it uses these types for a range of features, from indicating when a function is being called with the wrong input to enabling an IDE to auto-complete a class property name.

Without additional type hints, all variables in TypeScript have the any type, meaning they are allowed to contain any type of data, just like a JavaScript variable. The basic syntax for adding type constraints to code in TypeScript looks like this:
```ts
function toNumber(numberString: string): number {
  const num: number = parseFloat(numberString);
  return num;
}
```

The primitive types that TypeScript provides match the primitive types of JavaScript itself: any, number, string, boolean. TypeScript also has void (for null or undefined function return values), never, and as of TypeScript 3.0, unknown.

*unknown* is the type-safe counterpart of *any*; anything can be assigned to an *unknown* variable, but an unknown value can’t be assigned to anything other than an *any* variable without a type assertion or type narrowing.


