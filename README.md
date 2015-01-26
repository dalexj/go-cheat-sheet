# Go Cheat Sheet

I hope to work my way through go, and put some syntax things here

## Quickstart

```go
package main

import "fmt"

func main() {
  fmt.Println("Hello World")
}
```

## Variables

In general: `var var_name type = value`

Shorthand: `var_name := value`

```go
var a int = 85
var b string = "hello"
c := 146
d := "world"
var e, f int = 5, 8
g, h := 4, 334
```

## Operations

```go
1 + 4             // 5
3 - 8             // -5
7 * 4             // 28
14 / 5            // 2
14.0 / 5          // 2.8
"hello" + "world" // "helloworld"
```

## Conditionals

```go
if something{
  // do stuff
} else if anotherThing{
  // do stuff
} else {
  //do stuff
}
```

## Loops

```go
for {
  // loop forever (until a break)
}
for i := 0; i < 10; i++ {
  // loop 10 times
  // i is 0-9
}
for condition {
  // loop until condition is false
}
```

## Arrays

```go
fiveInts  := []int{0, 1, 2, 3, 4} // this might be a slice, not an array
fiveZeros := [5]int
fiveInts[4] = 9
```

## Structs

```go
// Create the type struct
type Human struct {
  Name string
  Age  int
}

// Use the struct
h := Human{
  Name: "Danny",
  Age:  21,
  }
  
// Display the struct (import "fmt")
fmt.Printf("Name: %s", h.Name)
```

## Maps
Similar to hashes or dicts
```go
// Empty map: make(map[key-type]value-type)
m := map[string]int{"one": 1, "two": 2}

m["three"] = 3
m["four"] = 4

fmt.Println(m) // map[one:1, two:2, three:3, four:4]
```
