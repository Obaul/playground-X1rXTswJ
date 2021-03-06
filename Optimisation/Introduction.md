# Bienvenue pour cette nouvelle partie : Optimisation

Dans cette partie, nous allons présenter différentes manières d'améliorer vos programmes principalement en rapidité. Pour l'instant, il n'est pas prévu de faire une partie cours sur la complexité algorithmique (je vous renvoie vers internet) mais seulement de présenter des méthodes pour programmer efficacement dans certaines situations classiques.

Je profite de cette page pour mettre quelques astuces courtes qui ne méritent pas une page à elles seules mais qui peuvent faire gagner du temps.

### Préférer les variables locales aux globales quand c'est possible. 

Autrement dit, il vaut mieux créer des fonctions pour faire des boucles longues plutôt que les lancer directement.  
Exemple : Considérons les deux façons de programmer suivante  
``` python
# Méthode directe
n=0
for i in range(10**8):
    n+=1
```  
et
```python
# Méthode en mettant la boucle dans une fonction
def fonction():
    n=0
    for i in range(10**8):
        n+=1

fonction()
```  
A priori, on fait la même chose or la première méthode met 15 sec pour s'executer et la seconde seulement 10 sec. Ce qui est énorme comme différence pour faire exactement la même chose donc il vaut mieux, quand on a des boucles longues, les mettre dans une fonction.
