# Notes Langage C#
- Auteur: DANSOKO Boubakar
- Date: 4/03/2019
- Source: MSDN 
- Lien utile: https://docs.microsoft.com/fr-fr/dotnet/csharp/tour-of-csharp/
### Création d'un projet

- Pour un projet en ligne de commandes:
```
dotnet new console
```

- Pour un projet en MVC:
```
dotnet new mvc
```

- Pour une app web:
```
dotnet new app
```

- Pour restaurer les packages
```
dotnet restore
```
- Pour lancer l'application:
```
dotnet run
```

## Syntaxe

### Commentaires
- `// Commentaire` : sur une ligne (avec le `//`)
- `/* Commentaires */`: délimité par `/*` au debut puis on fini par `*/` C'est à l'intérieur de celui-ci que l'on écrit nos commentaires.
- `///`: pour la documentation - dans visual studio (pas dans vs code) celà vas créer un summary au dessus d'une fonction, classe etc...

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
- `+` : addition
- `-` : soustraction
- `/` : divsion
- `%` : retourne le reste de la division

Raccourci / simplification:
- `++` : Incrémente la variable de 1 (ajoute 1 / +1)
- `--` : Décremente la variable de 1 (retire 1 / -1)
- `+=` : ajoute à la variable de gauche la valeur de droite
- `-=` : ajoute à la variable de gauche la valeur de droite

#### Exemples
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
string name = "Jean";
int age = 37;
string rep = name+" "+age+" ans";

Console.WriteLine(rep); // Jean 37 ans
```
### Conversion
### Boucles
#### For
- Théorie:
```
for(initialisation des valeurs/Compteurs ; condition de boucle; que faire à chaque boucle)
{
    Instruction;
    Instruction;
    ...
}
```
- Exemple:
```csharp
Console.WriteLine("Apprendre à compter jusqu'à 10.");

for(int i=1; i <= 10; i++)
{
    Console.WriteLine(i); //1 2 3 4 5 6 7 8 9 10
}
```
#### Do While
- Théorie:
```
Faire
{
    Instruction;
    Instruction;
    Instruction;

}
TantQue(ma condition est vrai/fausse/vérifié);
```
- Exemple:
```csharp
string mdp = "Youpi92";
string inp;

do
{
    Console.WriteLine("Entrez votre mot de passe:");
    inp = Console.ReadLine();
}
while(mdp != inp);
Console.WriteLine("Mot de passe correct.");

```
Noter que l'on entre dans le bloc au moins une fois et on peut rester bloqué à l'infini à moins de prévoir une évenutelle sortie.

#### While
- Théorie:
```
tantque(condition)
{
    Instruction;
    Instruction;
    ...
    ...
}

```
- Exemple:
```csharp
int compteur = 0;

while(compteur != 5)
{
    Console.WriteLine("La répétition est la clé de la maîtrise!");
    compteur++;
}
```
### Listes/Tableau

#### Tableau
- Théorie:
```cs
type[] nom = new type[taille];
type[] nom = new type[] {valeur1,valeur2, valeur3, .. ,..};
type[] nom = {valeur1, valeur2, .., ..};

type[,] nom = new int[nombre de colonne,nombre d item par colonne] 

```
- Exemple:
```csharp
//Déclaration + Instanciation
string[] prenom = new string[3];
int[] age = new int[3];

//Affectation des valeurs
prenom[0] = "Jean";
prenom[1] = "Franck";
prenom[2] = "Bernard";

age[0] = 15;
age[1] = 42;
age[2] = 85;

// équivaut à
string[] prenom = new string[]{"Jean","Franck","Bernard"}
int[] age = new int[]{12,42,85};


```
#### Listes
- Théorie:
```sh
List<type> nom = new List<type>(); //Déclaration +Instanciation
nom.Add(valeur1); //Affectation
nom.Add(valeur2);

// ou

List<type> = new List<type>(){valeur1, valeur2, valeur3, ... , ...}

```
- Exemple:
```csharp
List<string> noms = new List<string>();
noms.Add("Lilou");
noms.Add("Luc");
noms.Add("Louïse");
noms.Add("Liana");

for(int i=0; i < noms.Count;i++)
{
    Console.WriteLine(noms[i]);
} // Lilou Luc Louïse Liana 

// Equivaut à
List<string> noms = new List<string>(){"Lilou", "Luc", "Louïse", "Liana"};

for(int i=0; i < noms.Count; i++)
{
    Console.WriteLine(noms[i]);
} // Lilou Luc Louïse Liana

```
### Entrées / Sorties
#### Affichage dans la console
```csharp
string hello = "Hi Hello World!";
Console.WriteLine(hello);
```
### Conversion
- Théorie:
```


```
- Exemple:
```csharp
string n = "42";

```
### Fonctions

```sh
accessibilité type_de_retour nomDeLaFonction(typedeparamètre1 nomduParamètre1, typedeparamètre2)
{
    Instruction;
    Instruction;
    ...
} 
```

```csharp
public void Accueillir(string nom)
{
    Console.WriteLine($"Bienvenue à toi {nom}!");
}

public int InTenYears(int age)
{
    Console.WriteLine($"Dans dix ans vous aurez:{age+10}");
    return age + 10;    
}
```

## POO


