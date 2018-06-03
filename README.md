# mylisp

Lisp interpreter written in Clojure, mainly as an exercise to experiment with `clojure.spec` features for conforming and destructuring S-expressions.

## Goals

The main goals of this LISP interpreter implementation is to support evaluation of S-expressions of untyped lambda calculus:

* evaluation robust enough, so that Y-Combinator works
* support for basic LISP macro system (dirty, non-hiegenic)

## Usage

Run the REPL by executing `lein run` in the project root directory.

While in the REPL try executing the following expressions:

    (+ 1 2 3)
    ;; => 6

    (defun square (x) (* x x))
    ;; => square

    (square 5)
    ;; = > 25

    (let (x (+ 2 3)) (square x))
    ;; => 25

    (defun fact (n) (if (= n 0) 1 (* n (fact (- n 1)))))
	;; => fact

    (fact 0)
	;; => 1

    (fact 5)
	;; => 120

## License

Copyright © 2014 Daniel Dinnyes

Distributed under the Eclipse Public License either version 1.0 or any later version.
