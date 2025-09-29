# Syntax

Inspired by Clojure and Rust, Bereon syntax is very similar, but with some differences. 
For those with experience with languages with the LISP dialect (Clojure) and Rust, Bereon should be easy to pick up.

### Variables

```clojure
; Variables are immutable by default.
(let x: int = 10)

; Multiple variables can be declared at once
(let {
    x: int = 10
    y: bool = true
    z: string = "bereon"
})
```

### Functions

```clojure
(fn sum [x: int, y: int] { ; Multiple arguments can be passed
    (+ x y) ; The `+` is the function call.
} -> int) ; The `->` is the return type.

(sum 1 2) ; => 3
```


```clojure
; Function `even?`, returns true if the number is even, otherwise false
(fn even? [x: int] {
    (if (x % 2 == 0) {
        true
    } false ) ; Else: This `false` is not necessary. It's just for readability
} -> bool)

; If the number is even, returns "yep!", otherwise "not even!"
(if (even? x) { 
    "yep!" ; => true
} "not even!" ) ; => false

(even? 10) ; => "yep!"
```

```clojure
(fn max [x, y: int] {
    (if (x > y) {
        x
    } y )
} -> int)

(max 10 20) ; => 20
```

