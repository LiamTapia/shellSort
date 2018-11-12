<h1>¿Qué es Shellsort?</h1>

<p align="justify"> <img src="https://liamtapia.github.io/shellSort/imagenes/imagen.png" style="float:right;width:128px;height:128px;"> 
Shellsort es una variación del Insertion sort, en lugar de mover elementos sólo una posición, se mueven varios espacios haciendo sub-arreglos.</p>

<p align="justify">El algoritmo Shell sort mejora el ordenamiento por inserción comparando elementos separados por un espacio de varias posiciones. Esto permite que un elemento haga "pasos más grandes" hacia su posición esperada. Los pasos múltiples sobre los datos se hacen con tamaños de espacio cada vez más pequeños. El último paso del Shell sort es un simple ordenamiento por inserción, pero para entonces, ya está garantizado que los datos del vector están casi ordenados.</p>

<p align="justify">Este ordenamiento fue  denominado así en honor a su desarrollador Donald Shell.</p>

<p align="justify">Donald Shell nació el primero de marzo de 1924 y falleció el 2 de noviembre del 2015 a la edad de 91 años. </p>

<p align="justify">Fue un científico del área de computación americano que creó el algoritmo de ordenamiento Shellsort y administró el departamento de ingeniería del nuevo Centro de Servicios de Información de la General Electric, la cual fue la primer empresa comercial en conectar computadoras usando la arquitectura cliente-servidor. Esta arquitectura es el diseño base del Internet.</p>

<h1>Funcionamiento del algoritmo</h1>
<p align="justify">Se considera el siguiente arreglo: </p>

<p style="text-align:center;">
<img src="https://liamtapia.github.io/shellSort/imagenes/ex1.JPG" width="500" height="40" class="center"> 
</p>

<p align="justify">Se divide el número de elementos entre 2, obtenemos 5 y contamos desde el primer elemento para formar el primer sub-arreglo para enseguida ordenarlo: </p>

<p style="text-align:center;">
<img src="https://liamtapia.github.io/shellSort/imagenes/ex2.JPG" width="500" height="80" class="center"> 
</p>

<p>Se forma el siguiente sub arreglo: </p>

<p style="text-align:center;">
<img src="https://liamtapia.github.io/shellSort/imagenes/ex3.JPG" width="500" height="80" class="center"> 
</p>

<p>Se repite el proceso hasta hacerlo con todo el arreglo: </p>

<p style="text-align:center;">
<img src="https://liamtapia.github.io/shellSort/imagenes/ex4.JPG" width="500" height="40" class="center"> 
</p>

<p>El 5 que calculamos antes se divide entre 2 y se forman nuevos sub arreglos: </p>

<p style="text-align:center;">
<img src="https://liamtapia.github.io/shellSort/imagenes/ex5.JPG" width="500" height="80" class="center"> 
</p>

<p>Esto se repetirá hasta que el número que calculemos sea 1: </p>

<p style="text-align:center;">
<img src="https://liamtapia.github.io/shellSort/imagenes/ex6.JPG" width="500" height="40" class="center"> 
</p>

<h1>Ventajas del algoritmo ShellSort</h1>
<ul>
    <li>No requiere memoria adicional.</li>
    <li>Mejor rendimiento que el método de inserción clásico.</li>
    <li>5 veces más rápido que bubble sort.</li>
    <li>2 veces más rápido que insertion sort.</li>
</ul>
    
<h1>Desventajas del algoritmo ShellSort</h1>
<ul>
    <li>Implementación algo confusa.</li>
    <li>Realiza numerosas comparacciones e intercambios.</li>
    <li>Es significativamente más lento que merge, heap y quick sort.</li>
</ul>

<h1>Aplicaciones</h1>
<ul>
    <li>No suele ser utilizado de manera cotidiana pues los métodos Quicksort, Mergesort y Heapsort siguen siendo los más utilizados.</li>
    <li>Se usa en programas que ocupen menos cache de lo que se ocuparía en un método Quicksort.</li>
    <li>Se usa en aplicaciones que no ocupen llamar al execution stack.</li>
    <li>Se puede utilizar para comprimir archivos, usado en programas como bzip2.</li>
    <li>Está implementado en la función qsort de la librería uClibc de C.</li>
    <li>Es utilizado por el kernel de Linux en el procedimiento group_sort.</li>
</ul>
    
<h1>Implementación del algoritmo en C</h1>

```markdown
void shell_sort(int *a, int n)
{
    int i, j, gap, temp, z;
    for(gap = n/2; gap > 0; gap = gap/2){
        for(i = gap; i < n; i++){
            temp = a[i];
            for(j = i; j >= gap; j -= gap){
                if(temp < a[j - gap])
                    a[j] = a[j - gap];
                else
                    break;
            }
            a[j] = temp;
        }
    }
}
```

<h1>Explicación del código</h1>
<ol>
    <li><strong>Primer for:</strong> se encarga de obtener los “gap” al dividir en un comienzo el numero de valores en el arreglo entre dos,    para en las siguientes iteraciones dividir el mismo numero hasta llegar a 0.
    <li><strong>Segundo for:</strong> guarda el valor que se encuentra marcado por el “gap”, y realiza un tercer for que al terminar coloca el valor guardado por temporal en la posición correspondiente. Este for aumenta el contador para moverse a los siguientes bloques y acaba al llegar al último elemento del arreglo.  
    <li><strong>Tercer for:</strong> comienza en el elemento marcado por el “gap” y se mueve en orden decreciente a través de los elementos que indique el bloque en el que se dividió el arreglo.
    <li><strong>If else:</strong> revisa si el valor guardado en “temp” es menor al valor actual marcado por el for, de cumplirse , ese valor se mueve al elemento siguiente en el “gap”, de no cumplirse, se sale de la condición.
</ol>

<h1>Tiempos de ejecución para este código</h1>
<ul>
    <li>Peor caso: Θ(N (log N)^2)
    <li>Caso promedio: Θ(N (log N)^2)
    <li>Mejor caso: Θ(N logN)
</ul>

<h1></h1>
