#lang racket

(define atom?
  (lambda(x)
    (and (not (pair? x)) (not (null? x)))))

;
; > (+ 123 4 5 6 7)
; 145
; > (list ''a ''b ''c)
; '('a 'b 'c)

; > (define a 1)
; > a
; 1

(define a 1)
; (eval a)
; a

; cons list
; '() => the null element at the end of the list
(cons 'b (cons 'a '()))

(define myLength
  (lambda (x)
    (cond
      ((null? x) 0)
      (else (+ 1 (myLength (cdr x)))))))

; cdr - content of decrement register
; car - content of address register

;(myLength '(a b c))

(define iota
  (lambda (a  b)
    (cond
      ((= a b) (cons a '()))  ; return the list only with a
      (else (cons a (iota (+ 1 a) b))))))
; > (iota 2 6)
; '(2 3 4 5 6)

(define iota_if
  (lambda (a b)
    (if(= a b) (cons a '())
       (cons a (iota (+1 a) b)))))

; (member 2 '(1 2 3 4))
; #t

(define member
  (lambda (a l)
    (cond
      ((null? l) #f)
      ((= (car l) a) #t)
      (else (member a (cdr l))))))

(define member2
  (lambda (a l)
    (cond
      ((null? l) #f)
      (else (or (= (car l) a) (member2 a (cdr l)))))))
