## Functions
  * infix vs prefix functions
  * functions application has the highest precedence: succ 9 * 10 == 100
  * prefix infix equivalent: div 92 10 == 92 `div` 10
  * space denotes function application
  *   Why couldn't we wrote doubleMe in ghci itself?
  * Function names can include apostrophes (but can begin with one)
  *   Nor can they start with a capital letter
  *   Underscores are cool anywhere, hyphens aren't
  *   function with no parametrs = definition/name
  * Single quote can only be used for single character

## Lists
  * Double quotes are syntatic sugar for list of characters: ['h','e','l','l','o'] == "hello" # => True
  * (+) 3 3 == 3 + 3
  * syntactic sugar: 1:2:3:[] == [1,2,3]
  * concat lists: l1 ++ l2
  * return the Nth element L !! n
  * How do you create an empty string? Is it []?
  * list operations: head, last, init, tail (blows up on empty lists)
  * more list operations: length, null (boolean), reverse, take(n), drop(n), maximum, minimum, sum, product
  * "take n" returns the first n elements while `drop n` returns the nth element to the `length list`
  * ```4 \`elem\` [4]``` <=> `elem 4 [4]`

## Ranges
  * Unlike ruby, haskell can't enumerate strings of length longer than 1.
  * Ranges are inclusive [1..20]
  * Ranges with steps: [3, 6..20] == [3,6,9,12,15,18]
  * Step-down ranges first two elements must be specified: [20, 19..1]
  * Don't use floating point in ranges

## Infinite lists functions
  * cycle [1,2,3] # => [1,2,3,1,2,3,1,2,3,...]
  * repeat 8      # => [8,8,8,...]
  * Generate list of size 5 whose elements are all 8: `take 5 (repeat 8)`
  * Or: `replicate 5 8`

## List Comprehensions
  * The input function comes after the pipe
  * Predicates are separated with commas from the input function and from each other
  * mod is the modulus function
  * odd return true for odd numbers and false for even numbers
  * /= is the 'not equal' function (e.g `1 /= 0 #=> True`)
  * Wow! List comprehensions can draw from multiple lists.
  * If no limitations apply, the iteration/drawing starts from the left-most input function (see the triangle example).

## Tuples
  * Differences form lists: fixed size, can be non-homogenous.
  * A Tuple type is inferred by its size and the types of its elements.
  * No singletone tuples.
  * fst and snd works only on pairs.
  * zip combines two lists into a list of pairs.
  * zip's output list takes the length of the shorter list.
