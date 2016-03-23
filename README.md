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




### End

**Sources**: https://github.com/mrzool/letter-boilerplate

PiT, Pierre Bettens <pb@namok.be>                                    
[@pinkilla](http://twitter.com/pinkilla)

2016 mars                                                                    
version 0.1                                                                     
                                                                                  
[![CC](cc-by-nc-sa-80x15.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/deed.fr)


[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=Pinkilla&url=https://github.com/Pinkilla/pandoc-pitletter&title=pandoc-pitletter&language=&tags=github&category=software)



