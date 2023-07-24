# hello-rust

## Introduction
L'object de ce dépôt est de construire un atelier de découverte du langage **Rust** dans le cadre de l'initiation au codage d'Ada-flow.

Pour cela on utilisera le tutoriel de [Guillaume Gomez](https://blog.guillaume-gomez.fr/Rust)

En y ajoutant des points sautés et des exercices de code fait en python3.


## l'installation

Le tutoriel de Guillaume Gomez n'aborde pas [l'installation](https://www.rust-lang.org/fr/tools/install)
le site rust-lang.org la décrit

elle ce fait par la commande suivante que l'on trouvera sur [rustup.rs](https://rustup.rs/)

> curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh


La commande installe la chaîne d'outils Rust incluant
 * **rustc** le compilateur,
 * **cargo** le système de construction et le gestionnaire de paquets de Rust
 * **rustup**  est un installeur pour le language Rust .


 la commande **rustup update** mettra à jour le compilateur et les outils

## Les bases de la programmation en Rust

###  Le premier programme

Guillaume Gomez nous [propose](https://blog.guillaume-gomez.fr/Rust/1/3) la création d'un **Hello world classique**

Nous verrons ensuite qu'il exsite dans **rust** une proposition d'organisation des projets

### les variables, conditions et pattern matching*

Rust est un langage typé.

Voici une liste des différents types de base (aussi appelés "primitifs") disponibles :

    i8 : un entier signé de 8 bits
    i16 : un entier signé de 16 bits
    i32 : un entier signé de 32 bits
    i64 : un entier signé de 64 bits
    i128 : un entier signer de 128 bits
    u8 : un entier non-signé de 8 bits
    u16 : un entier non-signé de 16 bits
    u32 : un entier non-signé de 32 bits
    u64 : un entier non-signé de 64 bits
    u128 : un entier non-signé de 128 bits
    f32 : un nombre flottant de 32 bits
    f64 : un nombre flottant de 64 bits
    str (on va y revenir plus loin dans ce chapitre)
    slice (on va y revenir plus loin dans ce chapitre)

Le point le plus important étant que les variables sont des constantes sauf si elles sont déclarées comme **mutable**


#### conditions
IF cond { } ElSE {}

Exemples :
  > let age: i32 = 17;
  >
  if age >= 18 {
      println!("majeur !");
  } else {
      println!("mineur !");
  }

**Noter:** que tous les exemples peuvent être testé en [ligne](https://play.rust-lang.org/?version=stable&mode=debug&edition=2015)

[run](https://play.rust-lang.org/?code=fn+main%28%29+%7B%0A++++let+age%3A+i32+%3D+17%3B%0A++++%0A++++if+age+%3E%3D+18+%7B%0A++++++++println%21%28%22majeur+%21%22%29%3B%0A++++%7D+else+%7B%0A++++++++println%21%28%22mineur+%21%22%29%3B%0A++++%7D%0A%7D%0A)

####  filtrage par motif"

syntaxe :

```
let my_string = "hello";

match my_string {
    "bonjour" => {
        println!("français");
    }
    "ciao" => {
        println!("italien");
    }
    "hello" => {
        println!("anglais");
    }
    "hola" => {
        println!("espagnol");
    }
    _ => {
        println!("je ne connais pas cette langue...");
    }
}
````

### Les fonctions
Il n'y a pas d'ordre pour écrire les fonctions
* Sachez juste que les déclarations de fonctions ne sont pas nécessaires avant leur appel en Rust

syntaxe :
> fn addition(nb1: i32, nb2: i32) -> i32 {
    return nb1 + nb2;
}

exemple :

* Version Rust
> fn main() {
>
>    println!("1 + 2 = {}", addition(1, 2));
}
>
> fn addition(nb1: i32, nb2: i32) -> i32 {
    return nb1 + nb2;
}


*  version python3
>def addition ( x, y ) :
   return x+ y
>      
> print(addition(1,2))


**Noter** : Tous les appels ayant un '!' ne sont pas des fonctions, mais des macros.

### Les expressions

À [Lire](https://blog.guillaume-gomez.fr/Rust/1/7) attentivement


### Les boucles

C'est plus classique ;-)

* **while**

* **loop**

* **for**

Quoique :

* **Énumération**
* **boucles nommées**
