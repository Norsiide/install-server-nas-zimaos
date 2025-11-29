<p align="center"><img src="https://github.com/Norsiide/install-server-nas-zimaos/blob/main/img/zimaos.png" width="auto" alt="norsiide"></p>

# Installation d’un homelab sous ZimaOS

* **ZimaOS** est un système de type NAS (Network Attached Storage) open source, basé sur Debian, conçu pour être simple d’utilisation et accessible à tous.


> **PS :** Cette configuration est basée sur mon propre serveur, que je partage publiquement afin de vous aider dans l’installation. Certaines informations peuvent manquer ; n’hésitez pas à me contacter pour que je les ajoute et facilite ainsi l’installation pour les prochains utilisateurs.

---

### Liens utiles

* **Discord** : [Rejoins notre communauté](https://discord.gg/EV3fAhFZJT)
* **Site web** : [Plus d'informations](https://norsiide.be)
* **ZimaOS** : [Lien vers ZimaOS](https://www.zimaspace.com/zimaos)

---

Voici **un tuto clair, simple et complet** pour **installer ZimaOS** sur n’importe quel PC, mini-PC ou serveur (x86-64).
Je te donne les étapes **de A à Z**, comme si tu le faisais pour la première fois.

---

# 🚀 TUTORIEL COMPLET : Installer ZimaOS

## ✔️ Prérequis

### Matériel

* Un PC compatible **x86-64** (même un vieux mini-PC)
* Une **clé USB de 4 Go ou +**
* Un disque (HDD/SSD) pour installer ZimaOS

### Logiciel

* Un logiciel pour créer la clé USB bootable :

  * **Rufus** 👉 [Telecharge rufus](https://rufus.ie/fr/)(Windows)
  * **BalenaEtcher** (Windows, macOS, Linux)
  * **Ventoy** (si tu veux)

---

# 1️⃣ Télécharger ZimaOS

1. Va sur : 👉 [telecharge l'img de ZimaOS](https://www.zimaspace.com/zimaos/download)
2. Télécharge la **version img** pour PC
3. Enregistre-la sur ton ordinateur

---

# 2️⃣ Créer la clé USB bootable

### 🟦 Méthode avec RUFUS (Windows)

1. Branche ta clé USB
2. Ouvre **Rufus**
3. Sélectionne :

   * **Périphérique** : ta clé USB
   * **Sélection de boot** : l’image ISO de ZimaOS
4. Laisse les options par défaut (GPT / UEFI généralement)
5. Clique **Démarrer**

---

# 3️⃣ Démarrer sur la clé USB

Sur le PC où tu veux installer ZimaOS :

1. Branche la clé
2. Allume le PC
3. Ouvre le **boot menu** (selon la marque) :

| Marque   | Touche   |
| -------- | -------- |
| HP       | F9       |
| Dell     | F12      |
| Lenovo   | F12      |
| Acer     | F12      |
| ASUS     | F8 / Esc |
| MSI      | F11      |
| Gigabyte | F12      |

4. Choisis ta **clé USB**

Tu vas arriver sur le menu d’installation de ZimaOS.

---

# 4️⃣ Lancer l’installation de ZimaOS

1. Quand le menu apparaît, sélectionne :
   👉 **Install ZimaOS**
2. Choisis la langue (si FR dispo, sinon EN)
3. Sélectionne le **disque où installer ZimaOS**
   ⚠️ **Attention** : le disque sera formaté
4. L’installeur copie les fichiers
5. Le PC redémarre automatiquement

Tu peux retirer la clé USB à ce moment-là.

---

# 5️⃣ Faire la configuration initiale

Au premier démarrage :

1. ZimaOS te demande un **nom d’appareil** (ex : *mon-nas*)
2. Tu crées un **compte local** :

   * Nom d’utilisateur
   * Mot de passe
3. Tu configures le **réseau** (Ethernet recommandé)
4. Tu arrives sur le **dashboard web** 👍

---

# 6️⃣ Accéder à ZimaOS depuis ton navigateur

Depuis un autre appareil (PC / téléphone) connecté au même réseau :

1. Ouvre ton navigateur
2. Tape l’adresse indiquée à l’écran du serveur, généralement :

```
http://zimaos.local
```

ou

```
http://192.168.x.x
```

(donné par ZimaOS)

Tu arrives sur l’interface principale.
---

# 7️⃣ Configurer le NAS

À faire juste après l’installation :

### 📁 1. Créer ton “storage pool”

* Choisir un ou plusieurs disques
* Configurer RAID (optionnel)
* Formatage automatique

### 👤 2. Ajouter des utilisateurs (si besoin)

* Famille
* Amis
* Accès limité aux dossiers

### ☁️ 3. tu doit reglé ton interface reseau (pour que l'ip de change pas au demmarage du serveur)

* IP : 192.168.1.100 (l'adresse ip que tu souhaite utilise pour le serveur)
* Masque de sous-réseau : 255.255.255.0
* Adresse de la passerelle : 192.168.1.1 (ip de votre routeur)
* DNS : 1.1.1.1 (vous pouvez choisir votre serveur dns exemple metre adguard)

<p align="center"><img src="https://github.com/Norsiide/install-server-nas-zimaos/blob/main/img/ethernet.png" width="auto" alt="norsiide"></p>

### ☁️ 4. Installer des apps

Tu as un **App Center** (type Store) pour ajouter :

* Plex / Jellyfin (serveur multimédia)
* Nextcloud / FileBrowser
* Serveur de téléchargement
* Serveur photo
* Docker / Portainer
* etc.

### 🔄 4. Configurer les sauvegardes

* Vers disque USB
* Vers cloud
* Vers autre serveur

---

# 8️⃣ ZimaOS est installé !

Tu peux maintenant :

* centraliser tes fichiers
* créer ton cloud privé
* héberger des services
* installer des apps supplémentaires
* accéder à tout depuis ton téléphone / PC

---

