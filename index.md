## Welcome to GitHub Pages

## https://liamtapia.github.io/shellSort/

You can use the [editor on GitHub](https://github.com/LiamTapia/shellSort/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

 <img src="https://liamtapia.github.io/shellSort/imagenes/jorge.jpg" style="width:128px;height:128px:"> 
#Markdown
##Markdown
### Markdown

<h1>Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for caca</h1>

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
# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/LiamTapia/shellSort/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
