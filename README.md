## Métodos de ordenación
Los métodos de ordenación nos permite ordenar arrays. Pero ojo, debemos tener en cuenta que dependiendo del método de ordenación así será su eficiencia. Por lo que debemos tener en cuenta el tipo de datos que vamos a ordenar y el tamaño del array.

Puedes visualizarlos [aquí](https://www.cs.usfca.edu/~galles/visualization/Algorithms.html)

### Burbuja
Es un método de [ordenación](https://es.wikipedia.org/wiki/Ordenamiento_de_burbuja) con eficiencia O(n²). Es decir, el tiempo de ejecución es proporcional al cuadrado del tamaño del array. Este método consiste en ir comparando cada elemento con el siguiente, y si el elemento actual es mayor que el siguiente, se intercambian. Este proceso se repite hasta que no se producen más intercambios. Este método es muy sencillo de implementar, pero no es el más eficiente.

- https://www.youtube.com/watch?v=lyZQPjUT5B4


![imagen](https://upload.wikimedia.org/wikipedia/commons/c/c8/Bubble-sort-example-300px.gif)

# Explicación detallada de la Universidad Complutense de Madrid e implementación

- https://youtu.be/yfNLLIPtoYs?si=dF15CQtNe54oGk_M

# Este kata es muy recomendable: https://www.codewars.com/kata/5a63948acadebff56f000018/train/java

# Pseudocódigo

    funcion ProductOfMaxK() 
        definir array[5] entero = {4, 3, 5, 2, 1}
        definir k entero = 2
        definir producto entero = 1
        definir i, j, temp entero
    
        // Ordenar el arreglo de mayor a menor
        para (i <- 1; i <= longitud(array); i++) {
            para (j <- i + 1; j <= longitud(array) - 1; j++) {
                si (array[i] < array[j]) {
                    temp = array[i]
                    array[i] = array[j]
                    array[j] = temp
                }
            }
        }
    
        // Calcular el array de los primeros k números
        para (i <- 1; i <= k; i++) {
            producto = producto * (longitud(array) - 1 - i)
        }
    
        escribir "El producto de los ", k, " números máximos es: ", producto
    fin funcion

