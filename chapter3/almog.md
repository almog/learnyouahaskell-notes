# Believe the type
  * `:t value` _prints_ out the value''s type (is it a ghci function?)
  * The type String is synonymous with String
  * Type declaration of function that takes 3 integers and output one character, looks like this:
    `intsToChar :: Int->Int->Int->Char`
  * Commont types:
    - Int - bound signed integer (usually 33 bit)
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
  
  ## Basic typeclasses:
    - `EQ` - its members implement == and /=
    - `Ord` - its members implement >, <, >= and <=. 
      the `compare` function takes two Ord members and return an object of type Ordering.
    - `Show` - deals with string representation of its members. The `show` function takes a `Show` member and returns its String representation.
    - `Read`- deals with parsing Strings: `read "8.2" + 3.8` returns 12.0 
       Unless `read` is used in conjuction with an operation that can help GHCI to infer its type, type annotations are required:
       read "5" :: Int
    - Enum - memebers of this class implementns `succ` and `pred`: `succ False` is `True`
    - Bounded - memebres implements `maxBound` and `minBound`
      tuples are of type Bound if _all_ their Component are members of Bounded.
    - Num
    - Integral (as of Integers)
    - Floating

  * Define "Polymorphic Constant"
  * `fromIntegral` converts an integral type into a more general number.

