# Notes Langage C# - .Net/.Net core 
- Auteur: DANSOKO Boubakar
- Date: 4/03/2019
- Source: MSDN 
- Lien utile : https://docs.microsoft.com/fr-fr/dotnet/csharp/tour-of-csharp/
### Création d'un projet

Pour un projet en ligne de commandes:
```
dotnet new console
```

Pour un projet en MVC:
```
dotnet new mvc
```

Pour une app web:
```
dotnet new app
```

pour restaurer l'app
```
dotnet restore
```
pour lancer l'application:
```
dotnet run
```

## Syntaxe

### Commentaires
- `// Commentaire` : sur une ligne (avec le `//`)
- `/* Commentaires */`: délimité par `/*` au debut puis on fini par `*/` C'est à l'intérieur de celui-ci que l'on écrit nos commentaires.
- `///`: pour la documentation - dans visual studio celà vas créer un summary au dessus d'une fonction, classe etc...

### Variables
https://docs.microsoft.com/fr-fr/dotnet/csharp/tour-of-csharp/types-and-variables

Théorie:
```sh
type nom; //Déclaration
nom = valeur //affectation

type nom = valeur //Declaration + affectation
```
exemples 1:
```csharp
int age = 30;
string happy = "Yahou";

```
exemple 2:
```csharp
//Déclarations
int age;
string happy;

//Affectations
age = 30;
happy = "Yahou";

```

### Opérateurs
#### Théorie

Simple:
- `+`: addition
- `-`: soustraction
- `/`: divsion
- `%`: retourne le reste de la division

Raccourci / simplification:
- `++`: Incrémente la variable de 1 (ajoute 1 / +1)
- `--`: Décremente la variable de 1 (retire 1 / -1)
- `+=`: ajoute à la variable de gauche la valeur de droite
- `-=`: ajoute à la variable de gauche la valeur de droite


Exemple Opérations simple:
```csharp

int a = 3;
int b = 2;
int c = 1;

Console.WriteLine(a + b); //5
Console.WriteLine(a - b); //1
Console.WriteLine(a / b); //1
Console.WriteLine(a / c); //3
Console.WriteLine(a % b); //1
Console.WriteLine(a / c); //3

```
Exemple Incrémentation/Décrémentation:
```csharp
int a = 10;
int b = 653;

Console.WriteLine($"a={a} , b={b} - Avant incrément/décrementation"); //a=10 , b=653 - Avant incrément/décrementation


a++;
b--;

Console.WriteLine($"a={a} , b={b} - Après incrément/décrementation"); //a=11 , b=652 - Après incrément/décrementation
```
Exemple concaténation:
```csharp


```


