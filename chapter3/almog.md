# Believe the type
  * `:t value` _prints_ out the value''s type (is it a ghci function?)
  * The type String is synonymous with String
  * Type declaration of function that takes 3 integers and output one character, looks like this:
    `intsToChar :: Int->Int->Int->Char`
  * Commont types:
    - Int - bound signed integer (usually 32 bit)
    - Integer - unbound integer.
    - Float (single precision real Float)
    - Double (doubl precision real Float)
    - Bool
    - Character
    - () - The empty tuple

# Type variables
  * Polymorphic Functions - functions that take Type Variables.
    For example:  `:t head`.
  * It is a convention to use a single character for type variables.

# Typeclasses 101
  *  When printing a type with `:t` - everything before the => symbol is called a class constraint
  This constraint is enforced on the types (type variables?) that follow it
