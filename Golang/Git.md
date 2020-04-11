# Git + Golang

## Using github / local package
```Go
// recommended to checkout inside GOPATH
/*
GOPATH : /home/user/go/src/

/home/user/go/src/github.com/AAA
/home/user/go/src/github.com/BBB
/home/user/go/src/yourProj

*/

// checkout your project into /home/user/go/src/yourProj/

// /home/user/go/src/yourProj/util/util.go
package util
//...

// /home/user/go/src/yourProj/main.go
package main

import (
  "github.com/AAA"
  "github.com/BBB"
  "yourProj/util"
)

//...


```
