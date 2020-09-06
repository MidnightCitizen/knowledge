### Keys Comments

* TypeScript's if for development only (compilation).
* Javascript uses "dynamic types" (resolved at runtime), TypeScript uses "static types" (set during development). 

### Core Types 
* number 
* string 
* boolean
* object
* array
* tuple (array fixed-length)
* enum (enum Role { ADMIN, READ_ONLY, AUTHOR})
* any (to avoid most of the time)
* union (string | number)
* literal  (set specific values, example : 'option1' | 'option2')
* custom type (example: `type Combinaison = number | string`, or complex object)
* Function (example : `let iAmAFunction: (a:number, b:number) => number`)
* unknown (kind of similar to any)
* never (return nothing, not even undefined, return nada)

## Type Casing

TypeScript work with types like **string** or **number**, all lowercase

## Type Inference
When you declare a variable, or have a function with two specific types, you don't need to set a specific type : TypeScript understands already which type will be used or returned


## References

[Official Doc - Basic Types](https://www.typescriptlang.org/docs/handbook/basic-types.html)