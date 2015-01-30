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

In general: `var varName type = value`

Shorthand: `varName := value`

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

## Switches

```go
// import "time"
t := time.Now()
switch {
case t.Hour() < 10:
  fmt.Println("Breakfast Time")
case t.Hour() > 10, t.Hour() < 12:
  fmt.Println("Second Breakfast Time")
default:
  fmt.Println("Inferior Time")
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

## Ranges

```go
// Iterating over slices
nums := []int{1, 2, 3}
for i, num := range nums {
  if num == 2 {
    fmt.Println("Index:", i) // Index: 1
  }
}

// Use an underscore to tell the Go compiler you don't intend to use a variable.
nums := []int{1, 2, 3}
for _, num := range nums {
  fmt.Println(num)
}

// Iterating over maps
kvs := map[string]string{"Danny":"Awesome", "Alex":"Okay"}
for k, v := range kvs {
  fmt.Printf("%s is %s\n", k, v) // Danny is Awesome /n Alex is Okay
}
```

## Arrays

```go
// Arrays are fixed in length
fiveZeros := [5]int
fiveInts[4] = 9
```

## Slices

```go
// Same as an array but flexible in length
fiveInts  := []int{0, 1, 2, 3, 4}
fiveInts[:2] // [0,1]
fiveInts[:]  // [0,1,2,3,4]
fiveInts[2:] // [2,3,4]
```

## Structs

On struct creation, the multiline format requires a `,` at the end of the line

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
h2 := Human{ Name: "Alex", Age: 16 }

// Display the struct (import "fmt")
fmt.Printf("Name: %s", h.Name)
```
