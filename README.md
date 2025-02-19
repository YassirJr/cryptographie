# 🛠️ Travaux Pratiques de Cryptographie

## 📌 Sommaire

- [TP1 - Utiliser des algorithmes de chiffrement classiques et modernes](#tp1)
- [TP2 - Chiffrer et déchiffrer des données avec OpenSSL](#tp2)

---

## 🔐 TP1

### ✨ Partie 1 : Algorithme de chiffrement classique (Caesar)

- **Tâches :**
    - Utilisez l'algorithme **César** pour **chiffrer** un message texte.
    - **Déchiffrez** le texte chiffré avec **César**.
    - Modifiez les paramètres de l'algorithme.

📌 **Démo :**  

https://github.com/user-attachments/assets/a9de1655-66e1-4a24-9099-3f74dcfbe116

<img width="800" alt="Screenshot" src="https://github.com/user-attachments/assets/135383c6-75f3-46ee-8421-d06618a81210" />

---

### ⚡ Partie 2 : Algorithme de chiffrement symétrique moderne (AES)

- **Tâches :**
    - Utilisez **AES** pour **chiffrer** un message texte.
    - **Déchiffrez** un message texte avec **AES**.

📌 **Démo :**  

https://github.com/user-attachments/assets/ad88922a-f006-439f-b8bc-0cf8b9b36ba5

---

### 🔑 Partie 3 : Algorithme de chiffrement asymétrique moderne (RSA)

- **Tâches :**
    - Utilisez **RSA** pour **chiffrer** un fichier texte.
    - **Déchiffrez** un fichier texte avec **RSA**.

📌 **Démo :**  

https://github.com/user-attachments/assets/cab3207e-95bc-4019-9067-401f760bdc71

---

## 🛡️ TP2

### 🔹 Partie 1 : Chiffrer des messages avec OpenSSL

- **Tâche :**
    - **Chiffrement** d'un fichier texte avec **OpenSSL**.

- **Questions et réponses :**
    - **e - (Documenter le mot de passe) :** `yassirjr`
    - **f - (Le contenu du fichier message.enc s'affiche-t-il correctement ?) :**
        - Non, car il est chiffré. Il apparaît sous forme de caractères illisibles ou de données binaires.
    - **h - (Est-ce que message.enc s'affiche correctement maintenant ?) :**
        - Oui, sous forme de texte encodé en **Base64**, mais il reste **chiffré**. Pour voir le contenu original, il
          faut **le déchiffrer** avec OpenSSL et le mot de passe approprié.
    - **h - (Pouvez-vous imaginer un avantage à ce que message.enc soit codé en Base64 ?) :**
        - L'encodage en Base64 du fichier `message.enc` facilite le transfert des données binaires via des systèmes
          textuels comme les e-mails ou JSON. Il évite les problèmes d'affichage dans les terminaux et est
          universellement compatible avec la plupart des outils et langages. De plus, il permet une intégration simple
          dans des formats textuels et une détection d'erreurs plus aisée. En résumé, Base64 rend les données chiffrées
          plus pratiques à manipuler et à transférer.

### 🔹 Partie 2 : Déchiffrement avec OpenSSL

- **Tâche :**
    - **Déchiffrement** du fichier `message.enc` avec **OpenSSL**.

- **Questions et réponses :**
    - **i - (La lettre a-t-elle été correctement déchiffrée ?) :**
        - Oui, si le mot de passe saisi est correct et que le fichier `message.enc` n'a pas été altéré, la lettre sera
          correctement déchiffrée. Le contenu original sera enregistré dans le fichier `decrypted_letter.txt`, et vous
          pourrez le vérifier en utilisant la commande `cat decrypted_letter.txt`.
    - **j - (La commande utilisée pour déchiffrer contient également une option -a. Pouvez-vous expliquer pourquoi ?) :**
        - L'option `-a` indique à OpenSSL que le fichier chiffré (`message.enc`) est encodé en **Base64**. Sans cette
          option, OpenSSL supposerait que le fichier est en format binaire brut, ce qui entraînerait une erreur de
          déchiffrement. L'option `-a` permet donc de traiter correctement les fichiers encodés en **Base64**.


---
