# #연습문제 #
|[1.1](SICPChOne#1.1.md)|[1.2](SICPChOne#1.2.md)|[1.3](SICPChOne#1.3.md)|[1.4](SICPChOne#1.4.md)|[1.5](SICPChOne#1.5.md)|[1.6](SICPChOne#1.6.md)|[1.7](SICPChOne#1.7.md)|[1.8](SICPChOne#1.8.md)|1.9|1.10|
|:----------------------|:----------------------|:----------------------|:----------------------|:----------------------|:----------------------|:----------------------|:----------------------|:--|:---|
|1.11|1.12|1.13|1.14|1.15|1.16|1.17|1.18|1.19|1.20|

[sqrt-iter](SICPChOne#sqrt-iter.md)(1.1.7)


#### 1.1 ####
```
10
(+ 5 3 4)
(- 9 1)
(/ 6 2)
(+ (* 2 4) (- 4 6))
(define a 3)
(define b (+ a 1))
(+ a b (* a b))
(= a b)
(if (and (> b a) (< b (* a b)))
    b
    a)
(cond ((= a 4) 6)
      ((= b 4) (+ 6 7 a))
      (else 25))
(+ 2 (if (> b a) b a))
(* (cond ((> a b) a)
         ((< a b) b)
         (else -1))
   (+ a 1))
```

#### 1.2 ####
```
(/ (+ 5 4 (- 2 (- 3 (+ 6 (/ 4 3)))))
   (* 3 (- 6 2) (- 2 7)))
```

#### 1.3 ####
```
(define (square x) (* x x))

(define (sum-of-squares a b)
  (+ (square a) (square b)))

(define (larger-sum a b c)
  (cond ((and (> a b) (> b c)) (sum-of-squares a b))
        ((and (> a b) (> c b)) (sum-of-squares a c))
        (else (sum-of-squares b c))))
```

#### 1.4 ####
operator is compound expression.
```
(define (a-plus-abs-b a b)
  ((if (> b 0) + -) a b))

(a-plus-abs-b 3 -4)
```

#### 1.5 ####
normal order vs applicative order
```
(define (p) (p))

(define (test x y)
  (if (= x 0)
      0
      y))

(test 0 (p))
```

#### sqrt-iter ####
```lisp

(define (sqrt-iter guess x)
(if (good-enough? guess x)
guess
(sqrt-iter (improve guess x)
x)))

(define (improve guess x)
(average guess (/ x guess)))

(define (average x y)
(/ (+ x y) 2))

(define (good-enough? guess x)
(< (abs (- (square guess) x)) 0.001))

(define (sqrt x)
(sqrt-iter 1.0 x))

(sqrt 9)
(sqrt (+ 100 37))
(sqrt (+ (sqrt 2) (sqrt 3)))
(square (sqrt 1000))
```

using black box abstraction
```scheme

(define (sqrt x)
(define (good-enough? guess x)
(< (abs (- (square guess) x)) 0.001))
(define (improve guess x)
(average guess (/ x guess)))
(define (sqrt-iter guess x)
(if (good-enough? guess x)
guess
(sqrt-iter (improve guess x) x)))
(sqrt-iter 1.0 x))
```

#### 1.6 ####
```
(define (new-if predicate then-clause else-clause)
  (cond (predicate then-clause)
        (else else-clause)))

(new-if (= 2 3) 0 5)

(new-if (= 1 1) 0 5)

(define (sqrt-iter guess x)
  (new-if (good-enough? guess x)
          guess
          (sqrt-iter (improve guess x)
                     x)))

(sqrt 3)
```
왜 new-if를 쓰면 값이 안구해질까?

applicative order

#### 1.7 ####
```lisp

(define (square x) (* x x))
(define (average a b) (/ (+ a b) 2))

(define (sqrt x)
(define (good-enough? guess new-guess)
(< (abs (- new-guess guess)) 0.001))
(define (improve guess x)
(average guess (/ x guess)))
(define (sqrt-iter guess new-guess)
(if (good-enough? guess new-guess)
new-guess
(sqrt-iter new-guess (improve new-guess x))))
(sqrt-iter 1.0 x))


(sqrt 3.0)
(sqrt 0.0005)
```

#### 1.8 ####
```lisp


(define (square x) (* x x))

(define (cbrt x)
(define (good-enough? guess new-guess)
(< (abs (- new-guess guess)) 0.001))
(define (improve guess x)
(/ (+ (/ x (square guess)) (* 2 guess)) 3))
(define (cbrt-iter guess new-guess)
(if (good-enough? guess new-guess)
new-guess
(cbrt-iter new-guess (improve new-guess x))))
(cbrt-iter 1.0 x))

(cbrt 27.0)
(cbrt 1000.0)




```