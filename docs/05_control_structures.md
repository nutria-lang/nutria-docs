# Control structures

Nutria comes with popular control structures to provide programmatic step-through of statements to do something meaningful.

These control structures are inspired from many languages appeared before. They are easy to remember, with simple and clear meaning.

## if

If condition is a basic programming construct to either accept or skip a set of program statements. You use `if` keyword in a statement like below:

```nu
pkg main

fun Main() {
  age = 50

  if age > 18 {
    Print("You are an adult!") // Prints this
  }
}
```

## else

If a given condition is a binary for building a construct, like either this or everything else, you use `else` keyword.

```nu
pkg main

fun Main() {
  age = 10

  if age > 18 {
    Print("You are an adult!")
  } else {
    Print("You are a kid!") // Prints this
  }
}
```

## elseif

If you have to check multiple conditions to make a decision programatically, you can use `elseif` keyword.

```nu
pkg main

fun Main() {
  age = 20

  if age < 2 {
    Print("You are a baby!")
  } elseif age >= 2 && age < 18 {
    Print("You are a kid!")
  } else {
    Print("You are an adult!") // Prints this
  }
}
```

`&&` here is a logical and operator that checks truthness of Left-hand side and Right-hand side of condition.
