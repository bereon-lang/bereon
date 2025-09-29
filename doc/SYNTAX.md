# Syntax

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

(println (even? 10)) ; => "yep!"
```