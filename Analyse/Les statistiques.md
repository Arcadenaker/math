>[!TODO] Vocabulaire
> -**ECC**: Effectifs Cumulés Croissants
>-**$C_{i}$**: Centre de l'intervalle
>-**$n_{i}$**: Effectifs
>-Le **mode** est la valeur de la variable la plus fréquente de la population étudiée.
>-La **médiane** est la valeur de la variable qui permet de partager la population étudiée en deux.


# Théorie pour variable continue avec exemple

Voici une représentation de la répartition des notes obtenues à une évaluation dans une classe

|Notes|$n_{i}$|$C_{i}$|ECC|
|------|-------|---|---|
|$[0;4[$|10|2|10|
|$[4;8[$|15|6|25|
|$[8;12[$|30|10|55|
|$[12;16[$|20|14|75|
|$[16;20[$|5|18|80|
||N = 80|||

## Calcul de la moyenne

$$\bar{x}=\frac{\sum n_{i}.C_{i}}{N}$$
$$\bar{x}=\frac{2.10+6.15+10.30+14.20+18.5}{80}=\frac{780}{80}=9,75$$

## Calcul de la variance

$$V=\frac{\sum n_i(C_i-\bar{x})²}{N}$$
$$V=\frac{10(2-9,75)²+15(6-9,75)²+30(10-9,75)²+20(14-9,75)²+5(18-9,75)²}{80}=18,93$$

## Calcul de l'écart-type

$$\sigma=\sqrt{V}$$
$$\sigma=\sqrt{18,93}=4,35$$

## Calcul de la médiane (2ème quartile)

$$\frac{N}{2}=\frac{80}{2}=40$$
40 appartient à la classe $[8(x_{1});12(x_{2})[$ (combinaison de la classe 2 et 3)
40 appartient donc à l'effectif cumulé $[25(f(x_{1}));55(f(x_{2}))[$
$$\frac{Me-x_{1}}{\frac{N}{2}-f(x_{1})}=\frac{x_{2}-x_{1}}{f(x_{2})-f(x_{1})}$$
$$\frac{Me-8}{40-25}=\frac{12-8}{55-25}$$
$$\frac{Me-8}{15}=\frac{4}{30}$$
$$Me-8=\frac{60}{30}$$
$$Me=2+8=10$$

Ce qui signifie que 50% des étudiants ont obtenu une note égale ou en dessous de 10.

>[!NOTE]
>Il y a également moyen de trouver la médiane en traçant le graphique des **ECC et ECD par rapport aux notes**. Ce sera donc l'intersection des 2 courbes. Il est à noter que c'est moins précis.

## Calcul du troisième quartile

$$\frac{3N}{4}=\frac{160}{4}=60$$
60 appartient à la classe $[12(x_{1});16(x_{2})[$ (combinaison de la classe 2 et 3)
60 appartient donc à l'effectif cumulé $[55(f(x_{1}));75(f(x_{2}))[$

$$\frac{Q_{3}-x_{1}}{\frac{3N}{4}-f(x_{1})}=\frac{x_{2}-x_{1}}{f(x_{2})-f(x_{1})}$$
$$\frac{Q_{3}-12}{60-55}=\frac{16-12}{75-55}$$
$$\frac{Q_{3}-12}{5}=\frac{4}{20}$$
$$Q_{3}-12=\frac{20}{20}$$
$$Q_{3}=1+12=13$$

Ce qui signifie que 75% des étudiants ont obtenu une note égale ou en dessous de 13.

>[!SUCCESS] L'écart interquartile
>L'écart interquartile se calcule en faisant $Q_3-Q_1$ 

# Théorie pour variable discrète avec exemple

Soit la distribution statistique d'une population de 30 élèves d'une classe selon leur âge:

|Age|$n_i$|ECC|
|----|----|--|
|14|6|6|
|15|10|16|
|16|10|26|
|17|2|28|
|18|2|30|
||N = 30||

>[!TODO]
>Les calculs de la moyenne, de la variance et de l'écart-type restent les mêmes donc ne seront pas répétés pour cet exemple

## Calcul de la médiane

Le tableau ci-dessus montre que l'effectif total (N) est de 30, donc $\frac{N}{2}$ = 15. 
Grâce au tableau des ECC, on voit que 15 est atteint entre 14 et 15 ans donc par convention on va choisir la limite supérieure qui est **15 ans**.

## Calcul du troisième quartile

Le tableau ci-dessus montre que l'effectif total (N) est de 30, donc $\frac{3N}{4}$ = 22,5. 
Grâce au tableau des ECC, on voit que 22,5 est atteint entre 15 et 16 ans donc par convention on va choisir la limite supérieure qui est **16 ans**.