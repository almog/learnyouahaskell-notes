## Pattern Matching
  * If a pattern matching inside a list comprehension input function fail, it will move to the next element.
  * x:xs as an idiom for (give me the first element and 
  * Parentheses must be used when binding more than one variable.
  * Matching a singleton list can take either of these two forms: `x:[]` or `[x]`.
  * "as patterns" - a way to keep a reference to the thing we're patterning: `xs@(x:y:ys)`.
  * Impossible to use `++` in patterns due to the ambiguity nature it carries.

## Guards
  * If all guards evaluate to `False`, evaluation falls to the next _pattern_
  * When using guards, the function `=` sign is placed right after the guard test expression.
  * Guard's `else` is called `otherwise`.
  * If you see function with all too many pipes, they probably are guards.
  * It's possible to define functions in an infix fashion (use backticks!).
  * After the guards, comes the optional `where` binding, a way to indirect expressions by giving them names (must be aligned in one column)
  * Where binding can define expressions that are pattern matched to others.
  * Where can contain furnctions definitions as well.
## Let it be
  * Let are expressions. They take the form let `<binding> in <expression>`
  * Multiple binding in a single inline binding expression are separated with semicolons.
  * It's possible to pattern match let bindings to a tuple of matching values.
  * They can be introduced in a list comprehensions, like predicates only that no filtering is occurring (unless you apply a predicate on the let expression, which you can do).
  * let expressions can't be used _across_ `where` bindings.
