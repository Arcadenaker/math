#review 

L'intégrale a beaucoup d'utilités et permet de trouver l'aire sous une fonction, résoudre des équations différentielles,...

# Les primitives

La primitive d'une fonction $f(x)$ s'écrit $F(x)$. Celle-ci est la même chose que l'intégrale mais de manière générique pour toute la fonction, c'est la première étape d'une intégration définie. 

Une intégrale revient à faire la dérivée à l'envers et satisfait donc cette égalité: $F'(x) = f(x)$. Il est donc à noter que le tableau des [[Dérivées|dérivées]] est tout à fait valide.
$$\int f(x) dx = F(x) + C$$

La seule primitive moins intuitive est $\int x^ndx=\frac{x^{n+1}}{n+1}$. Pour le reste c'est juste le tableau à l'envers.

> [!DANGER]+
> Il est très important de ne pas oublier la constante $C$ à la fin de la primitive car il existe une infinité de primitives qui satisfont cette intégrale indéfinie.


# Les intégrales définies

Toute fonction continue sur un segment $[a, b]$ admet des primitives, et que l'intégrale de $a$ à $b$ est égale à _F_(_b_) – _F_(_a_), indépendamment de la primitive choisie.

Autrement dit:
$$\int_a^bf(x)dx = [F(x)]_a^b = F(b) - F(a)$$

Il peut être judicieux de **regarder la parité** de la fonction car 
* Si f(x) est paire et que $a = -b$ alors l'intégrale peut se réécrire: $2\int_{0}^{b}f(x)dx$.
* Si f(x) est impaire et que $a = -b$ alors la valeur de l'intégrale vaut 0.


# Les méthodes d'intégration

>[!warning]
>Les outils ci-dessous ne suffisent parfois pas à eux seuls il faut donc les combiner à d'autres méthodes ou les répéter plusieurs fois!

## Substitution

On utilise cette méthode pour intégrer une fonction qui en contient une autre. 

On pose une variable (ex: $t$) qui va servir à simplifier l'expression de l'intégrale et continuer à intégrer avec d'autres méthodes ou utiliser le tableau des primitives usuelles.

Après avoir posé la nouvelle variable (ex: $t$), il faut dériver les 2 côtés de l'égalité pour se retouver (par exemple) avec du $dt$ à gauche et $dx$ à droite (variable de l'intégrale). Il suffit juste de représenter $dx$ par rapport à $dt$.

**Voilà une brève démonstration de la méthode:**

$$\int_{1}^{2}(3x)²dx = \int_{1}^{2}t²dx = \frac{1}{3}[\frac{x³}{3}]_{1}^{2} = \frac{1}{3}(\frac{8}{3} - \frac{1}{3}) = \frac{7}{9}$$
$$t=3x$$
$$dt=3dx$$
$$\frac{dt}{3}=dx$$

>[!warning]
>Cette méthode comporte certaines limites car il faut dériver le contenu de la variable et l'exprimer par rapport à $dx$ et peut dans certaines situations compliquer et ne pas suffir. C'est pour cela qu'il est important de la combiner avec d'autres procédés.


## Par partie 

Cette méthode est redoutable pour intégrer un produit de 2 fonctions.
$$\int a(x).b(x)dx = f.g -\int f'.gdx$$
On pose une des deux fonctions (au choix) qui va être $f$ et l'autre $g'$.

$f=a(x)$ ou $b(x)$          $f' = A(x)$ ou $B(x)$
$g'=b(x)$ ou $a(x)$         $g = b'(x)$ ou $a'(x)$

Voilà un petit exmple pour cette méthode:

$$\int_{1}^{2}x.ln(x)dx = [\frac{x²ln(x)}{2}]_{1}^{2}-\int_{1}^{2}\frac{x}{2}dx$$

$f= ln(x)$          $f' = \frac{1}{x}$
$g'= x$        $g = \frac{x²}{2}$

$$[\frac{x²ln(x)}{2}]_{1}^{2} - \frac{1}{2}[\frac{x²}{2}]_{1}^{2} = 2ln(2)-\frac{1}{2}(2-\frac{1}{2}) = 2ln(2)-\frac{3}{4}$$

>[!warning]+
>Il est possible que l'intégration par partie redonne l'intégrale de base (boucle), voici une manière de palier à ce problème:
>$$\int e^xsin(x)dx$$
>$f= sin(x)$          $f' = cos(x)$
>$g'= e^x$          $g = e^x$
>$$=e^xsin(x)-\int e^xcos(x)dx$$
>$f= cos(x)$          $f' = -sin(x)$
>$g'= e^x$          $g = e^x$
>$$e^xsin(x)-(e^xcos(x)+\int e^xsin(x)dx)$$
>(_On passe l'intégrale à gauche_)
>$$2\int e^xsin(x)dx = e^xsin(x)-e^xcos(x)$$
>$$\int e^xsin(x)dx = \frac{e^xsin(x)-e^xcos(x)}{2} + C$$

## Méthode du "+1 -1"

La méthode du "+1 -1" peut être utile pour débloquer certaines situations où il peut être intéressant de faire un binôme conjugué dans une fraction par exemple.

Voici une démonstration:
$$\int \frac{cos²x}{1+cos(x)}dx = \int \frac{cos²x+1-1}{1+cos(x)}dx$$
$$\int \frac{(cos(x)+1)(cos(x)-1)}{1+cos(x)}dx-\int \frac{1}{1+cos(x)}dx$$
$$\int cos(x)dx-\int1dx-\int \frac{1}{1+cos(x)}dx$$
Selon les formules de Carnot:   $1+cos(x)=2cos²(\frac{x}{2})$
$$sin(x)-x-\int \frac{1}{2cos²(\frac{x}{2})}dx$$
$$t=\frac{x}{2}$$
$$2dt=dx$$
$$sin(x)-x-tan(\frac{x}{2}) + C$$

## Méthode de Euler

Il peut parfois être utile de passer par les complexes avec les formules d'Euler pour résoudre des intégrales de la forme $\int sin^n(x)dx$ avec des bornes différentes de $\frac{\pi}{2}$ car alors ce serait une intégrale de Wallis, plus facile à résoudre avec un théorème plus bas.

>[!todo]+ Exemple concret
>$$\int_{0}^{2022}sin⁵(\frac{\pi x}{2})dx$$
>$$t=\frac{\pi x}{2}$$
>$$\frac{2}{\pi}dt=dx$$
>$$=\int_{0}^{2022}sin⁵(t)dx$$
>----------------
>_Selon Euler:_
>$$sin(x)=\frac{e^{ix} -e^{-ix}}{2i}$$
>_En épargnant le développement..._
>$$sin⁵(x)=(\frac{e^{ix} -e^{-ix}}{2i})⁵$$
>$$=\frac{1}{16} (sin(5x)-5sin(3x)+10sin(x))$$
>----------------
>$$=\frac{1}{16} (\int_{0}^{2022}sin(5t)dx-5\int_{0}^{2022} sin(3t)dx+10\int_{0}^{2022} sin(t)dx)$$
>
>_**La suite est triviale**_

## Simplification par division polynomiale

Quand on arrive à une division de 2 polynômes, il est vivement conseillé d'essayer la division polynomiale et de voir si cela aide ou pas.