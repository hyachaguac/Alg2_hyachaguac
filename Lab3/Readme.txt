import time 
def f(x):
    return -x**4 + 30*(x**3) + 15*(x**2) + 34*x + 540 

def bisection (vi, vf): 
    fvi = f(vi) #O(1)
    fvf = f(vf) #O(1)
    c = (vi+vf)/2 #O(1)
    fc = f(c) #O(1)

    if abs(fc) <= 0.001: #O(1)
        return c #O(1)
    elif fvi*fc < 0: #O(1)
        return bisection(vi, c) #O(log(n)) siendo n la longitud del intervalo, ya que en cada recursión se divide a la mitad
    else: #O(1)
        return bisection(vf, c) #O(log(n))

tiempo_inic = time.time()
print(bisection(-1000, 1000))
print("Tiempo de ejecución:",time.time()-tiempo_inic,"s") 

O(bisection) = O(1) + O(1) + O(1) + O(1) + O(1) + O(1) + O(1)(O(log(n)) + O(1)(O(log(n)) 
O(bisection) = O(log(n))
