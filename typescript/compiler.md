# The TypeScript Compiler

1. Simple Compilation   
`
tsc app.js
`

2. Watch Mode    
`
tsc app.js -w
`

3. Compile Entire Project   
`
tsc --init
tsc -w
`
## Exclude files from compilation

Add to tscionfig.json, in the end, before the last bracket :
`
"exclude": [
    "node_modules",
    "fileNameToExcluse.ts"
]
`

## Notes

[[typescript]]
