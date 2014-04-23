#Aufgabenblatt 14 - Daniel Norman
-------

*The notation for Aufwand is as follows: `A-OPERATION` e.g. for addition `A-+`*

### Aufgabe 1.3

 1. bulding the polynom
        A-exp(n) = A-=, A-=, A-even + A-odd + 
                    max(A-/ + A-exp(n/2) + A-*,
                        A-- + A-/ + A-exp((n-1)/2) + 2*A-*)
        A-exp(n) = 2*A-= + A-even + A-odd + A-- + A-/ + A-exp((n-1)/2) + 2*A-*
        A-exp(n) = 2*const-equality + const-even + const-odd + const-subtraction + const-division + A-exp(x,(n-1)/2) + 2 * const-multiplication
        
        A-exp(n) = const-all + A-exp((n-1)/2)
 
 2. matching the variables 
        b = const
        c = 1
        k = 0
    
 3. `A-exp e O(log n)`

***

### Aufgabe 3.2
* ####Best-case
    1. bulding the polynom
            A-qsort(n) 
               = n*A-< + A-qsort(lesser) + A-++ + A-qsort(greaterEq)
               = n*const-< + const-++ + A-qsort(lesser) + A-qsort(greaterEq)
               = n*const-< + const-++ + 2A-qsort((n-1)/2) 
               = n + const-all + 2A-qsort((n-1)/2)
        **NOTE  A-qsort(lesser) + A-qsort(greaterEq) ~ 2A-qsort((n-1)/2)**
               
    2. matching variables
            c = 2
            b = 1
            k = 1
    3. matching polynom in the complexity table

        `O( n^k * log(n) ) 
        = O( n log(n) )`


* ####Worst-case (when the list is already ordered)
    1. bulding the polynom
            A-qsort(n) = n*A-< + A-qsort(lesser) + A-++ + A-qsort(greaterEq)
                       = n*const-< + const-++ + A-qsort(lesser) + A-qsort(greaterEq)
                       = n*const-< + const-++ + A-qsort(n-1)  
                       = n + const-all + A-qsort(n-1)
        **NOTE: A-qsort(lesser) is empty and A-qsort(greaterEq) = A-qsort(n-1)         **
    2. matching variables
            c = 1
            b = 1
            k = 1
    3. matching polynom in the complexity table

        `O( n^(k+1) ) =
        O( n^(2) )`




    