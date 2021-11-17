Taller 1 - Secueecia del Genoma Viral de referencia Sars-Cov 2

longitud = len(target)                          					                  O(1)
primer = target[0]									                                        O(1)
for i in range(len(secuence)):								                              O(n)	
    if primer == secuence[i]:								                                O(1)
        if secuence[i:i+longitud] == target:						                    O(1)  (En python, el slice es O(longitud), en este caso O(25), sin embargo, en este caso esa longitud es constante, por lo que queda como O(1)
            print('Posición inicial:', i,'\nPosición final:', i+longitud)		O(1)
            break									                                          O(1)

O(r) = O(1) + O(1) + O(n)[4*O(1)] = O(n)

Grupo #4
