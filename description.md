Definamos otra función que utiliza argumentos, en este caso es una función simple que indica si un número natural es a la vez par.

``` python
def entero_par(numero):
    # evaluacion de las condiciones logicas
    if numero % 2 == 0 and numero > 0:
        return True
    else:
        return False
  
```
Veamos los posibles llamados a esta función.


``` python
for numero in [1,2,3,4,5]:
    print(entero_par(numero))
```
  _Salida:_
**False**
**True**
**False**
**True**
**False**

Ahora vamos a definir una función que toma un número `num` y devuelve una lista en donde cada posición es el resultado de potenciar el número, con el valor de la posición.

``` python
def elevado(num):
    # definimos una lista vacia
    mi_lista = []
    
    # iteramos en un rango de 10 asignando un valor creciente a i (crece de 1 en 1)
    for i in range(10):
        # elevamos a la potencia dada en i y lo guardamos en num_elevado
        num_elevado = num ** i
        # guardamos al final de la lista el numero elevado a la potencia i
        mi_lista.append(num_elevado)
      
    return mi_lista  

# hacemos el llamado a función y lo imprimimos.
print(elevado(2))
```
  _Salida:_
**[1, 2, 4, 8, 16, 32, 64, 128, 256, 512]**

#### Explicación
Definimos una función que toma un numero `num`, a este valor se le llama argumento.

Dentro de la función lo primero que hacemos es definir una lista vacía, esta lista la definimos vacía para poblarla durante la iteración.

La idea es que a medida que iteramos sobre el `range(10)` el valor de `i` cambie sucesivamente, sumando 1 en cada iteracion. 

Este valor de `i` lo utilizamos para elevar el numero `num` que pedimos como argumento de la función.

El resultado de elevar el número lo guardamos en la variable `num_elevado` y utilizamos el método `append` para integrarlo a la lista, durante la iteración.

Una vez que la iteración termina, la función devuelve la lista con los valores calculados.
