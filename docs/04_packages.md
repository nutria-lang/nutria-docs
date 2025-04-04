# Packages

Nutria packages are similar to Go packages. They encapsulate and ship useful functions/classes for other Nutria programs.
All package names should be in lowercase without `-`(dashes) or special characters.

We already saw a default package called `main` in the Hello World program. To define a custom package, place your Nutria programs
into a directory and add a package name as the first line.

`converter/convert.nu`
```nu
pkg converter

import (
  enc/json
  typing as T
)

// ConvertToJson converts a given dictionary to JSON.
fun ConvertToJson(data) {
  assert data is T.Dict
  ret json.Dumps(data)
}
```

`main.nu`

```nu
pkg main

import converter as CVR

fun Main() {
  wordCount = {"pen": 3, "camera": 5}
  res = CVR.ConvertToJson(wordCount)

  Print(res) // Prints '{"pen": 3, "camera": 5}'
}
```
