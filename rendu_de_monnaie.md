# Problème du rendu de monnaie en le moins de "pièces" possible

### Remarque: ce problème a plusieurs solutions et est un classique des problèmes utilisant la récursivité.

Si vous rencontrez des difficultés avec ce problème (ou que cela semble prendre beaucoup de temps dans certains cas), consultez la page wikipedia, car ce problème est assez connu et a, en fait, sa propre [entrée Wikipedia (en)](https://en.wikipedia.org/wiki/Change-making_problem) ou [entrée Wikipedia (fr)](https://fr.wikipedia.org/wiki/Problème_du_rendu_de_monnaie)! 

## Description du problème

 Avec un montant cible **n** et une liste (tableau) des valeurs des pièces (on supposera que l'on a autant de pièces d'une valeur présente dans le tableau que l'on veut), quelle est la quantité de pièces minimale nécessaire pour effectuer le montant du rendu de monnaie. 
 
 Par exemple: Si n = 10 et que les pièces sont = [1,5,10]. Alors, il y a 4 façons possibles de faire de la monnaie sur 10: 
 
 * 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1 + 1
 * 5 + 1 + 1 + 1 + 1 + 1
 * 5 + 5
 * 10

 Et le rendu de monnaie demandant le moins de pièces est ici 10, soit une pièce (de 10 en l'occurence, si vous avez bien suivi ;-) )

 avec comme valeurs des pièces les valeurs [1, 2, 5], en appelant notre fonction rec_coin(valeur_cible, [valeur_unitaire_monnaie, ...]),
 
  on aura:

 rec_coin(17, [1, 2, 5]) = 4 (soit 5 + 5 + 5 + 2)

 rec_coin(23, [1, 2, 5]) = 6 (soit 5 + 5 + 5 + 5 + 2 + 1)

Ceci est un bon prétexte pour écrire vos tests et faire du Test-Driven Development (TDD), j'dis ça, j'dis rien...