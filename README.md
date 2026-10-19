# 🌐 TrameX · Studio Réseau — V2.5

### Simulateur pédagogique de réseaux informatiques, systèmes et cybersécurité

**Construire, comprendre, simuler et dépanner un réseau informatique directement dans un navigateur.**

**TrameX · Studio Réseau** est une application pédagogique interactive, entièrement en français, conçue pour faciliter l'apprentissage des réseaux informatiques, des systèmes et de la cybersécurité.

Elle s'adresse notamment aux :

- 🎓 **Bac Pro CIEL** — Cybersécurité, Informatique et réseaux, Électronique
- 🎓 **BTS CIEL** — Option Informatique et Réseaux (IR)
- 🎓 **BTS SIO** — Options SISR et SLAM
- 🎓 **BUT Réseaux & Télécommunications**
- 🎓 **Licences professionnelles et écoles d'informatique**
- 🎓 **Centres de formation et organismes professionnels**

**Une approche visuelle, progressive et pratique pour apprendre les réseaux autrement.**

---

## ✨ Pourquoi choisir TrameX ?

### 🖥️ Une application accessible

- **Zéro installation sur les postes élèves :** fonctionnement directement dans un navigateur web.
- **Déploiement flexible :** serveur local, NAS, XAMPP ou hébergement PHP compatible.
- **Interface en français :** conçue pour l'apprentissage et la formation.
- **Prise en main rapide :** équipements courants préconfigurés.
- **Utilisation pédagogique :** démonstrations, travaux pratiques, exercices et évaluations.
- **Version Windows :** application de bureau avec installateur dédié.

### 🔌 Construire librement son réseau

Les étudiants peuvent créer leurs propres architectures en plaçant et en reliant différents équipements.

**14 types d'équipements simulés :**

- 💻 Ordinateur Windows ou Linux
- 🖥️ Serveur
- 📱 Smartphone
- 📱 Tablette
- 🔀 Switch administrable
- 🔌 Hub
- 🌐 Routeur
- 📡 Borne Wi-Fi
- 📶 Relais Wi-Fi
- 🏠 Box Internet
- ☁️ Nuage Internet
- ⚡ Adaptateur CPL
- ☎️ Téléphone IP
- 🖨️ Imprimante réseau

Les équipements courants peuvent être utilisés avec leurs paramètres initiaux ou entièrement personnalisés pour les besoins du TP.

### 📡 Visualiser les échanges réseau

TrameX permet de suivre les communications entre équipements grâce à des animations de trames sur les liaisons du schéma.

Les mécanismes et protocoles représentés comprennent notamment :

- ARP
- ICMP (Ping)
- DHCP DORA
- DNS
- TCP et HTTP
- IPv4 et IPv6
- NDP et SLAAC
- Commutation Ethernet
- Routage IP

L'étudiant peut ainsi observer la différence entre un **Hub**, qui répète le signal, un **Switch**, qui utilise les adresses MAC pour commuter les trames, et un **Routeur**, qui assure le transfert entre réseaux IP.

---

# 🆕 Nouveautés — Version 2.5

## 🔬 Analyseur de Trame & Animation d'Encapsulation OSI / TCP-IP

La version **2.5 de TrameX** introduit un nouvel outil d'analyse permettant de comprendre chaque étape d'une communication réseau.

L'ancien affichage JSON brut des paquets capturés est remplacé par un **panneau visuel, interactif et pédagogique**, synchronisé avec la simulation.

L'objectif est de montrer non seulement où circulent les données, mais aussi **comment les équipements les traitent et comment elles sont encapsulées**.

### ⏱️ 1. Frise chronologique interactive des trames

Une nouvelle frise chronologique permet d'examiner les différentes étapes d'une communication.

Pour chaque saut, elle affiche :

- Le numéro de l'événement.
- Le temps simulé en millisecondes.
- Le type de trame ou de protocole.
- L'équipement émetteur.
- L'équipement récepteur.

**En cliquant sur un événement :**

- La trame correspondante est sélectionnée.
- Son contenu pédagogique est affiché.
- Le trajet correspondant est mis en évidence sur le schéma réseau.

L'étudiant peut ainsi étudier une communication étape par étape.

### 🔌 2. Animation du saut physique — Couche 1

L'analyseur représente visuellement les transmissions entre équipements.

Il précise :

- L'équipement émetteur.
- L'action réalisée par cet équipement.
- Le support physique ou radio utilisé.
- L'équipement récepteur.
- L'action réalisée à la réception.

**Supports représentés :**

| Support | Informations affichées |
|---|---|
| Ethernet | Liaison câblée et débit |
| Wi-Fi | Transmission radio et SSID |
| CPL | Courant porteur et groupe CPL |

