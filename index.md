<style>background-color:#ffffff;</style>
## https://liamtapia.github.io/shellSort/
<h1>¿Qué es Shellsort?</h1>

<p align="justify"> <img src="https://liamtapia.github.io/shellSort/imagenes/imagen.png" style="float:right;width:128px;height:128px:"> 
Shellsort es una variación del Insertion sort, en lugar de mover elementos sólo una posición, se mueven varios espacios haciendo sub-arreglos.</p>

<p align="justify">Este ordenamiento fue  denominado así en honor a su desarrollador Donald Shell.</p>

<p align="justify">Donald Shell nació el primero de marzo de 1924 y falleció el 2 de noviembre del 2015 a la edad de 91 años. </p>

<p align="justify">Fue un científico del área de computación americano que creó el algoritmo de ordenamiento Shellsort y administró el departamento de ingeniería del nuevo Centro de Servicios de Información de la General Electric, la cual fue la primer empresa comercial en conectar computadoras usando la arquitectura cliente-servidor. Esta arquitectura es el diseño base del Internet.</p>

<h1>Funcionamiento del algoritmo</h1>
<p align="justify">Se considera el siguiente arreglo: </p>

<p style="text-align:center;">
<img src="https://liamtapia.github.io/shellSort/imagenes/ex1.JPG" width="500" height="40" class="center"> 
</p>

<p>Se divide el número de elementos entre 2 y se forma el primer sub arreglo: </p>

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
<h1></h1>
