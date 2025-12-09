(define (hOl x y)
    (cond 
        ((> x y) (display "Higher!"))
        ((< x y) (display "Lower!"))
        (else (display "Correct!"))))

(define (guessingGame x)
    (display "Choose a number 1-10: ")
    (newline)
    (let ((y (read)))
    (if (equal? x y)
        (begin
            (display "You got it! Number was ")
            (display x)
            (newline))
        (begin
            (hOl x y)
            (display " Try again.")
            (newline)
            (newline)
            (guessingGame x)))))
        
; Source - https://stackoverflow.com/a
; Posted by user448810, modified by community. See post 'Timeline' for change history
; Retrieved 2025-12-08, License - CC BY-SA 3.0

(define random
  (let ((a 69069) (c 1) (m (expt 2 32)) (seed (sys-time))) ;;(sys-time) will always make answer 8, trying to find a new seeding method
    (lambda new-seed
      (if (pair? new-seed)
          (set! seed (car new-seed))
          (set! seed (modulo (+ (* seed a) c) m)))
      (/ seed m))))



(display "Computer has chosen a number! It's your turn to guess!") 
(newline)
(guessingGame (+ 1 (modulo (floor (* (random) 10)) 10)))
