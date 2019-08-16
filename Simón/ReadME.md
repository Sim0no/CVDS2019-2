# Readme
*Bienvenido, mi nombre es **Germán Simón Marín Mejía**,* soy estudiante de la [Escuela Colombiana de Ingeniería](https://www.escuelaing.edu.co/es/) 

## Acerca de mi
Nací en Bogotá en el año 2000, estudio *ingenieria de sistemas* y disfruto de practicar baloncesto y tennis de mesa.


  ![Mesa de ping pong](https://image.freepik.com/foto-gratis/tenis-mesa-o-ping-pong_1232-2632.jpg)
  ![Cesta y Balon](http://www.dondeporte.com/wp/wp-ddp/wp-content/uploads/2018/04/medidas-canastas-baloncesto.jpg)


Actualmente estoy cursando el plan de estudios *#14* y  me encuentro cursando las siguientes asignaturas: 
- Ciclos de vida del Desarrollo de Software
- Redes de Computadores
- Probabilidad y Estadistica
- Fundamentos contables y financieros
- Ingles 4

## Scripts
1. Problema 1235 de uVa, [Anti Brute Force Lock](https://uva.onlinejudge.org/index.php?option=com_onlinejudge&Itemid=8&page=show_problem&problem=3676), resuleto por mi en Python para la clase de *Programación imperativa modular*


        from sys import stdin
        def findpadre(x):
            global padre,rank
            p=padre[x]
            if p!=x:
                padre[x]=findpadre(padre[x])
            return padre[x]
        def union(x,y):
            global padre,rank
            xp=findpadre(x)
            yp=findpadre(y)
            if xp!=yp:
                if rank[xp]>rank[yp]:
                    padre[yp]=xp
                    rank[xp]+=1
                else:
                    padre[xp]=yp
                    rank[yp]+=1
                return True
            return False
        #Algoritmo de Kruskal
        def kruskal(adj):
            total=0
            for arco in adj:
                if union(arco[1],arco[2]):
                    total+=arco[0]
            return total
        def minimo(st1,st2):
            res = 0
            for i in range(4):
                res +=min(abs(int(st1[i])-int(st2[i])),10-abs(int(st1[i])-int(st2[i])))
            return res
        def main():
            global padre,rank
            x = int(stdin.readline().strip())
            for i in range(x):
                dic = {}
                inicial = '0000'
                ady = []
                minimus =  []
                lista = stdin.readline().strip().split()
                casos = int(lista.pop(0))+1
                padre=[i for i in range(casos)]
                rank=[0 for i in range(casos)]
                ini = 0
                for j in lista:
                    dic[j] = ini
                    ini += 1
                    minimus.append(minimo(inicial,j))
                minimus = min(minimus)
                while len(lista) != 1:
                    nodo = lista.pop(0)
                    for k in lista:
                        dista = (minimo(nodo,k),dic[nodo],dic[k])
                        ady.append(dista)
                ady.sort()
                ans = kruskal(ady)
                print(ans+minimus)   
        main()
2. [Pigeon Hole Sort](https://www.youtube.com/watch?v=nVQz0kZNC64), ordenamiento con complejidad O(n + Rango):

        def pigeonhole_sort(a): 
            minimo,maximo = min(a),max(a) 
            Rango = maximo - minimo + 1
            agujeros = [0] * Rango 
            for elementos in a: 
                agujeros[elementos - minimo] += 1
            i = 0
            for count in range(Rango): 
                while agujeros[count] > 0: 
                    agujeros[count] -= 1
                    a[i] = count + minimo
                    i += 1
            return a
              
# END

Muchas gracias por visitar mi perfil, vuelva pronto :)

# LABORATORIO #1

## MAIN

![pantallazo1](https://i.ibb.co/44T6Gct/PARTE-1.png)


## REMOTE

![pantallazo2](https://i.ibb.co/FmwTbYF/Captura1.png)

![pantallazo3](https://i.ibb.co/JdcD91k/Captura2.png)




>  Saber es recordar a tiempo. 
>
>    Raul Chaparro, 2018 
