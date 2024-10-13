# LaTeX_Tours

## Introduction

Bienvenue dans ce dépôt, qui a été spécialement conçu pour les étudiants du Master de Physique Théorique de l'Université de Tours. 

Ce dépôt contient un modèle de document LaTeX, optimisé pour la rédaction de rapports de stage. Vous y trouverez :

- Une mise en page sérieuse et conforme aux attentes académiques.
- Une variété de commandes LaTeX utiles pour enrichir votre rapport, telles que l'insertion d'équations, de tableaux, et de figures.
- Des instructions détaillées pour l'installation des outils nécessaires et la compilation du document.

Ce fichier README vous guidera à travers les étapes d'installation de l'environnement LaTeX, l'utilisation d'éditeurs recommandés, et les bonnes pratiques pour optimiser votre expérience de rédaction. Que vous soyez novice en LaTeX ou déjà familiarisé avec cet outil, ce dépôt vous aidera à produire un rapport de stage de haute qualité.

## Table des Matières

1. [Structure du dépôt](#structure-du-dépôt)
2. [Prérequis](#prérequis)
3. [Installation](#installation)
   - [Installation sous Windows avec WSL](#1-installation-sous-windows-avec-wsl)
   - [Installation sous Windows sans WSL](#2-installation-sous-windows-sans-wsl)
   - [Installation sous Linux](#3-installation-sous-linux)
   - [Installation sous macOS](#4-installation-sous-macos)
   - [Installation de makefile](#5-installation-de-makefile)
4. [Compilation du document avec LaTeX Workshop dans VS Code](#compilation-du-document-avec-latex-workshop-dans-vs-code)
5. [Bonnes pratiques avec LaTeX Workshop dans VS Code](#bonnes-pratiques-avec-latex-workshop-dans-vs-code)
6. [Dépannage](#dépannage)
7. [Contribuer au dépôt](#contribuer-au-dépôt)

## Structure du dépôt

Ce dépôt est organisé de manière à faciliter la navigation et l'utilisation des ressources LaTeX. Voici un aperçu de la structure des dossiers et des fichiers :

```
LaTeX_Tours/
├── README.md                # Fichier contenant des informations sur le dépôt, des instructions d'installation et des bonnes pratiques.
├── .gitignore               # Fichier indiquant les fichiers et dossiers à ignorer par Git lors des commits.
└── Canva_Universite/        # Dossier principal contenant tous les fichiers liés au projet LaTeX.
    ├── logos/               # Dossier contenant les logos utilisés dans le document.
    │   └── [logos utilisés dans le document]  # Fichiers image des logos .
    ├── images/              # Dossier contenant les images nécessaires pour le document.
    │   └── [images nécessaires pour le document] # Fichiers image pour la production du rapport.
    ├── Canva_Tours.pdf      # Fichier PDF généré à partir du code LaTeX, contenant le rapport final.
    ├── Canva_Tours.tex      # Fichier source LaTeX principal du projet.
    └── references.bib       # Fichier BibTeX contenant une référence bibliographique utilisée dans le document.
```

## Prérequis

Il est nécessaire d'installer un environnement LaTeX. Vous trouverez ci-dessous les instructions pour installer LaTeX et les paquets requis sur les systèmes suivants : [Installation](#installation).

1. Windows (avec ou sans WSL) [Instructions](#installation-sous-windows-avec-wsl)
2. Linux [Instructions](#installation-sous-linux)
3. macOS [Instructions](#installation-sous-macos)

Il est recommandé d'utiliser l'éditeur de code **Visual Studio Code (VS Code)** avec l'extension **LaTeX Workshop** pour une expérience de développement optimisée (plus de détails à ce sujet [ici](#compilation-du-document-avec-latex-workshop-dans-vs-code)).

## Installation

Dans cette section, vous trouverez les instructions pour installer LaTeX et les outils nécessaires sur différents systèmes d'exploitation. LaTeX fonctionne en utilisant un éditeur de texte pour écrire votre document, un compilateur pour convertir ce code source en un fichier PDF, et souvent plusieurs packages pour étendre ses fonctionnalités. Que vous utilisiez Windows, Linux ou macOS, des étapes claires et simples vous guideront à travers le processus d'installation de LaTeX, des éditeurs de texte, ainsi que des dépendances requises. À la fin de cette section, nous aborderons l'installation de **make**, qui est nécessaire pour certaines fonctionnalités avancées sur toutes les distributions. En cas de **problème** des pistes sont proposées dans la section [**Dépannage**](#dépannage).

### 1. Installation sous Windows avec WSL

Si vous utilisez Windows Subsystem for Linux (WSL), vous pouvez installer LaTeX comme sur une distribution Linux (par exemple Ubuntu) à l'intérieur de WSL.

#### Étapes :

1. Installez WSL si ce n'est pas déjà fait :
   - Ouvrez PowerShell en mode Administrateur et exécutez la commande suivante :
     ```
     wsl --install
     ```
   - Suivez les instructions pour installer Ubuntu (ou une autre distribution de votre choix).

2. Ouvrez votre terminal WSL et exécutez les commandes suivantes pour installer LaTeX et les outils nécessaires :
   ```
   sudo apt-get update
   sudo apt-get install texlive texlive-latex-extra texlive-math-extra texlive-fonts-recommended latexmk texmaker
   ```

3. Installez Visual Studio Code et l'extension LaTeX Workshop :
    - Téléchargez VS Code depuis ce lien.
    - Installez l'extension LaTeX Workshop depuis le Marketplace intégré dans VS Code.

### 2. Installation sous Windows sans WSL

Si vous préférez ne pas utiliser WSL, vous pouvez installer LaTeX directement sous Windows à l'aide de MiKTeX.

#### Étapes :

1. Téléchargez et installez **MiKTeX** depuis [ce lien](https://miktex.org/download).

2. Pendant l'installation, choisissez l'option d'installer les paquets à la demande (on-the-fly), afin que les paquets nécessaires soient automatiquement téléchargés lors de la compilation.

3. Téléchargez et installez **TeXmaker** (un éditeur LaTeX) depuis [ce lien](https://www.xm1math.net/texmaker/).

4. Installez **Visual Studio Code** et l'extension **LaTeX Workshop** :
   - Téléchargez VS Code depuis [ce lien](https://code.visualstudio.com/).
   - Installez l'extension **LaTeX Workshop** depuis le Marketplace intégré dans VS Code.

5. Ouvrez VS Code et configurez-le pour utiliser MiKTeX :
   - Ajoutez MiKTeX au PATH lors de l'installation, ou configurez-le manuellement dans les paramètres de LaTeX Workshop.

### 3. Installation sous Linux

Sous Linux, l'installation est simple grâce au gestionnaire de paquets de votre distribution.

#### Étapes :

1. Ouvrez un terminal et exécutez les commandes suivantes pour installer LaTeX et les outils nécessaires :
   ```
   sudo apt-get update
   sudo apt-get install texlive texlive-latex-extra texlive-math-extra texlive-fonts-recommended latexmk texmaker
   ```

2. Installez Visual Studio Code et l'extension LaTeX Workshop :
    - Téléchargez VS Code depuis ce lien.
    - Installez l'extension LaTeX Workshop depuis le Marketplace intégré dans VS Code.

### 4. Installation sous macOS

Sous macOS, l'installation de LaTeX se fait généralement à l'aide de **MacTeX**.

#### Étapes :

1. Téléchargez et installez **MacTeX** depuis [ce lien](https://www.tug.org/mactex/).

2. MacTeX inclut tous les paquets LaTeX nécessaires, ainsi que **TeXShop**, un éditeur LaTeX. Vous pouvez utiliser cet éditeur ou installer **TeXmaker** si vous le préférez :
   - Téléchargez TeXmaker depuis [ce lien](https://www.xm1math.net/texmaker/).

3. Installez **Visual Studio Code** et l'extension **LaTeX Workshop** :
   - Téléchargez VS Code depuis [ce lien](https://code.visualstudio.com/).
   - Installez l'extension **LaTeX Workshop** depuis le Marketplace intégré dans VS Code.

### 5. Installation de `makefile`

Pour la génération de tables d'acronymes et autres fonctions avancées, il est souvent nécessaire d'installer **make**. Voici comment procéder sur chaque système d'exploitation :

- **Windows (avec WSL)** : `make` est inclus par défaut dans WSL. Il suffit d’installer un environnement comme Ubuntu via le Microsoft Store.
  
- **Windows (sans WSL)** : Si vous utilisez MiKTeX, `make` n'est pas nécessaire. Pour des fonctionnalités avancées, envisagez d’installer Cygwin ou MinGW, qui incluent `make`.

- **Linux** : La plupart des distributions incluent `make` par défaut. Si ce n'est pas le cas, installez-le via votre gestionnaire de paquets :
  ```
  sudo apt-get install make
  ```

- **macOS** : Installez `make` en utilisant Homebrew :
  ```
  brew install make
  ```


## Compilation du document avec LaTeX Workshop dans VS Code

L'extension **LaTeX Workshop** pour **Visual Studio Code (VS Code)** simplifie le processus de compilation des documents LaTeX et fournit plusieurs outils pour optimiser votre flux de travail.

### 1. Compilation automatique avec LaTeX Workshop

Pour compiler votre document LaTeX dans **VS Code** avec **LaTeX Workshop**, plusieurs options s'offrent à vous :

- **Utilisation de l'icône de flèche verte** : Une fois votre fichier `.tex` ouvert dans **VS Code**, vous pouvez lancer la compilation en cliquant sur l'icône de **flèche verte** en haut de l'interface. Cette icône lance la compilation rapide de votre document, générant automatiquement le PDF.

- **Raccourci clavier** : Vous pouvez également utiliser `Ctrl + Alt + B` pour lancer la compilation rapide.

- **Compilation automatique à la sauvegarde** : Chaque fois que vous enregistrez votre fichier `.tex` en appuyant sur `Ctrl + S`, **LaTeX Workshop** effectue automatiquement une compilation du document pour que votre PDF soit mis à jour avec les dernières modifications.

Le mode de compilation rapide gère automatiquement plusieurs passes (grâce à `latexmk`) pour assurer la génération correcte des éléments complexes comme les tables des matières, les acronymes ou les bibliographies.

### 2. Compilations successives pour des éléments complexes (table des matières, acronymes, etc.)

Lorsque vous travaillez avec des éléments LaTeX complexes tels que :

- Une **table des matières**
- Une **table d'acronymes**
- Des **références croisées**
- Une **bibliographie**

LaTeX nécessite souvent plusieurs compilations pour générer ces éléments correctement. Voici les différentes passes que LaTeX effectue lors de la compilation :

- **Première compilation :** Génère le document principal, mais la table des matières ou les acronymes peuvent ne pas apparaître immédiatement.
- **Deuxième compilation :** Met à jour ces éléments à partir des fichiers auxiliaires générés lors de la première compilation (comme `.toc` pour la table des matières).
- **Troisième compilation (si nécessaire) :** Finalise les éléments comme la table des matières et les acronymes.

**LaTeX Workshop** prend en charge ces compilations successives automatiquement via `latexmk`, donc généralement, vous n'avez pas à vous en préoccuper.

### 3. Exécution manuelle de la commande `makeglossaries` pour mettre à jour la table d'acronymes

Dans certains cas, si votre projet utilise une **table d'acronymes** avec le package **`acronym`**, il est nécessaire d'exécuter la commande `makeglossaries` pour générer ou mettre à jour la table des acronymes après modification.

Voici comment faire cela dans **VS Code** :

1. **Ouvrez le terminal intégré dans VS Code** en utilisant `Ctrl + \`` (backtick).
2. **Exécutez la commande `makeglossaries`** pour générer ou mettre à jour la table des acronymes :
   ```
   makeglossaries Canva_Tours
   ```
   Cette commande générera la table d’acronymes dans votre document. Après cela, il vous suffit de recompiler le document avec LaTeX Workshop pour intégrer les modifications dans le PDF final.

## Bonnes pratiques avec LaTeX Workshop dans VS Code

Voici quelques fonctionnalités supplémentaires et bonnes pratiques qui vous aideront à optimiser votre utilisation de **VS Code** avec **LaTeX Workshop**.

### 1. Navigation entre le code source et le PDF avec `Ctrl + Clic`

Grâce à **SyncTeX** intégré dans **LaTeX Workshop**, vous pouvez facilement synchroniser votre fichier `.tex` avec le PDF généré. Cela permet de naviguer rapidement entre le code source et le rendu PDF.

- **Depuis le PDF :** En cliquant avec `Ctrl + clic` dans le PDF, vous serez redirigé vers la ligne de code correspondante dans le fichier `.tex`.

### 2. Commande `Alt + Z` : Activation du retour à la ligne automatique

Lorsque vous travaillez sur des paragraphes longs dans un fichier `.tex`, il peut être utile d'activer le retour à la ligne automatique pour faciliter la lisibilité sans affecter le contenu du fichier.

- **Raccourci :** Appuyez sur `Alt + Z` dans **VS Code** pour activer ou désactiver le retour à la ligne automatique.

Cela vous permet de voir l'intégralité du texte sans avoir à faire défiler horizontalement.

### 3. Utilisation d'un fichier `.gitignore`

Lors de la compilation d'un document LaTeX, de nombreux fichiers auxiliaires (comme `.aux`, `.log`, `.toc`, etc.) sont générés. Ces fichiers ne doivent pas être inclus dans votre dépôt Git, car ils sont temporaires et inutiles pour d'autres utilisateurs.

Il est recommandé d'utiliser un fichier **`.gitignore`** pour exclure ces fichiers du suivi Git. Vous pouvez trouver un exemple de fichier `.gitignore` adapté aux projets LaTeX dans ce dépôt.

## Dépannage

Si vous rencontrez des problèmes lors de l'installation ou de l'utilisation de LaTeX, voici quelques conseils et ressources qui peuvent vous aider :

### 1. Installation de WSL sur Windows

Si vous choisissez d'installer LaTeX via Windows Subsystem for Linux (WSL) et que vous rencontrez des difficultés, assurez-vous d'avoir suivi les étapes d'installation correctement. Voici un lien vers la documentation officielle de Microsoft sur l'installation de WSL : [Installer WSL sur Windows](https://docs.microsoft.com/fr-fr/windows/wsl/install) et [Étapes d’installation manuelle pour les versions antérieures de WSL](https://learn.microsoft.com/fr-fr/windows/wsl/install-manual).

- **Note :** Dans certains cas, il peut être nécessaire d'activer la virtualisation dans le BIOS de votre ordinateur pour que WSL fonctionne correctement. Consultez le manuel de votre carte mère ou le site Web du fabricant pour des instructions sur l'activation de la virtualisation.

### 2. Problèmes d'installation de MiKTeX

Si vous avez des difficultés à installer MiKTeX sur Windows, vérifiez que vous avez téléchargé la dernière version depuis le site officiel : [Télécharger MiKTeX](https://miktex.org/download). Si vous avez des problèmes spécifiques, vous pouvez consulter la section FAQ de MiKTeX : [FAQ MiKTeX](https://miktex.org/faq).

### 3. Erreurs lors de la compilation

Si vous rencontrez des erreurs lors de la compilation de votre document LaTeX dans VS Code, vérifiez les points suivants :

- Assurez-vous que tous les paquets requis sont installés. Si vous utilisez MiKTeX, activez l'option d'installation automatique des paquets.
- Consultez le panneau de sortie de LaTeX Workshop pour des messages d'erreur détaillés.
- Recherchez les messages d'erreur spécifiques en ligne pour des solutions. La communauté LaTeX est active, et il y a de fortes chances que d'autres utilisateurs aient rencontré le même problème.

### 4. Autres ressources utiles

- Pour des questions générales sur LaTeX, consultez le site [TeX Stack Exchange](https://tex.stackexchange.com/), où vous pouvez poser des questions et trouver des réponses de la communauté LaTeX.
- Des tutoriels et des guides supplémentaires peuvent être trouvés sur [Overleaf](https://www.overleaf.com/learn), une plateforme en ligne populaire pour LaTeX.
- Si vous avez des questions ou des problèmes spécifiques, n'hésitez pas à dialoguer avec [ChatGPT](https://chatgpt.com/).

## Contribuer au dépôt

Ce dépôt a été conçu pour les étudiants et les enseignants du Master de Physique Théorique de l'Université de Tours. Pour contribuer à ce projet :

1. **Forkez le dépôt** : Cliquez sur "Fork" en haut à droite. [En savoir plus](https://docs.github.com/en/get-started/quickstart/fork-a-repo).
  
2. **Clonez votre fork** : [Détails ici](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository).
   ```
   git clone https://github.com/votre_nom_utilisateur/LaTeX_Tours.git
   ```

3. **Créez une nouvelle branche** : [Voir les branches](https://docs.github.com/en/repositories/creating-and-managing-branches/creating-and-deleting-branches).
   ```
   git checkout -b nom_de_votre_branche
   ```

4. **Apportez vos modifications** : Modifiez les fichiers nécessaires.

5. **Committez vos changements** : [En savoir plus sur les commits](https://docs.github.com/en/get-started/using-git/committing-changes-to-your-repository).
   ```
   git add .
   git commit -m "Description des modifications"
   ```

6. **Poussez vos changements** : [Voir comment pousser](https://docs.github.com/en/get-started/using-git/pushing-changes-to-your-remote-repository).
   ```
   git push origin nom_de_votre_branche
   ```

7. **Créez une Pull Request** : Cliquez sur "New Pull Request" sur votre fork. [Instructions ici](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/creating-a-pull-request).


### Auteur Initial

Ce dépôt a été créé par **Antoine FAYOLLE**, ancien étudiant au Master de Physique Théorique - Modèles Non Linéaires à l'Université de Tours. Vous pouvez le trouver sur GitHub à l'adresse [@fayollea](https://github.com/FAYOLLEAntoine).

Merci pour votre aide !