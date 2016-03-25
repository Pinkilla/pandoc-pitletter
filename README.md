# Template de lettre pour pandoc

Ce template est a utiliser avec `pandoc` pour écrire des lettres. À l'usage,
écrire un document en *markdown* contenant un entête `Yaml` de la forme: 

```yaml
---
author: François Pignon
from:
 - Passerelle des champions du monde, 1
 - 1000 Bruxelles
 - \texttt{fpignon@example.org}
to: 
 - Éditions ACME
 - Pierre Brochan
 - Ruelle incroyable, 112
 - 1000 Bien bien loin
object: L'objet de ma lettre
vref: Vos références
mref: Mes références
opening: Monsieur,
closing: Salutem dicit   
---
```

Cet entête est suivi du corps de la lettre en *markdown* et se compile avec
une commande du style

    pandoc lettre.md --template template/lettre.tex -o lettre.pdf 

### Structure du répo

Le seul fichier nécessaire est le fichier `template/lettre.tex`.  
Les fichiers `lettre.md` et `lettre.pdf` servent d'exemple tandis que les
fichiers `blog*` référencent l'[article du
blog](http://namok.be/blog/?post/2016/03/25/pandoc-lettre-markdown).   
Les images sont… des images. 

```
.
├── blog-pandoc-pitletter.md
├── blog-pandoc-pitletter.md.pdf
├── cc-by-nc-sa-80x15.png
├── letter-pit.jpg
├── lettre.md
├── lettre.pdf
├── README.md
└── template
    └── lettre.tex
```


### End

**Sources**: https://github.com/mrzool/letter-boilerplate

PiT, Pierre Bettens <pb@namok.be>                                    
[@pinkilla](http://twitter.com/pinkilla)

2016 mars                                                                    
version 0.1                                                                     
                                                                                  
[![CC](cc-by-nc-sa-80x15.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/deed.fr)


[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=Pinkilla&url=https://github.com/Pinkilla/pandoc-pitletter&title=pandoc-pitletter&language=&tags=github&category=software)



