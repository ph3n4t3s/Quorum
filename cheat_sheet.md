## Quorum

#### Variables et types

```quorum
integer nombreEntier = 42
number nombreDecimal = 3.14
text chaine = "Bonjour"
boolean estVrai = true
```

#### Opérations arithmétiques sur des entiers

```quorum
integer somme = a + b
integer difference = a - b
integer produit = a * b
integer quotient = a / b // Conversion implicite en entier
integer modulo = a mod b // Reste de la division entière
```

#### Concaténation de chaînes de caractères

```quorum
text prenom = "Jean"
text nom = "Dupont"
text nomComplet = prenom + " " + nom
output nomComplet
```

#### Saisir un nombre

```quorum
text ageTexte = input("Entre ton âge : ") // Lecture d'un nombre en texte
integer age = cast(integer, ageTexte) // Conversion explicite en entier
output "Tu es né(e) soit en " + (2025 - age) + ", soit en " + (2024 - age)
```

#### Structure conditionnelle if - else  *(avec opérateur différent de)*

```quorum
text nombreTexte = input("Quel est le nombre à inverser ?")
number nombre = cast(number, nombreTexte) // Conversion de type explicite
if nombre not= 0
    number inverse = 1/nombre
    output "Inverse " + inverse // Conversion de type implicite
else
    output "Division par zéro"
end
```



#### Conditions multiples  *(attention à l'ordre !)*

```quorum
number temperature = 85
if temperature >= 100
    output "L'eau boue et se transforme en vapeur"
elseif temperature <= 0
    output "L'eau se transforme en glace"
else
    output "L'eau est à l'état liquide"
end
```

#### Boucle repeat times

```quorum
repeat 5 times
    output "Itération en cours"
end
```

#### Boucle repeat while  *(répète tant que c'est vrai)*

```quorum
integer compteur = 0
repeat while compteur < 5
    output compteur
    compteur = compteur + 1
end
```

#### Boucle repeat until  *(répète jusqu'à ce que ça devienne vrai)*

```quorum
integer valeur = 0
repeat until valeur = 5
    valeur = valeur + 1
end
```

#### Action

```quorum
action Add(integer a, integer b) returns integer
    return a + b
end
```

