# Hello world

Like starting every programming language, let's write a simple Hello World program in Nutria. A Nutria program is a UTF-8 text file
with extension `.nu`

`hello.nu`
```nu
pkg main

fun Main() {
  Print("Hellow World")
}
```

That's it. Isn't it easy!


Every Nutria program (hello.nu) should be in a package. For the hello world program, program's package is specified with `pkg` keyword and value `main`. Every Nutria program/s should have a single Main function in `main` package
from where the execution starts.

In `hello.nu`, a function called `Main` is defined with a keyword: `fun`.

A sharp-eye catches something in this tiny program. 'M' in `Main()` is a capital letter. Same for 'P' in `Print`. There is a reason for that.

In Nutria, all symbols exported from a package to another package should begin with a Capital letter. This similarity comes from Go and gives a clear indication whether
a symbol is local or imported.

But wait, where did we import `Print` ?

The `Print` function is by default imported from `builtin` package. So, a programmar doesn't have to re-import it again.

## Running the program

A Nutria program can be run with `nutria` command like this:

```sh
// Prints 'Hello World' to console
nutria hello.nu
```
