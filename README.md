# jc
a language in the works 



## Language features, syntax, ideation
1. purely immutable by default, any side effect code is considered unsafe
2. functional by default
3. opt in laziness
4. no access to memory management (probably garbage collected but maybe some other way...)
5. no objects
6. pattern matching
7. compiles to WASM
8. type inferencing
9. simple syntax
10. currying
11. algebraic types
12. no `==` just `=`
13. strong typing obviously
14. fast compile time
15. modules
16. no accessable pointers
17. everything should be pass by value (or lazy)
18. natural numbers by default
19. optionals
20. (),[],{} are equivalent


### syntax
```
// assignment
set x 5
set <name> <value>
// type hinting
set x 5 ? nat

// functions
// type decorated
op sum : (num1 num2 ? nat) ? num {
  num1 + num2
}

// type infered
op sum : num1 num2 {
  num1 + num2
}

// if equivalent
if x = 5
then put | "5"
else put | "not 5"

// recursive function
rec sum : (num1 ? nat) ? nat {
  fib | num1 
}

// matching
op match_list : lst ? [nat] {
  lst...
  ? head::rest -> put | "first case"
  ? [] where 5 = 5 -> put | "second case"
  ? _ -> put | "match anything else"
}
```
