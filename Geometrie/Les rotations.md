Les rotations sont des transformations du plan qui permettent d'émettre une rotation sur un élément tel qu'une droite, conique,... 

# Théorie

Il existe **deux matrices** pour faire la rotation:
* La rotation dans le sens horaire
* La rotation dans le sens anti-horaire

## Rotation horaire

$$\begin{pmatrix}  
cos(\theta) & -sin(\theta)\\  
sin(\theta) & cos(\theta)  
\end{pmatrix} 
\begin{pmatrix}  
x \\  
y  
\end{pmatrix}
=
\begin{pmatrix}  
x' \\  
y'  
\end{pmatrix}
$$

Ce qui équivaut pour $x'$ à $xcos(\theta)-ysin(\theta)$
Ce qui équivaut pour $y'$ à $xsin(\theta)+ycos(\theta)$

### Exemple de rotation avec une ellipse

Pour l'exemple, nous allons prendre l'ellipse d'équation:
$$\frac{x²}{9}+\frac{y²}{4}=1$$


![[Ellipse.png|450]]

J'applique une rotation de 30° à cette ellipse dans le sens horaire. Nous obtenons donc:
$$\frac{xcos(\frac{\pi}{6})-ysin(\frac{\pi}{6})}{9} + \frac{xcos(\frac{\pi}{6})+ysin(\frac{\pi}{6})}{4} = 1$$


![[Rotation ellipse sens horaire.png|450]]


## Rotation anti-horaire

$$\begin{pmatrix}  
cos(\theta) & sin(\theta)\\  
-sin(\theta) & cos(\theta)  
\end{pmatrix} 
\begin{pmatrix}  
x \\  
y  
\end{pmatrix}
=
\begin{pmatrix}  
x' \\  
y'  
\end{pmatrix}
$$

Ce qui équivaut pour $x'$ à $xcos(\theta)+ysin(\theta)$
Ce qui équivaut pour $y'$ à $-xsin(\theta)+ycos(\theta)$

### Exemple de rotation avec une droite

Voici une équation banale d'une droite:
$$y=2x$$
![[y=2x.png]]

Après une rotation anti-horaire avec la formule ci-dessous, nous faisons tourner cette droite à 60° vers la gauche.

$$x.cos(\frac{\pi}{3})+y.sin(\frac{\pi}{3})=2(-x.sin(\frac{\pi}{3})+y.cos(\frac{\pi}{3}))$$

![[Rotation de y=2x.png]]