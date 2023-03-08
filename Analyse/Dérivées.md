#review 

Selon la définition de la dérivée, le taux d'accroissement/variation d'une fonction (dérivée) au point $a$ se calcule avec la limite:
$$f'(a) = lim_{\Delta x\rightarrow 0}\frac{\Delta y}{\Delta x} = lim_{\Delta x\rightarrow 0}\frac{f(a+\Delta x)  -  f(a)}{\Delta x}$$


Exemple avec $f(x) = x³$
$$f'(x) = lim_{\Delta x\rightarrow 0}\frac{(x+\Delta x)³  - x³}{\Delta x} = lim_{\Delta x\rightarrow 0}\frac{x³ +3x²\Delta x + 3x\Delta x² + \Delta x³ - x³}{\Delta x}$$
$$= lim_{\Delta x\rightarrow 0}\frac{\Delta x(3x² + 3x\Delta x + \Delta x²)}{\Delta x} = lim_{\Delta x\rightarrow 0}3x² + 3x\Delta x + \Delta x² = 3x²$$

# Fonctions élémentaires

| Fonction | Dérivée    |
| -------- | ---------- |
| *$x^n$*  | $nx^{n-1}$ |
|$\frac{1}{x}$|$\frac{-1}{x²}$|
| $\sqrt{x}$ | $\frac{1}{2\sqrt(x)}$ |

# Fonctions exponentielles

|Fonction|Dérivée|
|---|---|
|$ln(x)$|$\frac{1}{x}$|
|$\log_{a}x$|$\frac{1}{xln(a)}$|
|$e^x$|$e^x$|

> [!tip]-
> Pour dériver une fonction exponentielle de la forme $a^x$, on peut effectuer la transformation: $$a^x = e^{ln(a^x)} = e^{xln(a)}$$

# Fonctions trigonométriques

|Fonction|Dérivée|
|------|-----|
|$sin(x)$|$cos(x)$|
|$cos(x)$|$-sin(x)$|
|$tan(x)$|$\frac{1}{cos²(x)}$ ou $1 + tan²(x)$|
|$arccos(x)$|$\frac{-1}{\sqrt{1-x²}}$|
|$arcsin(x)$|$\frac{1}{\sqrt{1-x²}}$|
|$arctan(x)$|$\frac{1}{1+x²}$|