Cette fonctionnalité permet de distinguer les différents moyens de transmission tout en conservant une lecture cohérente de la communication réseau.

### 💬 3. Explication pédagogique de chaque étape

Une nouvelle zone intitulée **« Ce qui se passe à cette étape »** explique en français les opérations effectuées pendant la simulation.

**Exemples :**

**Hub — Couche 1**

Le Hub répète le signal reçu vers les autres ports concernés, sans exploiter les adresses MAC pour déterminer le destinataire.

**Switch — Couche 2**

Le Switch analyse les adresses MAC, alimente sa table d'apprentissage et commute les trames vers les ports appropriés.

**Routeur — Couche 3**

Le Routeur traite le paquet IP, consulte sa table de routage, gère le TTL en IPv4 ou le Hop Limit en IPv6, puis prépare une nouvelle encapsulation de liaison pour le prochain saut.

**Box Internet**

La Box assure les fonctions nécessaires à la communication entre le réseau local et les autres réseaux, notamment le routage et, selon la configuration, le NAT.

**Terminal**

Un ordinateur ou un serveur réalise les opérations d'encapsulation lors de l'émission et de désencapsulation lors de la réception.

**Objectif : comprendre pourquoi les équipements réseau n'effectuent pas les mêmes opérations selon leur rôle et leur couche de fonctionnement.**

### 🪆 4. Animation de l'encapsulation — Les poupées russes

La V2.5 intègre une animation des différentes couches de données sous forme d'éléments imbriqués.

Cette représentation permet de découvrir les mécanismes d'encapsulation et de désencapsulation utilisés dans les communications réseau.

| Couche | Éléments représentés |
|---|---|
| **Couche 7 — Application** | Données applicatives |
| **Couche 4 — Transport** | TCP, UDP, ports |
| **Couche 3 — Réseau** | IPv4, IPv6, TTL et informations réseau |
| **Couche 2 — Liaison** | Ethernet, Wi-Fi, CPL, VLAN, FCS |
| **Couche 1 — Physique** | Support de transmission |

L'affichage est adapté aux protocoles concernés : tous les échanges ne contiennent pas nécessairement les mêmes couches ou en-têtes.

Les animations accompagnent notamment les scénarios suivants :

- Ping / ICMP
- ARP
- DHCP DORA
- DNS
- TCP / HTTP
- NDP / IPv6

### ▶️ 5. Amélioration des animations réseau

La version 2.5 corrige également le comportement des animations de trames sur le schéma.

**Améliorations :**

- Chaque saut est animé une seule fois de l'émetteur au récepteur.
- Les animations ne restent plus bloquées en boucle sur le dernier câble.
- La dernière trame disparaît proprement à la fin de la lecture automatique.
- Le déroulement des communications est plus lisible.

### ✅ Validation technique

**117 tests automatisés Node.js réussis** lors de la validation de cette version.

### 🎯 Objectif pédagogique de la V2.5

Permettre aux étudiants de passer d'une simple observation du déplacement des trames à une compréhension du fonctionnement des protocoles, des couches réseau et du traitement des données par chaque équipement.

---

# 🖧 Équipements et protocoles simulés

TrameX regroupe plusieurs domaines techniques dans une même interface.

| Domaine | Fonctionnalités |
|---|---|
| **Réseaux locaux** | Ethernet, Hub, Switch, apprentissage MAC |
| **VLAN** | VLAN d'accès, Trunk 802.1Q, règles VLAN |
| **Commutation avancée** | STP, EtherChannel, LACP, Port Security |
| **Routage** | Routes statiques, RIP, OSPF |
| **IPv4** | Adressage, tables de routage, NAT/PAT |
| **IPv6** | Double pile, NDP, RA, SLAAC |
| **DHCP** | Attribution automatique, réservations MAC, relais DHCP, baux T1/T2 |
| **DNS** | Zones A, TTL, délégations NS, cache, fichier Hosts |
| **Services Web** | HTTP, HTTPS, TLS, proxy inverse |
| **Systèmes et applications** | SQL, FTP, SSH, SMTP, POP3 |
| **Téléphonie** | VoIP SIP/RTP, SMS |
| **Cybersécurité** | Pare-feu stateless/stateful, VPN, filtrage |
| **Sécurité Web** | Anti-DoS, SQLi, XSS, CSRF, verrouillage anti-force-brute |
| **Connectivité** | Wi-Fi, relais Wi-Fi, CPL |

> **Note pédagogique :** TrameX modélise les mécanismes utiles à l'apprentissage. Il ne remplace pas une infrastructure de production, un laboratoire physique ou un émulateur matériel complet.

---

# 📚 30 travaux pratiques intégrés et auto-corrigés

