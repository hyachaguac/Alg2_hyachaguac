Cálculo de complejidad de tiempo de cada algoritmo:

Número de Fibonacci

def calc_fib(n):

    res1, res2  = 1, 1 # O(1)
    if n <= 0: # O(1)
        return 0 # O(1)
    elif n>100:  # O(1)
        return "Por favor, ingrese un número menor a 100" # O(1)
    else: # O(1)
        for i in range(2, n): # O(n)
            res2, res1 = res1 + res2, res2 # O(1)
        return res2 # O(1)

O(calc_fib) = O(1) + O(1) + O(1) + O(1) + O(1) + O(1)(O(n)*O(1)) + O(1)
O(calc_fib) = O(n)

Multiplicación La Russe

def la_russe(n,m):
    resp = 0  # O(1)

    if (n < 0 or n > 5) or  (m < 0 or m > 5): #O(1)
        return resp   # O(1)

    while (m>0):  # O(log(m)) Esto debido a que m se parte (aproximadamente) a la mitad en cada iteración

        if m%2 != 0: # O(1)
            resp += n O(1)

        n = 2*n  # O(1)
        m = m//2 # O(1)
    return resp # O(1)

O(la_russe) = O(1) + O(1) + O(1) + O(log(m))*(O(1) + O(1) + O(1) + O(1)) + O(1)
O(la_russe) = O(log(m))
