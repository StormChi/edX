# Expressions
``` lisp
(+ 3 4)
(+ 3 (* 2 3))
(/ 12 (* 2 3))
(sqr 3)
(sqrt 16)
(sqrt (+ (sqr 3) (sqr 4)))
```
# Strings and Images
```lisp
"apple"
(string-append "Ada" " " "Lovelace")
(string-length "apple")
(substring "Caribou" 2 4)   ; "ri"
(substring "Caribou" 0 3)   ; "Car"
```
## Image
```lisp
(require 2htdp/image)
(circle 10 "solid" "red")
(rectangle 30 60 "outline" "blue")
(text "hello" 24 "orange")

(above (circle 10 "solid" "red")
       (circle 20 "solid" "yellow")
       (circle 30 "solid" "green"))

(beside (circle 10 "solid" "red")
       (circle 20 "solid" "yellow")
       (circle 30 "solid" "green"))

(overlay (circle 10 "solid" "red")
       (circle 20 "solid" "yellow")
       (circle 30 "solid" "green"))

# Constant Definitions
``` lisp
(require  2htdp/image)

(define WIDTH 400)
(difine HEIGHT 600)

(* WIDTH HEIGHT)

(* 400 HEIGHT)

(* 400 600)


(define CAT XXX)    ; XXX is a cat pircure, just copy and paste from other material

(define RCAT (rotate -10 CAT))
(define LCAT (rotate 10 CAT))
```
# Function Definitons
``` lisp
(require 2htdp/image)

(above (circle 40 "solid" "red")
       (circle 40 "solid" "yellow")
       (circle 40 "solid" "green"))

(define (bulb c)
  (circle 40 "solid" c))

(above (bulb "red") 
       (bulb "yellow") 
       (bulb "green"))
```
``` lisp
(require 2htdp/image)

(define (bulb c)
  (circle 40 "solid" c))

(bulb (string-append "re" "d"))
(bulb "red")
(circle 40 "solid" "red")
```
# Booleans and if Expressions 
``` lisp
(require 2htdp/image)
;true
;false

(define WIDTH 100)
(define HEIGHT 100)

(> WIDTH HEIGHT)
(>= WIDTH HEIGHT)

(= 1 2)
(= 1 1)
(> 3 9)

(string=? "foo" "bar")

(define I1 (rectangle 10 20 "solid" "red"))
(define I2 (rectangle 20 10 "solid" "blue"))

(< (image-width I1)
   (image-width I2))

(if (< (image-width I1)
       (image-height I1))
    "tall"
    "wide")

(and (> (image-height I1) (image-height I2))
     (< (image-width I1) (image-width I2)))
```