TrameX propose **30 activités pédagogiques**, organisées autour de deux approches complémentaires.

## 🏗️ 20 TP « Partir de zéro »

L'étudiant démarre avec une feuille de travail vierge.

Chaque activité propose une **Feuille de TP** précisant :

- Les objectifs pédagogiques.
- Les équipements à installer.
- Les liaisons à réaliser.
- Les configurations attendues.
- Les tests et vérifications à effectuer.

Un bouton **« ✅ Vérifier mes objectifs du TP »** permet de contrôler automatiquement les objectifs définis dans l'activité.

### 🌐 Réseau et infrastructure — TP 01 à TP 09

1. Premier LAN commuté
2. Du Hub au Switch
3. Routage inter-LAN
4. Box Internet : NAT, DHCP et accès Internet
5. Réseau hybride Wi-Fi et CPL
6. Segmentation VLAN 10 et VLAN 20
7. Lien Trunk 802.1Q
8. Boucle réseau, STP et EtherChannel
9. Routage dynamique OSPF et RIP

### 🖥️ Systèmes et services — TP 10 à TP 15

10. Serveur DHCP dédié
11. Serveur DNS local (`intranet.local`)
12. Serveur Web HTTP et base SQL (`/data`)
13. Messagerie SMTP / POP3
14. Serveur FTP et SSH
15. Téléphonie VoIP SIP

### 🛡️ Cybersécurité — TP 16 à TP 20

16. Site HTTPS et autorité TLS
17. Routeur pare-feu stateful
18. Filtrage MAC et Port Security
19. Tunnel VPN et protection Lockout
20. Durcissement Web : anti-DoS, SQLi, XSS et CSRF

---

## 🗺️ 10 topologies pré-câblées avec TP d'évolution

Ces topologies permettent d'aborder directement des situations concrètes sans commencer systématiquement par le câblage.

1. Architecture réseau complète — 14 équipements
2. Maison connectée et télétravail
3. Entreprise multi-sites routés
4. Comparaison Switch et Hub
5. Segmentation VLAN et Trunk
6. Haute disponibilité STP et EtherChannel
7. Laboratoire des services réseau
8. Atelier cybersécurité
9. Deux LAN routés
10. Double pile IPv4 / IPv6 et SLAAC

Chaque topologie constitue une base d'expérimentation pouvant être analysée, modifiée et enrichie.

---

# 🔧 Mode Panne — Enseignant / Élève

Le **Mode Panne** permet de transformer une topologie réseau en exercice de diagnostic.

## 👨‍🏫 Côté enseignant

L'enseignant peut :

- Préparer ou utiliser une topologie existante.
- Sélectionner de 1 à 12 pannes.
- Générer automatiquement des symptômes.
- Fournir des indices pédagogiques sans révéler la cause.
- Proposer un scénario de dépannage aux élèves.

## 👨‍🎓 Côté étudiant

L'étudiant doit :

1. Observer les symptômes.
2. Identifier les équipements potentiellement concernés.
3. Réaliser les tests nécessaires.
4. Analyser les configurations.
5. Identifier les causes des dysfonctionnements.
6. Appliquer les correctifs.
7. Vérifier que le réseau fonctionne à nouveau.

Une fois la panne résolue, un **récapitulatif des tests et des correctifs réalisés** est proposé et peut être exporté.

### 🎯 Objectif

Développer les compétences de diagnostic, d'analyse et de résolution d'incidents, dans un contexte proche des situations professionnelles.

---

# 🎓 Une application conçue pour l'enseignement

TrameX peut être utilisé dans différentes situations pédagogiques.

### 📖 Pendant un cours

L'enseignant peut projeter une topologie et montrer en direct :

- Une résolution ARP.
- L'attribution d'une adresse IP par DHCP.
- Une communication entre VLAN.
- Le traitement d'un paquet par un routeur.
- Le fonctionnement d'un serveur DNS.
- Les mécanismes d'encapsulation OSI et TCP/IP.

### 🧪 Pendant un TP

Les étudiants peuvent construire leurs propres réseaux, modifier les configurations et valider les objectifs attendus.

### 🔧 Pendant une séance de dépannage

Le Mode Panne permet d'organiser des exercices de diagnostic adaptés aux compétences travaillées.

### 🏠 En autonomie

Les étudiants peuvent s'entraîner sur les différentes topologies et approfondir leur compréhension des protocoles.

**TrameX complète les équipements physiques et les autres outils de simulation utilisés dans les établissements.**

---

# 🆓 Mode Démo gratuit

Un **Mode Démo** permet de découvrir les fonctionnalités de TrameX avant l'acquisition d'une licence.

Il donne accès à :

