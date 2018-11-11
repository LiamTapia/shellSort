## Welcome to GitHub Pages

## https://liamtapia.github.io/shellSort/

You can use the [editor on GitHub](https://github.com/LiamTapia/shellSort/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

#Markdown
##Markdown
### Markdown

<h1>¿Qué es Shellsort?</h1>
<p> <img src="https://liamtapia.github.io/shellSort/imagenes/imagen.png" style="float:right;width:128px;height:128px:"> 
Shellsort es una variación del Insertion sort, en lugar de mover elementos sólo una posición, se mueven varios espacios haciendo sub-arreglos.</p>
<p>Este ordenamiento fue  denominado así en honor a su desarrollador Donald Shell.</p>


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

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/LiamTapia/shellSort/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
