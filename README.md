# TP Android : Introduction à JNI et aux Fonctions Natives

## Présentation

Cette application Android développée en Java démontre l’intégration du code natif dans une application mobile grâce à Java Native Interface (JNI).

Le projet combine du code Java Android avec des fonctions natives afin d’illustrer comment exploiter des performances natives et renforcer certaines fonctionnalités sensibles.

---

# Objectifs du TP

Ce projet permet de découvrir :

- le fonctionnement de JNI ;
- l’intégration du code natif dans Android ;
- le chargement des bibliothèques natives ;
- l’appel de fonctions C/C++ depuis Java ;
- la sécurisation simple contre certains environnements suspects.

---

# Fonctionnalités implémentées

L’application fournit plusieurs fonctionnalités natives :

## Message provenant du code natif

Une fonction native retourne une chaîne de caractères générée côté natif.

Exemple :

- communication Java ↔ code natif
- récupération d’informations natives

---

## Calcul Factoriel Natif

L’utilisateur peut exploiter une fonction native permettant :

- calculer un factoriel ;
- transférer les paramètres Java vers le code natif ;
- récupérer les résultats calculés.

---

## Vérification d’environnement

L’application effectue une vérification simple afin de détecter certains environnements potentiellement suspects.

Comportement :

- validation de l’environnement ;
- désactivation des fonctionnalités sensibles ;
- affichage d’un état de sécurité.

---

# Architecture du projet

```text
com.example.lab24

├── MainActivity.java
│
├── native
│   └── native-lib
│
├── res
│   ├── layout
│   └── values
│
└── Gradle Configuration
```

---

# Technologies utilisées

| Technologie | Utilisation |
|------------|------------|
| Java | Interface Android |
| JNI | Communication Java / Natif |
| Android Studio | Développement |
| C / C++ | Fonctions natives |
| NDK | Compilation native |

---

# Fonctionnement général

## Étape 1 : Chargement de la bibliothèque native

L’application charge automatiquement la bibliothèque :

```java
System.loadLibrary("native-lib");
```

---

## Étape 2 : Déclaration des méthodes natives

Les fonctions natives sont exposées sous forme de méthodes Java.

Exemples :

- récupération de texte natif ;
- calcul ;
- contrôle de sécurité.

---

## Étape 3 : Exécution native

Lorsque l’utilisateur lance l’application :

1. Android charge la bibliothèque native ;
2. les fonctions natives deviennent accessibles ;
3. l’application récupère les résultats.

---

# Interface utilisateur

L’interface affiche :

- l’état de sécurité ;
- les informations provenant du code natif ;
- les résultats calculés.

L’objectif principal est de visualiser simplement les interactions Java ↔ Natif.

---

# Résultats obtenus

Fonctionnalités validées :

- ✅ Chargement d’une bibliothèque native
- ✅ Appels JNI fonctionnels
- ✅ Échange de données Java / Natif
- ✅ Calcul effectué côté natif
- ✅ Vérification simple de sécurité
- ✅ Intégration Android + NDK

---

# Concepts étudiés

Durant ce TP, les notions suivantes sont abordées :

- Java Native Interface
- Android NDK
- Bibliothèques partagées
- Appels natifs
- Sécurité logicielle basique
- Communication inter-langages

---

# Conclusion

Ce projet constitue une introduction pratique au développement Android hybride combinant Java et code natif afin de mieux comprendre le fonctionnement interne des applications Android.

---

# Auteur

AIT HMAD OUSSAMA