- ✅ L'interface de création de réseaux.
- ✅ Le placement et le câblage des équipements.
- ✅ La simulation des principales communications.
- ✅ Deux TP « Partir de zéro ».
- ✅ Deux topologies préconfigurées.

Certaines fonctionnalités sont réservées à la version complète.

### 🌐 Accéder à TrameX

**[Découvrir TrameX et accéder à l'application](http://dams1140.myasustor.com/lab)**

*L'accès au Mode Démo dépend de son activation sur l'instance publique.*

---

# 🔑 Licence Établissement

## 🎓 149 € TTC — Paiement unique

**Une licence perpétuelle pour l'ensemble de l'établissement.**

L'objectif est de proposer un modèle de licence simple, adapté aux structures d'enseignement et de formation.

### Ce que comprend la licence

- ✅ Utilisation sans limitation de durée.
- ✅ Nombre illimité de postes informatiques.
- ✅ Nombre illimité d'enseignants.
- ✅ Nombre illimité d'élèves.
- ✅ Utilisation dans plusieurs salles informatiques.
- ✅ Accès aux fonctionnalités de la version acquise.
- ✅ Aucun abonnement annuel.
- ✅ Activation par identifiant unique d'établissement.
- ✅ Fonctionnement local possible, sans connexion permanente à un serveur externe de licences.

**149 € TTC pour l'établissement, sans facturation par utilisateur ni par poste.**

Les conditions de maintenance, d'assistance et d'accès aux futures versions sont précisées lors de l'acquisition.

## 📩 Commander ou demander un devis

Pour obtenir des renseignements, demander une licence ou un devis :

**📧 [dams1140@gmail.com](mailto:dams1140@gmail.com?subject=Demande%20de%20licence%20TrameX%20Studio%20Reseau)**

Merci de préciser :

- Le nom de votre établissement.
- Le type de formation concerné.
- Vos coordonnées professionnelles.

---

# 💻 Versions Web et Windows

## 🌐 TrameX Web

La version Web fonctionne directement dans un navigateur compatible.

Elle peut être déployée sur différents environnements :

- Serveur local.
- NAS.
- XAMPP.
- Hébergement PHP compatible.

Elle est particulièrement adaptée aux salles informatiques et aux environnements pédagogiques disposant d'un serveur centralisé.

## 🪟 TrameX Windows

TrameX existe également sous forme d'application de bureau pour Windows.

Cette version dispose d'un système d'installation dédié et permet d'utiliser l'application dans un environnement Windows compatible.

Les conditions d'accès et de distribution sont communiquées avec la licence.

---

# 📋 Historique des versions

Les évolutions de TrameX sont documentées afin de suivre les fonctionnalités ajoutées, les améliorations et les corrections.

### Version 2.5 — Analyseur de trames et encapsulation OSI / TCP-IP

- Nouvel analyseur de trames interactif.
- Frise chronologique des transmissions.
- Visualisation du saut physique.
- Explications pédagogiques détaillées.
- Animation des couches d'encapsulation.
- Amélioration des animations réseau.
- 117 tests automatisés réussis.

**Voir également : [Historique détaillé des versions](CHANGELOG.md)**

---

# 🔒 Licence logicielle et propriété intellectuelle

**TrameX · Studio Réseau est un logiciel propriétaire.**

Ce dépôt GitHub est destiné à la présentation publique du projet.

Il ne contient pas :

- Le code source complet de l'application.
- Le générateur privé des licences.
- Les clés de signature ou autres secrets cryptographiques.
- Les fichiers sensibles de configuration.
- Les mécanismes internes privés d'activation commerciale.

La mise à disposition de ce dépôt ne constitue pas une autorisation de reproduire, modifier, redistribuer ou commercialiser TrameX.

**Tous droits réservés.**

Pour toute question concernant l'utilisation ou la distribution du logiciel, contactez son auteur.

---

# 👨‍💻 À propos du développeur

**TrameX · Studio Réseau est développé par Damien Massé.**

Professionnel de l'informatique, spécialisé dans les systèmes, les réseaux et l'administration d'infrastructures, et enseignant en **BTS CIEL — Option Informatique et Réseaux**.

Le projet est né d'un constat pédagogique : les étudiants peuvent apprendre à configurer des équipements sans toujours comprendre précisément ce qui se passe lorsqu'une trame circule sur le réseau.

TrameX vise à rendre ces mécanismes visibles, compréhensibles et manipulables à travers une approche interactive.

**L'objectif : rapprocher la théorie, la pratique et les situations professionnelles.**

---

### 🌐 TrameX · Studio Réseau

**Construire. Simuler. Comprendre. Diagnostiquer.**

*Un simulateur pédagogique francophone dédié aux réseaux informatiques, aux systèmes et à la cybersécurité.*

**© 2026 Damien Massé — Tous droits réservés.**
