---
title: Go
---

## Syntax cheatsheet

```go
package main

import(
        "fmt"
)

func main() {
        fmt.Println("hello world")
}
```

## Cross-compilation
```bash
# Compile for AMD64 Linux
GOOS=linux GOARCH=amd64 go build
```

[https://golang.org/doc/install/source#environment](List of compilation targets)

## Resources

* <https://golang.org/>
* [Language Specification](https://golang.org/ref/spec)

## Looking into

* https://www.kablamo.com.au/blog-1/2018/12/10/just-tell-me-how-to-use-go-modules
* https://cryptic.io/go-http/
* https://medium.com/@nate510/don-t-use-go-s-default-http-client-4804cb19f779