---
title: \Huge\bf Utiliser pandoc pour écrire une lettre en markdown
author: notes·de·pit
date: 24 mars 2016
abstract:
geometry: margin=3cm
header-includes:
	- \renewcommand{\abstractname}{}
	- \renewcommand{\contentsname}{}
	- \usepackage{wallpaper}
---

\ThisLLCornerWallPaper{1}{letter-pit.jpg}
\pagebreak

Pour écrire une lettre, on peut utiliser un **traitement de texte** si l'on
veut. Par contre, si l'on a l'habitude d'écrire avec un **éditeur de texte**,
que l'on aime écrire en [*markdown*][blog] et que [`pandoc`][pandoc] est déjà
installé sur la machine, voici une alternative. 

Je veux pouvoir écrire une lettre très rapidement en ouvrant un éditeur de
texte et en y mettant quelque chose à l'allure suivante: 

```yaml
---
author: François Pignon
from:
 - Passerelle des champions du monde, 1
 - 1000 Bruxelles
 - fpignon@example.org
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

L'incroyable contenu de ma lettre. 
```

Les parties de ma lettre sont clairement identifiées (et facultatives). Elles
vont donc très vite à remplir. Le corps de ma lettre suit et se rédige en
*markdown* simple. Une fois que tout est mis en place, c'est très rapide. 

Pour générer le texte (*markdown* → LaTeX → PDF), un petit appel à `pandoc` et
c'est fait:

    pandoc lettre.md --template template/lettre.tex -o lettre.pdf

Le fichier `lettre.md` est la source de la lettre, le fichier `lettre.pdf` est
le document final à imprimer / envoyer… et le fichier `lettre.tex` est le
template à utiliser. C'est lui qui demande un peu de mise en place. Cette mise
en place ne doit être faite qu'une seule fois, ensuite, il est inutile de
toucher à ce fichier. Vous pouvez le laisser dans un coin de votre disque (ou
chez Claude). 

Bref, tout se trouve sur <http://github.com/Pinkilla/pandoc-pitletter>.
[D'autres template][pandoc-letter] se trouvent [facilement][boilerplate] mais
je préfèrais avoir « le mien ».  Vous pouvez l'adapter à vos goûts et [y
ajouter un *letterhead* si vous voulez][letterhead], un logo de votre
entreprise. 

\bigskip

*Crédit photo pit. Ma main, ma feuille, ma belle écriture.*  
*Billet publié sur [notes·de·pit][billet]*

[pandoc]:http://pandoc.org/
[pandoc-letter]:https://github.com/aaronwolen/pandoc-letter
[letterhead]:http://blog.hartleygroup.org/2015/08/01/a-pandoc-template-for-letterhead/
[boilerplate]:https://github.com/mrzool/letter-boilerplate
[blog]:http://namok.be/blog/?post/2013/11/19/billet-markdown
[billet]:http://namok.be/blog/?post/2016/03/25/pandoc-lettre-markdown
