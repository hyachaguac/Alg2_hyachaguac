Proyecto Final - Algoritmos 2021-2

- Johan Steeb Rodríguez Alarcón
- Santiago Alexander Rodríguez Triana
- Harol Achagua Clavijo
- Andrés Felipe Moreno Pinzón

import time
first_time = time.time()
def dijsktra(Grafo, Nodos):
    
    grafo = nx.to_dict_of_lists(Grafo)              		O(1)
    #print(grafo)                                    		
    S = []; Queue = [];                                 O(1)
    anterior = [0 for i in range(max(grafo)+1)]; 		    O(1)
    distancia = [0 for i in range(max(grafo)+1)]		    O(1)
    
    for nodo in grafo:                             		  O(n)
        distancia[nodo] = 10000					                O(1)
        Queue.append(nodo)					                    O(n)
        
    distancia[Nodos[0]] = 0                         		O(1)
    
    while not len(Queue) == 0:					                O(n)
        distancia_minima = 10000				                O(1)
        for nodo in Queue:					                    O(n)
            if distancia[nodo] < distancia_minima:		  O(1)
                distancia_minima = distancia[nodo]	  	O(1)
                nodo_temporal = nodo                		O(1)
        nodo_distancia_minima = nodo_temporal			      O(1)
        Queue.remove(nodo_distancia_minima)			        O(1)
        
        for vecino in grafo[nodo_distancia_minima]:		      O(n)
            if distancia[nodo_distancia_minima] == 10000:	  O(1)
                distancia_temporal = 0                    	O(1)
            else:
                distancia_temporal = distancia[nodo_distancia_minima]					O(1)  
            distancia_con_peso = distancia_temporal + Grafo[nodo_distancia_minima][vecino]['weight']	O(1)
            if distancia_con_peso < distancia[vecino]:		O(1)
                distancia[vecino] = distancia_con_peso		O(1)
                anterior[vecino] = nodo_distancia_minima	O(1)
                
        if nodo_distancia_minima == Nodos[1]:			O(1)
            if anterior[nodo_distancia_minima] != 0 or nodo_distancia_minima == Nodos[0]:	O(1)
                while nodo_distancia_minima != 0:						      O(n)
                    S.insert(0, nodo_distancia_minima)						O(1)
                    nodo_distancia_minima = anterior[nodo_distancia_minima]			O(1)
                return S									O(1)

print(f"Camino mas corto en distancia: {dijsktra(GD, (6, 10))}")
print(f"Camino más corto en tiempo: {dijsktra(GT, (6, 10))}")

O(dijsktra) = O(n)
