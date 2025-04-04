# Looping structures

Looping is an essential element in programming. Programs loop through a set of instructions for finite/infinite amount of time.
Those looped over statements are mostly for accesing data from a datastructure or building a new datastructure.

Nutria provides a `for` loop to range over a given number range or anyone of list/set/dict types.

## for

Let us loop from 1 to 10 and print the numbers.

### Loop over range

```nu
pkg main

fun Main() {
  for i := 1..10 { // Prints 1 2 3...10
    Print(i, " ")
  }
}
```

To reverse the pattern, just reverse the range:

```nu
for i := 10..1 { // Prints 10 9 8 7...1
  Print(i, " ")
}
```

The `..` symbol is a range-between symbol for natural numbers. `:=` symbol assigns a given element everytine the loop iterates.

### Loop over data types

To loop over a list and read elements, you can use list as range after `:=` symbol.
```nu
/* Prints
0 96
1 67
...
3 55
*/

scores = [96, 67, 29, 54, 55]
for i, s := scores {
  Println(i, " ", s)
}
```

Here iteration step collects an Index and Element from a given list.

If you are not using `i`, you can leave it blank (`_`) identifier for readability.
```nu
for _, s := scores {
  Println(s)
}
```

## for with step

Sometimes you need to step over multiple elements while looping. This is possible by adding a second `..` after range-between.

For ex: To print all even numbers between 1 to 100,

```nu
pkg main

fun Main() {
  for i := 2..100..2 { // Prints 2 4 6...100
    Print(i, " ")
  }
}
```

`2..100..2` specifies loop from 2 until 100 but step two items everytime. 2 + 2 = 4, 4 + 2 = 6 etc till the end number (100) is reached.
