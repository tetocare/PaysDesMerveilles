# 📘 Mémo Git – Travailler proprement avec GitHub

Ce mémo est destiné à moi-même (et aux partenaires éventuels), pour ne pas oublier les bonnes pratiques Git.  
Il résume les manipulations essentielles pour travailler en ligne de commande, **dans les deux sens** : de mon ordi vers GitHub et inversement.

---

## 🔄 1. Mettre à jour le dépôt local depuis GitHub (pull)

À faire **avant de commencer à travailler**, **et aussi chaque fois que j’ai modifié quelque chose via le site web GitHub** :

```bash
git pull origin main
```

🧠 _Récupère la version la plus récente du dépôt depuis GitHub dans mon dossier local.  
Évite les conflits plus tard lors du `push`._

---

## ✏️ 2. Travailler localement

Je modifie, ajoute ou supprime des fichiers dans mon dossier local (comme d’habitude).  
Quand je veux sauvegarder ces changements dans Git :

```bash
git add .
```

🧠 _Ajoute tous les fichiers modifiés au suivi de Git (prépare le commit)_

```bash
git commit -m "Message clair qui résume ce que j’ai fait"
```

🧠 _Crée une version enregistrée de mon travail (comme un point de sauvegarde)_

---

## 🚀 3. Envoyer mes modifications sur GitHub (push)

Quand mon travail est prêt à être partagé (ou juste sauvegardé à distance) :

```bash
git push origin main
```

🧠 _Envoie mon commit local vers GitHub (visible en ligne)_

---

## 🌱 4. Initialiser un nouveau dépôt depuis mon ordi

Si je crée un projet sur mon ordi et que je veux le publier sur GitHub :

```bash
git init
```
🧠 _Démarre un dépôt Git dans mon dossier_

```bash
git remote add origin git@github.com:mon-utilisateur/mon-depot.git
```
🧠 _Lie mon dossier local à un dépôt vide que j’ai créé sur github.com_

```bash
git add .
git commit -m "Initial commit"
git branch -M main
git push -u origin main
```
🧠 _Ajoute tout, crée un premier commit, pousse vers GitHub_

---

## 📌 Conseils

- Toujours faire un `git pull` avant de commencer
- Toujours faire un `git pull` si j’ai modifié un fichier depuis l’interface web de GitHub
- Toujours faire un `git add .` + `commit` avant de faire `git push`
- Écrire un message de commit **utile** (ex: "Ajout README pour python-sqlite")
- Ne jamais paniquer : Git garde tout en mémoire 😉

---

_Conçu pour le Pays des Merveilles 🐇_
