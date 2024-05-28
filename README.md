<h1 align="center">Algorithme de Récursivité</h1>

**La récursivité** est une technique de programmation où une fonction s'appelle elle-même pour résoudre un problème. C'est une approche puissante utilisée pour résoudre des problèmes qui peuvent être divisés en sous-problèmes plus petits du même type. Voici un aperçu des concepts clés liés à la récursivité :

![Recursion](https://github.com/mohamedtalhaouii/Recursion/assets/144726758/6e6ee037-86b2-4f85-9d17-5bfde8aea959)


<h2>Concepts de Base</h2>

-  **Fonction Récursive :** Une fonction qui s'appelle elle-même.
-  **Cas de Base :** La condition qui arrête les appels récursifs pour éviter une récursion infinie.
-  **Appel Récursif :** L'étape où la fonction s'appelle elle-même avec des arguments modifiés pour progresser vers le cas de base.

<h2>Exemple de Récursivité</h2>

Un exemple classique de récursivité est le calcul de la factorielle d'un nombre \( n \) (noté \( n! \)), qui est défini comme :
\[ n! = n \times (n-1)! \]
Avec la condition que \( 0! = 1 \).

```python
def factorielle(n):
    if n == 0:
        return 1  # Cas de base
    else:
        return n * factorielle(n - 1)  # Appel récursif
```

<h2>Avantages</h2>

- **Simplicité et Clarté :** Les solutions récursives peuvent être plus simples et plus intuitives pour certains problèmes comme les arbres, les graphiques, et les structures de données imbriquées.
- **Décomposition Naturelle :** Facilite la décomposition des problèmes complexes en sous-problèmes plus petits et plus gérables.

<h2>Inconvénients</h2>

- **Consommation de Mémoire :** Chaque appel récursif ajoute une nouvelle couche à la pile d'appels, ce qui peut conduire à une utilisation excessive de la mémoire et des débordements de pile pour les grandes entrées.
- **Performance :** Les solutions récursives peuvent être moins performantes que les itératives en raison des appels de fonction répétés.

<h2>Optimisations</h2>

- **Mémorisation (Memoization) :** Technique de stockage des résultats des appels de fonction pour éviter les calculs redondants.
- **Récursion Terminale (Tail Recursion) :** Forme de récursion où l'appel récursif est la dernière opération dans la fonction, permettant certaines optimisations par le compilateur ou l'interpréteur.

<h2>Exemple d'Optimisation avec Mémorisation</h2>

Voici un exemple de calcul de la série de Fibonacci avec mémorisation pour améliorer l'efficacité.

```python
def fibonacci(n, memo={}):
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fibonacci(n - 1, memo) + fibonacci(n - 2, memo)
    return memo[n]
```

En résumé, la récursivité est une méthode puissante et expressive pour résoudre des problèmes qui peuvent être divisés en sous-problèmes similaires. Toutefois, il est important de prendre en compte les limites et les optimisations nécessaires pour éviter les problèmes de performance et de consommation de mémoire.

<hr>
<h3 align="center"> 🧑🏻‍💻 | Made By : <a href="https://github.com/mohamedtalhaouii" target="_blank">Mohamed Talhaoui</a></h3>
