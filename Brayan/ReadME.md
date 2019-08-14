
# Readme 
_Hola, mi nombre es *Brayan Felipe Rojas Bernal* y estudio Ingenieria de sistemas en la Escuela Colombiana de Ingenieria Julio Garavito, ubicada en la ciudad de Bogotá._ ✒️


## Acerca de mi 🚀
Soy una persona apasionada por el deporte, he participado en diferetes actividades deportivas en las cuales he llegado a ser campeon del campeonato **B** de la universidad de **Football 7**. A su vez, quede tercero en un torneo  de **Ajedrez** organizado en el colegio. 

![Torneo de ajedrez](https://i.ibb.co/ZRr772c/Torneo-Ajedrez.jpg)
_Soy una persona que disfruta en aprender cosas nuevas cada dia 📌 y en especial ver feliz a la gente que me rodea_ 🤓.
### Actualmente estoy cursando ⚡️:  
>> **CVDS** Ciclos de Vida del Desarrollo de Software
>**ACSO** Arquitectura Computacional y Sistemas Operativos
>**CNYT** Ciencias Naturales y Tecnología
>**PRYE** Probabilidad y estadística
>**EGI3** Ingles 3



## Scripts

_El Convex Hull se puede definir como la intersección de todos los conjuntos convexos que contiene X y se pueden extender desde espacios euclidianos a espacios vectoriales reales._ 💥
```
 def hulls(points):
    if len(points) <= 1:
        return points

    def cross(o, a, b):
        return (a[0] - o[0]) * (b[1] - o[1]) - (a[1] - o[1]) * (b[0] - o[0])
    lower = []
    for p in points:
        while len(lower) >= 2 and cross(lower[-2], lower[-1], p) <= 0:
            lower.pop()
        lower.append(p)
    upper = []
    for p in reversed(points):
        while len(upper) >= 2 and cross(upper[-2], upper[-1], p) <= 0:
            upper.pop()
        upper.append(p)

    return  upper[:-1]+ lower[:-1]

```
> _Representacion grafica del  [Convex hull]([https://giphy.com/gifs/j5Eo5GyDDy08PgOULV](https://giphy.com/gifs/j5Eo5GyDDy08PgOULV))_

>>>>>>> Agregue mi ReadMe
