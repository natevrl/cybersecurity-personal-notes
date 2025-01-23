# <mark class="hltr-orange">3.0 Implementation 25%</mark> 

## 3.1 -  implement secure protocols

**Protocols (Protocoles)**:

- **Domain Name System Security Extensions (DNSSEC)**: (anti dns spoofing) **Protocole utilisé pour renforcer la sécurité du DNS** en garantissant l'authenticité et l'intégrité des données DNS.
    
- **SSH (Secure Shell)**: Protocole de communication sécurisé utilisé pour obtenir un accès à une machine (serveur/système) à distance.
    
- **Secure/Multipurpose Internet Mail Extensions (S/MIME)**:(cryptage et sécurisation des e-mails) Standards utilisés pour le cryptage et la signature numérique des e-mails. **Il est largement utilisé pour sécuriser les communications par e-mail dans les environnements professionnels et personnels.**
    
- **SRTP**: Secure Real-time Transport Protocol (Protocole sécurisé, VoiP, Zoom) Protocole sécurisé pour **le transport de données multimédia en temps rée**l.

- **Lightweight Directory Access Protocol Over SSL (LDAPS)**: (LDAP over SSL, active directory) Version sécurisée du protocole LDAP.
    
- **File Transfer Protocol, Secure (FTPS)**: (**FTP + TLS/SSL**) Protocole de transfert de fichiers sécurisé basé sur **FTP**, utilisant TLS ou SSL pour sécuriser les communications.
    
- **SSH File Transfer Protocol (SFTP)**: (**Transfert de fichier avec SSH**)Protocole de transfert de fichiers sécurisé, souvent utilisé pour les transferts de fichiers sécurisés sur les serveurs.

- **Simple Network Management Protocol, version 3 (SNMPv3)**: (Protocole sécurisé permettant de communiquer avec les équipements réseaux) Collecte des infos sur les routeurs, switches...

- **Hypertext Transfer Protocol over SSL/TLS (HTTPS)**: Protocole HTTP sécurisé utilisant SSL/TLS pour crypter les communications Web.
    
- **IPSec (IP Security)**: (**Meilleur protocole pour VPN (most secured)**)
  Suite de protocoles utilisée pour sécuriser les communications Internet.
	-  **AH (Authentication Header)** : IPSec header. Garanti l'intégrité et mais pas la confidentialité (car ne chiffre pas les données). Protège des replays attacks.
	- **ESP (Encapsulating Security Payload)** : IPSec protocol that provides data confidentiality (encryption)



- **Post Office Protocol (POP) / IMAP)**: Post Office Protocol / Internet Message Access Protocol. Protocol pour Récupérer et gérer les emails sur un serveur

**Use cases (Cas d'utilisation)**:

- **Voice and video (Voix et vidéo)**: (**SRTP**) Utilisation des protocoles sécurisés pour assurer la confidentialité et l'intégrité des communications vocales et vidéo.
    
- **Time synchronization (Synchronisation du temps)**: (**NTP**) Utilisation de protocoles sécurisés pour synchroniser l'horloge des appareils et des systèmes.
    
- **Email and web (E-mail et Web)**: (**SMTP, HTTPS**) Sécurisation des communications par e-mail et des transactions Web.
    
- **File transfer (Transfert de fichiers)**: (**SFTP**) Sécurisation des transferts de fichiers entre les systèmes.
    
- **Directory services (Services de répertoire)**: (**LDAPS**) Sécurisation des accès aux annuaires et services de répertoire.
    
- **Remote access (Accès distant)**: (**SSH**) Utilisation de protocoles sécurisés pour permettre l'accès distant aux systèmes et aux réseaux.
    
- **Domain name resolution (Résolution de noms de domaine)**: (**DNSSEC**) Sécurisation du processus de résolution des noms de domaine.
    
- **Routing and switching (Routage et commutation)**: (**IPsec**) Sécurisation des communications entre les routeurs et les commutateurs.
    
- **Network address allocation (Allocation d'adresses réseau)**: (**DHCPv6**) Sécurisation des processus d'attribution d'adresses IP aux dispositifs réseau.
    
- **Subscription services (Services d'abonnement)**: (**HTTPS**) Utilisation de protocoles sécurisés pour protéger les informations d'abonnement et les données sensibles.


## 3.2 - Implement host or application security solutions

**Endpoint protection (Protection des points de terminaison)**: vise à protéger les appareils finaux, tels que les ordinateurs, les portables, les smartphones et les tablettes, contre les menaces et les attaques malveillantes.

- **Antivirus**: Logiciel de sécurité qui identifie, bloque et supprime les virus basiques tels que les virus, les vers et les Trojan.
    
- **Anti-malware**: (**Contrairement aux anti-virus, traite une variété de menaces plus large**) Détecte et élimine divers types de logiciels malveillants, y compris les virus, les ransomwares et les logiciels espions, les kootkits
    
-  **EDR**: Endpoint detection and response (**pour les professionnels**) Système de sécurité qui surveille et détecte les activités suspectes sur les endpoints et répond à ces incidents. Surveille les DB, la mémoire, les comportements des apps... Contraiment a un IPS qui se concentre sur le traffic réseau 
    
- **DLP (Data Loss Protection)**: Représente toutes les mesures mises en place pour éviter la perte ou la fuite des datas hors de l'entreprise.
	- **Exemples** de mesures : (Surveillance et blocage des e-mails, Contrôle des périphériques de stockage...)
	- **Logiciels** : McAfee Data Loss Prevention (DLP), Symantec Data Loss Prevention (DLP)

- **Firewall** : contrôle et filtre le trafic réseau pour protéger les systèmes et les données contre les menaces potentielles.

- **Next-generation firewall (NGFW)**: (**Firewall + IPS**) Pare-feu avancé qui offre des fonctionnalités de filtrage de paquets, d'inspection en profondeur des applications et de prévention des intrusions.

- **IDS (Intrusion Detection System)** : système de détection d'intrusion qui surveille le trafic réseau ou les activités système pour identifier les comportements suspects ou les attaques potentielles. Envoie des alerts et logs lorsque qu'il detecte des anomalies
	- App : **Suricata**

- **IPS (Intrusion Prevention System)** : comme IDS + prend des mesures pour bloquer ou prévenir les attaques en temps réel (real-time)
	- App : **Suricata**

- **FIREWALL vs IDS vs IPS vs EDR**: En résumé, le pare-feu agit comme une barrière de filtrage entre les réseaux, l'IDS surveille le trafic pour détecter les anomalies, tandis que l'IPS détecte et prend des mesures actives pour bloquer ou prévenir les attaques en temps réel. L'EDR surveille les endpoints plus globalement (db, mémoire, traffic), contrairements aux autres que se concentrent sur le réseau

- **Host-based intrusion prevention system (HIPS))**: Système qui détecte et bloque les activités malveillantes sur un système hôte.
    
- **Host-based intrusion detection system (HIDS)**: Système qui surveille les activités suspectes sur un système hôte.
    
- **Host-based firewall (Firewall basé sur l'hôte)**: Pare-feu installé directement sur un système hôte pour contrôler le trafic réseau entrant et sortant.



**Boot integrity (Intégrité du démarrage)**:

- **Boot security** : **Terme général qui englobe toutes les mesures (measured boot, boot attestation, secure boot...**) visant à s'assurer que le processus de démarrage d'un système informatique est sécurisé et fiable
- **Unified Extensible Firmware Interface (UEFI)**: Micrologiciel moderne remplaçant le BIOS traditionnel. L'UEFI offre des fonctionnalités avancées et une interface graphique plus conviviale par rapport au BIOS. Il permet également d'améliorer la sécurité du démarrage grâce à des fonctionnalités telles que le **Secure Boot**.
	- **Measured boot (Démarrage mesuré)**: (processus au démarrage qui vérifie l'intégité des logiciels grace au TPM) Lorsque le Measured Boot est activé, chaque étape du processus de démarrage du système est mesurée (ou évaluée) par un composant matériel de sécurité appelé **TPM** (Trusted Platform Module) (**Se couple avec le secure boot**). 
    
- **Boot attestation (Attestation de démarrage)**: (Prouve l'intégrité du démarrage) Extension du concept de **Measured Boot**, crée une preuve vérifiable de l'intégrité du démarrage (**peut être transmise à un tiers de confiance**)

**TPM (Trusted Platform Module)** : **Hardware intégré à la carte mère d'un ordinateur**, fournissant zone sécurisée pour stocker les clés de chiffrement, les certificats et les données sensibles (utilisés par le **Measured boot, Boot attestation & Secure boot** pour sécurisé le démarrage).


**Database (Base de données)**:

- **Tokenization (Tokenisation)**: Technique de substitution des données sensibles par des valeurs aléatoires (jetons) tout en préservant leur référence.
    
- **Salting (Salage)**: Ajout d'une valeur aléatoire (sel) aux données avant de les hacher pour renforcer la sécurité des mots de passe stockés.
    
- **Hashing (Hachage)**: Transformation de données en une valeur de hachage, souvent utilisée pour vérifier l'intégrité des données.
    

**Application security (Sécurité des applications)**:

- **Input validations (Validation des entrées)**: Vérification des données entrantes pour prévenir les attaques par injection et les erreurs de saisie.
    
- **Secure cookies (Cookies sécurisés)**: Utilisation de cookies sécurisés pour prévenir les attaques de vol de session.
    
- **Hypertext Transfer Protocol (HTTP) headers (En-têtes HTTP)**: Configuration d'en-têtes HTTP pour améliorer la sécurité et la protection contre les attaques.
```makefile
// http HEADER
GET /exemple/page HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.3
Accept: text/html,application/xhtml+xml
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Connection: keep-alive
```
    
- **Code signing (Signature de code)**: Processus de signature numérique (par un hash) des fichiers exécutables. Cela permet aux utilisateurs de **vérifier que le code n'a pas été modifié ou altéré depuis qu'il a été signé** 
    
- **Allow list (Liste autorisée)**: Liste des entités, actions ou ressources autorisées.
    
- **Block list/deny list (Liste bloquée/refusée)**: Liste des entités, actions ou ressources interdites.
    
- **Secure coding practices (Pratiques de codage sécurisé)**: Méthodes de développement d'applications pour réduire les vulnérabilités.
    
- **Static code analysis (Analyse statique du code)**: Vérification du code source pour détecter les erreurs de sécurité potentielles **avant d'executer le programme**, contrairement au Dynamic code analysis.
    
	- **Manual code review (Examen manuel du code)**: Analyse manuelle du code pour identifier les vulnérabilités.
    
- **Dynamic code analysis (Analyse dynamique du code)**: Test des applications en cours d'exécution pour détecter les vulnérabilités.
    
- **Fuzzing**: Technique de test des applications en injectant des données aléatoires pour trouver des bugs et des vulnérabilités.
    

**Hardening (Renforcement)**:

- **Open ports and services (Ports et services ouverts)**: Fermeture des ports et services inutiles pour réduire les vecteurs d'attaque.
    
- **Registry (Registre)**: Configuration sécurisée du registre Windows pour renforcer la sécurité du système.
	- **registry windows** : base de données centralisée dans les systèmes Windows qui stocke des informations critiques sur la configuration du système, des apps et des users. Utilisé par le système d'exploitation pour fonctionner correctement et les applications pour stocker leurs informations de configuration.
    
- **Disk encryption (Chiffrement du disque)**: Utilisation de techniques de chiffrement pour protéger les données stockées sur un disque.
    
- **OS (Système d'exploitation)**: Configuration sécurisée du système d'exploitation pour limiter les vulnérabilités.
    
- **Patch management (Gestion des correctifs)**:
    - **Third-party updates (Mises à jour tierces)**: Application de correctifs pour les logiciels tiers pour réduire les vulnérabilités.
    - **Auto-update (Mise à jour automatique)**: Activation des mises à jour automatiques pour assurer la sécurité continue du système.

**Self-encrypting drive (SED) / Full-disk encryption (FDE)**: Font référence à des technologies de chiffrement utilisées pour protéger les données stockées sur des disques durs ou des périphériques de stockage.
- **SED (Self-Encrypting Drive)** : Type de disque dur équipé d'un processeur de chiffrement matériel intégré (contrairement a un HDD/SDD qui dépendent de l'OS pour le chiffrement).
	- **Opal**: Standard de gestion de disque auto-chiffrant (**SED**) pour le chiffrement matériel.
- **FDE (Full-Disk Encryption, chiffrement intégral du disque)** : Lorsqu'il est activé, toutes les données écrites sur le disque sont automatiquement chiffrées et toutes les données lues depuis le disque sont automatiquement déchiffrées (y compris l'OS).

**Hardware root of trust (Racine de confiance materielle)** : Utilisation de composants matériels sécurisés pour garantir l'intégrité et la confidentialité des opérations.


**Sandboxing** : Technique qui permet d'exécuter des applications ou du code potentiellement dangereux dans un environnement isolé et contrôlé, appelé le "bac à sable"


## 3.3 - Implement secure network designs

**Load balancing (Répartition de charge)**:  Distribuer équitablement la charge de travail pour éviter les surcharges.

- **Active/active (Actif/actif)**: Tous les équilibreurs de charge gèrent simultanément le trafic en répartissant la charge entre eux.
    
- **Active/passive (Actif/passif)**: Un équilibreur de charge est actif et gère le trafic, tandis que les autres sont en mode veille de secours, prêts à prendre le relais en cas de besoin.
    
- **Scheduling (Planification)**: Méthode utilisée pour déterminer comment le trafic est réparti entre les serveurs.
    
- **Virtual IP (IP virtuelle)**: Adresse IP utilisée pour représenter un groupe de serveurs, permettant de masquer la véritable adresse IP des serveurs.
    
- **Persistence (Persistance)**: Mécanisme pour s'assurer que les requêtes d'un client sont toujours envoyées au même serveur.
    

**Network segmentation (Segmentation du réseau)**:

- **Virtual Local Area Network (VLAN) (Réseau local virtuel)**: 
  Utilisé pour diviser un réseau en plusieurs sous-réseau (subnets)
  Méthode de segmentation logique des réseaux physiques pour isoler des groupes d'appareils, meme si ils sont connecte au meme switch.
     ![[dgiw0e22.bmp|400]]
     
- **Screened subnet (previously known as DMZ) (Sous-réseau filtré)**: Un sous-réseau sécurisé séparant les réseaux internes et externes.Ce sous-réseau est **situé entre le routeur/pare-feu** frontal et le réseau interne.
   ![[F19-02.jpg|400]]
- **East-west traffic (Trafic est-ouest)**: Flux de trafic entre les appareils au sein d'un réseau local (**Nord-sud = client/serveur**).
    
- **Extranet**: Partie du réseau qui permet l'accès aux utilisateurs externes autorisés.
    
- **Intranet**: Réseau interne réservé aux utilisateurs et appareils internes de l'organisation.
    
- **Zero Trust (Confiance zéro)**: **(Confiance en personne, meme au sein de l'entreprise)** Modèle de sécurité qui ne fait pas confiance implicitement aux appareils ou utilisateurs, même s'ils sont internes au réseau (Demande d'authentification permanente etc).
    

**Virtual Private Network (VPN) (Réseau privé virtuel)**: Créer une connexion sécurisée et chiffrée entre un appareil et un serveur distant (du VPN). masque l'IP (prend l'IP du VPN)

- **Always-on (Toujours actif)**: VPN qui maintient une connexion sécurisée en permanence.
    
- **Full tunnel**: Tout le trafic, y compris le trafic Internet personnel, est chiffré et passe par le VPN, offrant une sécurité maximale.Tout le trafic Internet personnel consomme la bande passante de l'entreprise, ce qui peut entraîner des ralentissements.

- **Split tunnel** : Choisir mes apps qui utilise VPN ou non. 
  Diviser son trafic réseau entre une connexion VPN et une connexion Internet directe (non chiffré). 
  Ex: Seul le trafic lié aux ressources de l'entreprise passe par le VPN, ce qui réduit la charge sur le réseau de l'entreprise car le trafic Internet personnel ne consomme pas la bande passante de l'entreprise.


    
- **Remote access vs. site-to-site (Accès distant vs. site-à-site)**: Les VPN d'accès distant permettent aux utilisateurs distants de se connecter au réseau interne, tandis que les VPN site-à-site connectent des réseaux distants.
    
- **IPSec**: Protocole de sécurité utilisé pour établir des connexions VPN sécurisées.
    
- **SSL/TLS**: Protocole de cryptage utilisé pour sécuriser les connexions Web.
    
- **HTML5**: Dernière version du langage de balisage utilisé pour structurer le contenu des pages Web.
    
- **Layer 2 Tunneling Protocol (L2TP) (Protocole de tunnelisation de couche 2)**: 
  (trés sécurisé, smartphone, lent)
  Type de VPN facile d'accès et facile a configuré sur les smartphones et ordi perso. Très sécurisé car encapsule les données deux fois, ce qui signifie une double vérification des données
    

**DNS (Système de noms de domaine)**: Système utilisé pour traduire les noms de domaine en adresses IP.

<mark class="hltr-blue">**Network Access Control (NAC) (Contrôle d'accès au réseau)**</mark> :
Gère les accès à un réseau en fonction de l'identité ou de la conformité d'un appareil. Utile pour BYOD (bring you own device)
Exemple : 
Un employé tente de se connecter au réseau d'entreprise avec un ordinateur portable. Le *** vérifie si l'ordinateur a la dernière version de l'antivirus. Si ce n'est pas le cas, l'accès au réseau est refusé jusqu'à ce que l'employé mette à jour l'antivirus.
- *** Agent : logiciel sur la machine client qui communique avec le ***
- *** Agentless : sans agent, vérifie les ports ouverts de la machine pour l'autoriser, par exemple.

**Out-of-band management (Gestion hors bande)**: Méthode pour gérer les dispositifs réseau via un canal de communication distinct du réseau principal, pour administrer et gérer les équipements réseau. L'objectif principal de l'OOB est d'**assurer une gestion continue même en cas de problèmes** ou de congestion sur le réseau principal.

**Port security (Sécurité des ports)**:
- **Broadcast storm prevention** : Mécanisme pour éviter la surcharge du réseau due à des diffusions excessives.
    
- **Bridge Protocol Data Unit (BPDU) guard**: Mécanisme pour protéger contre les attaques basées sur les BPDU, tels que les attaques de l'arbre de couverture.
    
- **Loop prevention (Prévention des boucles)**: Méthodes pour détecter et éviter les boucles de réseau.
    
- **Dynamic Host Configuration Protocol (DHCP) snooping**: Mécanisme pour protéger contre les attaques d'usurpation d'adresse IP.
    
- **MAC filtering**: Méthode pour contrôler l'accès au réseau en fonction des adresses MAC des périphériques.
    

**Network appliances (Appareils réseau)**:
- **Jump servers (Serveurs de saut)**: Serveurs utilisés pour accéder à des réseaux sensibles ou isolés.
    
- **Proxy servers** : intermédiaire entre un client (généralement un utilisateur) et un serveur de destination (masque l'IP réelle du client)
    
    - **Forward (Transfert)**: (**Proxy classique**) Les clients envoient leurs requêtes au proxy, qui les relaie ensuite vers les serveurs appropriés.
    - **Reverse Proxy**: proxy qui agit au nom des serveurs de destination en gérant le trafic entrant de l'extérieur et en le redirigeant vers les serveurs internes appropriés.

- **Network-based Intrusion Detection System (NIDS)/Network-based Intrusion Prevention System (NIPS): Comme IDS/IPS mais pour les réseaux
    
    - **Signature-based (Basé sur les signatures)**: Utilise des signatures connues pour détecter les attaques connues.
    - **Heuristic/behavior (Heuristique/comportement)**: Identifie les comportements malveillants en fonction de modèles et d'heuristiques.
    - **Anomaly (Anomalie)**: Détecte les comportements anormaux du trafic réseau.
    - **Inline vs. passive (En ligne vs. passif)**: En ligne bloque activement les attaques, tandis que passif surveille sans intervention.

- **HSM (Hardware Security Module)**: (Matériel, Sécurité, Cryptographie)
  Appareil physique conçu spécifiquement pour gérer et protéger les clés cryptographiques tout en offrant des performances de cryptographie à haute vitesse.
    
- **Sensors (Capteurs)**: (**forwarder splunk**) Dispositifs de surveillance utilisés pour collecter des données sur les réseaux et les systèmes.
    
- **Collectors (Collecteurs)**: (**Wireshark**) Appareils qui recueillent et agrègent les données provenant de plusieurs sources.
    
- **Aggregators (Agrégateurs)**: (**Splunk**) Dispositifs qui combinent les données de multiples sources pour faciliter leur analyse.
    
- **Firewalls (pare-feu)**:(**Gardiens a l'entrée du Royaume**) contrôle et filtre le trafic réseau pour protéger les systèmes et les données contre les menaces potentielles.
    
    - **Web Application Firewall (WAF)**: (Pare-feu d'application Web, examine les requêtes entrantes) Spécialisé dans la protection des applications Web contre les attaques (XSS, CSRF...).
    - **NGFW (Pare-feu nouvelle génération)**: Combine les fonctionnalités d'un pare-feu traditionnel avec des capacités avancées de filtrage de paquets et d'inspection approfondie des applications.
    - **Stateful (À état)**: S'occupe de la session de connexion entière, en gardant des traces de chaque paquets reçus
    - **Stateless (Sans état)**: Traite chaque paquet individuellement sans se soucier des connexions établies précédemment.
    - **UTM**: Unified Threat Management
      Solution de sécurité tout-en-un (firewall, DLP, antivirus, VPN, IDS...)
    - **Network Address Translation (NAT) gateway** : Permet de masquer les adresses IP internes des appareils derrière une seule adresse IP publique.
    - **Content/URL filter (Filtre de contenu/URL)**: Filtrage du trafic en fonction du contenu ou des URL visitées.
    - **Open-source vs. proprietary (Open-source vs. propriétaire)**: Différences entre les pare-feu basés sur un logiciel open-source et ceux basés sur des logiciels propriétaires.
    - **Hardware vs. software (Matériel vs. logiciel)**: Différences entre les pare-feu basés sur du matériel dédié et ceux basés sur un logiciel exécuté sur des serveurs.
    - **Appliance vs. host-based vs. virtual** :
	    - **Appliance** : pare-feu matériel
	    - **host-based** : pare-feu logiciel installé sur l'OS d'un user
	    - **virtual** : pare-feu utilisé dans les VM (sécuriser les charges de travail virtuelles et les environnements de cloud computing, en appliquant des politiques de sécurité aux instances virtuelles.)

**ACL**: Liste de contrôle d'accès (Portier de données, Permissions, Ressources)
Liste qui détermine quels utilisateurs ou systèmes sont autorisés à accéder à quelles ressources.
Exemple : CHMOD est considéré comme une forme d'ACL

**Route security (Sécurité des routes)**: Mesures de sécurité pour protéger les informations de routage et empêcher les attaques d'usurpation de route.

**Quality of Service (QoS) (Qualité de service)**: Mécanisme pour prioriser le trafic réseau en fonction de ses exigences de performance.

**Implications of IPv6 (Implications de l'IPv6)**: Considérations de sécurité spécifiques à l'IPv6, le protocole de nouvelle génération d'Internet.

**Port Spanning/Port Mirroring**: (Duplication, Surveillance, Diagnostic) Le commutateur crée une copie du trafic qui traverse un port (ou un groupe de ports) et l'envoie à un port spécifique où un dispositif d'analyse, comme un analyseur de protocole, peut examiner le trafic en détail.
- **Port taps**: dispositif physique qui copie le traffic réseau et l'envoi vers un monitoring service pour l'analyse et la surveillance, sans perturber le trafic original.

**Monitoring services (Services de surveillance)**: Services utilisés pour surveiller l'état et la performance du réseau.

**File Integrity Monitors (Moniteurs d'intégrité des fichiers)**: Outils pour surveiller les fichiers système et détecter les modifications non autorisées.


## 3.4 - Install and configure wireless security settings

- <mark class="hltr-blue">**Protocoles cryptographiques**:</mark> 
    - **WiFi Protected Access 2 (WPA2)**: Protocole de sécurité sans fil qui utilise des clés de chiffrement (AES et CCMP) pour sécuriser les communications Wi-Fi. Il est plus sécurisé que son prédécesseur WEP.
    - **<mark class="hltr-blue">WEP</mark>** : Protocole de sécurité sans fil **considéré comme obsolète car sensible au brute-force**
    - **WiFi Protected Access 3 (WPA3)**: Évolution de WPA2 avec des améliorations de sécurité, y compris une protection renforcée contre les attaques de force brute.
    - **CCMP**: Counter-mode/CBC-MAC Protocol. (Confidentialité et intégrité et données sans fil)
      Dans WPA2, lorsque des données sont transmises sur un réseau Wi-Fi, elles sont chiffrées avec AES via le protocole CCMP, garantissant ainsi à la fois leur confidentialité et leur intégrité.
    - **Simultaneous Authentication of Equals (SAE)**: (Robuste, WPA3) mécanisme d'authentification introduit dans WPA3 pour renforcer la sécurité de l'échange initial de clés..

- **Protocoles d'authentification**:
    - <mark class="hltr-blue">Extensible Authentication Protocol (EAP)</mark>: Protocole d'authentification sous-jacent utilisé dans les réseaux sans fil. utilisé pour WPA2 et IEEE 802.1X.
	  ex : Lorsqu'un employé tente de se connecter au réseau Wi-Fi d'une entreprise, il pourrait être invité à entrer un nom d'utilisateur et un mot de passe. Cette authentification est souvent gérée par EAP avec un serveur RADIUS en arrière-plan
    - **Protected Extensible Authentication Protocol (PEAP)**: (EAP over TLS) Sécurise le canal EAP en le faisant passer à travers un tunnel TLS.
    - **EAP-FAST**: (PEAP more flexible and secure) méthode Cisco qui a été conçue pour améliorer la sécurité et la flexibilité de PEAP.
    - **EAP-TLS**: (EAP avec certificats X.509) Méthode d'authentification qui utilise des certificats numériques côté serveur et côté client pour une authentification mutuelle.
    - **EAP-TTLS**: (PEAP + multiple authentification) Similaire à PEAP mais permet plusieurs authentification dans le tunnel.
    -<mark class="hltr-blue">IEEE 802.1X</mark> : (Contrôle, Accès, Réseau) (Connexion dans une **bibliotheque** avec username & MDP = **IEEE 802.1X** recoit une demande encapsulées dans un paquet EAP, puiscontrôle l'accès au réseau en vérifiant vos identifiants via un serveur d'authentification central (comme un serveur **RADIUS**) ) 
    standard d'authentification pour le contrôle d'accès réseau basé sur le port.
    - **Remote Authentication Dial-in User Service (RADIUS) Federation**: (Serveur, Authentification, Centralisé.) Le serveur back-end qui vérifie les informations d'identification de l'utilisateur.

- **Méthodes**:
    - **Pre-shared key (PSK) vs. Enterprise vs. Open**: Différentes méthodes d'authentification et de sécurité pour les réseaux Wi-Fi.
	    - <mark class="hltr-blue">(PSK) Pre-shared key</mark> : (**MDP WIFI PERSONNEL**) Une clé secrète déjà connue par les deux parties (toi et la box) avant d'établir une communication sécurisée. **Chiffrement symmétrique, utile pour WPA2 et VPN**.
	    - **Enterprise** : (Centralisé, RADIUS) Utilise un serveur d'authentification central (RADIUS) pour valider les utilisateurs sur le réseau.
	    - Open : (freewifi)nécessite aucun mot de passe, gratuit pour tous.
    - <mark class="hltr-blue">WiFi Protected Setup (WPS)</mark> : Méthode simplifiée pour ajouter des appareils à un réseau Wi-Fi en utilisant un **code PIN** ou un **bouton de connexion** (Connecté une imprimante en appuyant sur son bouton WPS + sur le bouton WPS du routeur).
    - **Captive portals**: (macdo, flixbus) Portails d'authentification où les utilisateurs doivent se connecter avant d'accéder au réseau Wi-Fi.

- **Considérations lors de l'installation**:
- **Site surveys** (Études de site) : Études pour déterminer la couverture optimale des points d'accès Wi-Fi.
- **Heat maps** (Cartes de chaleur) : Cartes pour visualiser la couverture du signal sans fil.
- **WiFi analyzers** (Analyseurs Wi-Fi) : Outils pour analyser les performances et la qualité du réseau sans fil.
- **Channel overlaps** (Chevauchements de canaux) : Gestion des interférences et des chevauchements de canaux.
- **Wireless access point (WAP) placement** : Emplacement stratégique des points d'accès sans fil pour une couverture efficace.
- **Controller and access point security** : Sécurité des contrôleurs et des points d'accès sans fil pour protéger la gestion du réseau.

## 3.5 - Implement secure mobile solutions

- **Méthodes de connexion et récepteurs**:
    - **Cellulaire (Cellular)**: (**4g/5g**) Utilisation de réseaux de téléphonie mobile pour la connectivité.
    - **WiFi (WiFi)**: Connexion sans fil à des réseaux locaux ou à Internet.
    - **Bluetooth (Bluetooth)**: Technologie sans fil courte portée pour la communication entre appareils.
    - **NFC (Near Field Communication) (Communication en champ proche)**: Communication pour le partage d'informations entre appareils à courte distance.
    - **Infrarouge (Infrared)**: Utilisation de signaux infrarouges pour la communication entre appareils.
    - **USB (USB)**: Connexion à l'aide de câbles USB.
    - **Point à point (Point-to-point)**: Connexion directe entre deux appareils.
    - **Point à multipoint (Point-to-multipoint)**: Connexion d'un appareil à plusieurs autres appareils.
    - **Global Positioning System (GPS)**: Utilisation de signaux satellites pour déterminer la position géographique.
    - **RFID (Radio Frequency Identification)**: Utilisation de signaux radio pour identifier et suivre les objets.

- **Mobile Device Management (MDM)**:
    - **Gestion des applications (Application Management)**: Contrôle et gestion des applications installées sur les appareils mobiles.
    - **Gestion des contenus (Content Management)**: Gestion des données et du contenu sur les appareils mobiles.
    - **Effacement à distance (Remote Wipe)**: Capacité à effacer les données d'un appareil à distance en cas de perte ou de vol.
    - **Géorepérage (Geofencing)**: Définition de zones géographiques pour déclencher des actions ou des politiques spécifiques.
    - **Géolocalisation (Geolocation)**: Suivi de la position géographique des appareils.
    - **Verrouillage de l'écran (Screen Locks)**: Exiger un mot de passe ou un code PIN pour déverrouiller l'appareil.
    - **Notifications push (Push Notifications)**: Envoi de notifications directement sur l'appareil.
    - **Mots de passe et codes PIN (Passwords and PINs)**: Utilisation de mots de passe et de codes PIN pour sécuriser l'accès.
    - **Biométrie (Biometrics)**: Utilisation de caractéristiques physiques uniques (empreintes digitales, reconnaissance faciale, etc.) pour l'authentification.
    - **Authentification contextuelle (Context-Aware Authentication)**: Adaptation du niveau de sécurité en fonction du contexte de l'utilisateur.
    - **Containerisation (Containerization)**: Isolation des applications et des données dans des conteneurs sécurisés.
    - **Ségmentation du stockage (Storage Segmentation)**: Séparation des données professionnelles et personnelles sur l'appareil.
    - **Chiffrement complet de l'appareil (Full Device Encryption)**: Chiffrement de toutes les données sur l'appareil pour protéger la confidentialité.

- **Appareils mobiles**:
    - **HSM (mobile device)**: HSM (Hardware Security Module) sour forme MicroSD.
      Dispositif physique qui gère, génère et stocke des clés cryptographiques.
      
    - **MDM/UEM (mobile device)**: Mobile Device Management/ Unified Endpoint Management
      Plateformes pour gérer et sécuriser les appareils mobiles dans une entreprise.
      Une entreprise installe MDM sur les smartphones des employés pour pour pouvoir remote wipe en cas de vol/perte.
    - **MAM (mobile device)**: Mobile Application Management
      "Sécurisation des apps, pas des appareils". Gestion spécifique des applications installées sur les appareils mobiles.
    - **SEAndroid (mobile device)**: (Android avec armure) Version modifiée d'Android avec des fonctionnalités de sécurité renforcées.

- **Application et surveillance de**:
    - **Magasins d'applications tiers (Third-Party Application Stores)**: Contrôle et surveillance des applications provenant de sources autres que les app stores officiels.
    - **Rooting / Jailbreaking**: (Bypass, Restrictions, iOS) Processus de suppression des restrictions imposées par Apple sur les appareils iOS pour permettre l'installation d'applications non approuvées par l'App Store.
    - **Installation latérale (Sideloading)**: Installation d'applications sans passer par le magasin d'applications officiel (Playstore, App store).
    - **Firmware personnalisé (Custom Firmware)**: Utilisation de versions modifiées du système d'exploitation.
    - **Déverrouillage du transporteur (Carrier Unlocking)**: Désimlockage.
    - **Firmware Over-The-Air Updates**: Mises à jour du firmware et du système d'exploitation sans fil.
    - **Utilisation de la caméra (Camera Use)**: Contrôle et surveillance de l'utilisation de l'appareil photo.
    - **Services de messagerie SMS / MMS / RCS (Rich Communication Services)**: Sécurisation des services de messagerie texte et multimédia.
    - **Supports externes (External Media)**: Contrôle des supports de stockage externes tels que les cartes SD et les clés USB.
    - **USB On-The-Go (USB OTG)**: cable usb/usb-c pour connecter son smartphone avec un dispositif USB (clé, souris..)
    - **Microphone d'enregistrement (Recording Microphone)**: Surveillance de l'utilisation du microphone.
    - **Balises GPS (GPS Tagging)**: Surveillance de l'utilisation du suivi GPS.
    - **WiFi Direct / Ad hoc**: Connexions Wi-Fi directes entre appareils.
    - **Partage de connexion (Tethering)**: Partage de connexion
    - **Point d'accès (Hotspot)**: Utilisation de l'appareil comme point d'accès Wi-Fi.
    - **Méthodes de paiement (Payment Methods)**: Sécurisation des méthodes de paiement mobiles.

- **Modèles de déploiement**:
    - **BYOD**: (Bring Your Own Device) Autoriser les employés à utiliser leurs propres appareils au travail.
    - **COPE**:(Corporate-Owned Personally-Enabled) L'entreprise fournit et gère l'appareil, mais l'employé peut également l'utiliser à des fins personnelles.
    - **CYOD**: (Choose Your Own Device) L'entreprise offre une sélection d'appareils parmi lesquels les employés peuvent choisir.
    - **Corporate-Owned**: L'entreprise fournit et gère entièrement l'appareil.
    - **Infrastructure de bureau virtuel (VDI) (Virtual Desktop Infrastructure)**: Utilisation d'environnements de bureau virtuels pour accéder aux applications et aux données depuis des appareils mobiles.


## 3.6 - solutions to the cloud

**Cloud security controls (Contrôles de sécurité du cloud)** : Mesures pour sécuriser les données et services dans le cloud.

- **High availability across zones (Haute disponibilité entre les zones)** : Garantir un service ininterrompu même si une zone du cloud a des problèmes.
  __Informations__ : En cas de défaillance dans une zone, le trafic est automatiquement redirigé vers une zone saine.
  __Technique__ : Cela implique souvent la mise en place de clusters multi-zones, de balancers de charge et de systèmes de basculement automatique.

- **Resource policies (Politiques de ressources)** : Règles définissant comment les ressources cloud sont utilisées. (souvent définies en JSON* ou YAML*)

- **Secrets management (Gestion des secrets)** : Gestion sécurisée des informations sensibles. (clé API, les mots de passe, les certificats et d'autres données qui doivent être gardées secrètes)

- **Integration and auditing (Intégration et audit)** : Processus d'ajout de services ou d'applications à un système existant et de vérification de leur conformité.
    
- **Storage (Stockage)** : Espace où les données sont conservées dans le cloud (Elasticity & scalability).
    - **Permissions (Permissions)** : Règles définissant qui peut accéder à quoi.
        
    - **Encryption (Chiffrement)** : Processus de conversion des données en code pour empêcher l'accès non autorisé. _Informations_ : Assure que même si les données sont interceptées ou compromises, **elles restent illisibles sans la clé de déchiffrement appropriée**. _Technique_ : Les standards comme AES* et RSA* sont couramment utilisés pour le chiffrement.
        
    - **Replication (Réplication)** : Création de copies de données pour assurer la redondance et la disponibilité. _Technique_ : Les bases de données comme MySQL* peuvent être configurées en mode maître-esclave pour la réplication.

- **Network (Réseau)** : Infrastructure permettant la communication entre différents dispositifs dans le cloud.
  
	- **Virtual networks (Réseaux virtuels)** : Les réseaux virtuels permettent de créer des environnements réseau isolés et personnalisés dans le cloud
    
    - **Public and private subnets (Sous-réseaux publics et privés)** : Un sous-réseau public est généralement utilisé pour des ressources qui doivent être accessibles depuis l'Internet public, comme un serveur web, tandis qu'un sous-réseau privé est utilisé pour des ressources internes comme une base de données. 
      _Technique_ : Utilisation d'un NAT gateway* pour permettre aux ressources d'un sous-réseau privé d'accéder à Internet tout en restant non exposées directement.
        
    - **Segmentation (Segmentation)** : Division d'un réseau en segments pour améliorer performance et sécurité.
        
    - **API inspection and integration (Inspection et intégration d'API)** : Surveillance et connexion d'API. _Technique_ : Des solutions comme les gateways d'API* et les WAF* (web applicaton firewall)
        
- **Compute (Calcul)** : Ressources du cloud dédiées au traitement des données. Le calcul dans le cloud offre une flexibilité (elasticity) et une évolutivité (scalability), permettant d'ajuster les ressources en fonction des besoins. 

	- **Security groups (Groupes de sécurité)** : Filtres qui contrôlent le trafic entrant et sortant pour les ressources cloud. _Informations_ : Les groupes de sécurité agissent comme un pare-feu virtuel pour vos instances, garantissant que seul le trafic autorisé atteint vos instances. _Technique_ : Ils sont basés sur des règles définies par l'utilisateur concernant le protocole, le port et l'adresse IP source/destination.
    
	- **Dynamic resource allocation (Allocation dynamique de ressources)** : Ajustement automatique des ressources en fonction de la demande (optimise et économise des coûts).  _Technique_ : Les services comme AWS Auto Scaling* ajustent dynamiquement le nombre d'instances.
    
	- **Instance awareness (Conscience d'instance)** : Capacité d'une application ou d'un service à reconnaître et à répondre à l'état d'une instance. Utile pour la récupération après sinistre et la performance.
    
	- **Virtual private cloud (VPC) endpoint (Point de terminaison du VPC)** : Assure une communication privée entre les instances du VPC et les services sans nécessiter d'accès Internet. _Technique_ : AWS VPC Endpoint* est un exemple qui permet la communication privée avec les services AWS.
    
	- **Container security (Sécurité des conteneurs)** : Mesures de sécurité pour protéger les applications et les services exécutés dans des conteneurs. _Technique_ : Des outils comme Docker Bench* pour la sécurité et Clair* sont utilisés pour analyser la sécurité des conteneurs.

**Solutions :**
- **CASB (Cloud Access Security Broker)** : 
  2 fonctions du CASB : Liste des applications in use, Verification du chiffrement des données
  Intermediaire entre les utilisateurs et les fournisseurs de services cloud pour assurer la sécurité. _Technique_ : Ils peuvent offrir des fonctionnalités comme la détection des menaces, le chiffrement et l'authentification multi-facteurs.
    
- **Application security (Sécurité des applications)** : Mesures pour protéger les applications contre les menaces. _Technique_ : Des outils comme OWASP ZAP* et Burp Suite* sont utilisés pour tester la sécurité des applications.
    
- **Next-generation secure web gateway (SWG) (Passerelle web sécurisée de nouvelle génération)** : Les SWG modernes offrent une protection contre les menaces web avancées, tout en permettant l'accès aux applications cloud. _Technique_ : Ils peuvent inclure des fonctionnalités comme la détection de sandboxing*, le filtrage URL et l'inspection SSL*.
    
- **Firewall considerations in a cloud environment (Considérations du pare-feu dans un environnement cloud)** : Les environnements cloud ont des besoins spécifiques en matière de pare-feu, tels que la scalabilité et l'intégration avec d'autres services cloud. _Technique_ : Les pare-feux de nouvelle génération, ou NGFW*, sont souvent utilisés dans les environnements cloud pour leur capacité à s'intégrer et à évoluer.
    
**Cloud native controls vs. third-party solutions (Contrôles natifs du cloud vs. solutions tierces)** : Comparaison entre les outils de sécurité intégrés proposés par les fournisseurs de cloud et les solutions externes

**Termes techniques** :

- _SIEM_ : Security Information and Event Management - Plateformes conçues pour la surveillance en temps réel et la réponse aux incidents de sécurité.
- _ACL_ : Access Control List - Liste définissant qui a accès à quoi.
- _AES_ : Advanced Encryption Standard - Algorithme de chiffrement symétrique couramment utilisé.
- _RSA_ : Algorithme de cryptographie asymétrique utilisé pour la sécurité des données.
- _MySQL_ : Système de gestion de base de données relationnelle open-source.
- _VPN_ : Virtual Private Network - Réseau privé qui permet de sécuriser la connexion entre des sites distants.
- _NAT gateway_ : Network Address Translation gateway - Permet aux ressources d'un sous-réseau privé d'accéder à Internet.
- _VLAN_ : Virtual Local Area Network - Réseau local virtuel pour la segmentation.
- _API Gateway_ : Service qui permet de créer, publier, gérer, surveiller et sécuriser des APIs.
- _AWS Auto Scaling_ : Service AWS qui ajuste automatiquement la capacité pour maintenir les performances et minimiser les coûts.
- _CloudWatch_ : Service de surveillance offert par AWS.
- _AWS VPC Endpoint_ : Service qui permet la communication privée entre le VPC et les services AWS.
- _Docker Bench_ : Outil de script qui vérifie les déploiements Docker contre les meilleures pratiques.
- _Clair_ : Outil d'analyse de vulnérabilité pour les conteneurs.
- _OWASP ZAP_ : Outil de test de sécurité open-source pour les applications web.
- _Burp Suite_ : Outil de test de sécurité pour les applications web.
- _Sandboxing_ : Technique permettant d'exécuter des programmes dans un environnement isolé.
- _SSL Inspection_ : Examiner le contenu des communications SSL chiffrées.
- _NGFW_ : Next-Generation Firewalls - Pare-feux avancés avec des capacités telles que l'inspection approfondie des paquets et la prévention des intrusions.



## 3.7 - implement identity and account management controls.

**Identity (Identité)** : Savoir qui accède à quoi est essentiel pour maintenir la sécurité des données et des ressources. 
- **Identity provider (IdP) (Fournisseur d'identité)** : (**Active Directory == IdP**) Services qui créent, maintiennent et gèrent l'identité des utilisateurs.
    
- **Attributes (Attributs)** : Caractéristiques ou propriétés associées à une identité (rôle, département, emplacement, etc.). _Technique_ : Dans LDAP*, les attributs peuvent inclure des éléments comme "cn" (common name) ou "mail".
    
- **Certificates (Certificats)** : Fichiers numériques utilisés pour prouver l'identité et établir une confiance.
    
- **Tokens (Jetons)** : Objets ou informations utilisés pour prouver l'identité ou les droits d'accès. _Informations_ : Les jetons peuvent être physiques (comme un jeton USB) ou numériques (comme un JWT*). _Technique_ : Ils sont souvent utilisés dans l'authentification à deux facteurs (2FA*).
    
- **SSH keys (Clés SSH)** : Clés utilisées pour l'authentification dans le protocole SSH*.
    
- **Smart cards (Cartes à puce)** : Important : Contient un certificat digital embarquée dans la puce
  Cartes avec une puce électronique intégrée utilisée pour l'authentification.
    
**Account types (Types de comptes)** : Différents types de comptes utilisés pour accéder aux systèmes.
- **User account (Compte utilisateur)** : Compte attribué à un utilisateur individuel. 
    
- **Shared and generic accounts/credentials (Comptes/identifiants partagés et génériques)** : Comptes utilisés par plusieurs personnes ou pour plusieurs services.
    
- **Guest accounts (Comptes invités)** : Comptes avec des droits limités, souvent temporaires. 
    
- **Service accounts (Comptes de service)** : Comptes utilisés par des applications ou des services. _Informations_ : Ils permettent aux applications ou services de s'exécuter avec les permissions nécessaires.
    
**Account policies (Politiques de compte)** : Règles définissant comment les comptes sont gérés et sécurisés. 

- **Password complexity (Complexité du mot de passe)** : Exigences pour la création de mots de passe forts.

- **Password history (Historique des mots de passe)** : Mémoire des anciens mots de passe utilisés.
  *Informations* : Empêche la réutilisation des mots de passe précédemment utilisés, augmentant la sécurité du compte.

- **Password reuse (Réutilisation des mots de passe)** : Utilisation du même mot de passe sur plusieurs comptes ou services.
  *Informations* : C'est une pratique risquée car si un service est compromis, tous les comptes utilisant le même mot de passe sont vulnérables.

- **Network location (Emplacement réseau)** : L'emplacement physique ou logique d'où un utilisateur accède à un réseau.
  *Technique* : Les VPNs* peuvent être utilisés pour masquer ou changer l'emplacement réseau.

- **Geofencing (Géorepérage)** : Définir des limites géographiques virtuelles et déclencher des actions lorsqu'elles sont franchies.
  *Informations* : Utile pour restreindre l'accès ou envoyer des alertes basées sur la localisation géographique.

- **Geotagging (Géomarquage)** : Ajout d'informations de localisation, comme la latitude et la longitude, à des ressources comme les photos.
  *Technique* : Les appareils photo modernes et les smartphones incluent souvent des fonctionnalités de géomarquage (metadata).

- **Geolocation (Géolocalisation)** : Détermination de l'emplacement physique d'un objet, comme un appareil mobile.

- **Time-based logins (Connexions basées sur le temps)** : Restrictions d'accès basées sur l'heure ou la date.

- **Access policies (Politiques d'accès)** : Règles définissant qui peut accéder à quoi et dans quelles conditions.
  *Technique* : Souvent mises en œuvre avec des listes de contrôle d'accès (ACLs*).

- **Account permissions (Permissions de compte)** : Les permissions définissent ce qu'un utilisateur ou un service peut voir, modifier ou exécuter.

- **Account audits (Audits de compte)** : Examen des activités et des actions associées à un compte.

- **Impossible travel time/risky login (Temps de déplacement impossible/connexion risquée)** : Détection d'accès suspect basé sur des emplacements géographiques improbables en un court laps de temps.
  *Informations* : **Si quelqu'un se connecte depuis Paris et 5 minutes plus tard depuis New York**, c'est probablement une activité suspecte.

- **Lockout (Verrouillage)** : Action de bloquer un compte après un certain nombre de tentatives de connexion échouées. (anti brute force)

- **Disablement (Désactivation)** : Action de rendre un compte inactif.
  *Informations* : Utile pour les employés qui quittent une organisation ou pour les comptes qui ne sont plus nécessaires.

---

**Termes techniques** (mise à jour) :

- ***ACLs*** : Access Control Lists, listes utilisées pour définir les permissions.
- **_LDAP_** : Lightweight Directory Access Protocol, protocole pour accéder et maintenir des informations de l'annuaire.
- _Okta_ : Plateforme d'identité pour l'entreprise.
- _Microsoft AD_ : Microsoft Active Directory, service d'annuaire pour la gestion des identités.
- _JWT_ : JSON Web Token, format de jeton compact pour l'authentification.
- _2FA_ : Authentification à deux facteurs, méthode d'authentification utilisant deux formes différentes de vérification.
- _SSH_ : Secure Shell, protocole crypté pour la communication réseau sécurisée.
- *Hashs* : Fonctions qui transforment l'entrée (comme un mot de passe) en une chaîne de caractères fixe.
- *Gestionnaires de mots de passe* : Outils qui stockent et gèrent les mots de passe de l'utilisateur.
- *VPN* : Virtual Private Network, réseau privé qui permet de sécuriser la connexion entre des sites distants.
- *GPS* : Global Positioning System, système de navigation par satellite.

## 3.8 -  implement authentication and authorization solutions

**Authentication management (Gestion de l'authentification)** : Processus de vérification de l'identité d'un utilisateur, d'un système ou d'une application.

- **Password keys (Clés de mot de passe)** : Clés générées à partir de mots de passe pour l'authentification.
  *Informations* : Ces clés offrent un moyen plus sécurisé d'authentification que les simples mots de passe.
  *Technique* : Souvent utilisées en combinaison avec des algorithmes de chiffrement*.

- **Password vaults (Coffres-forts de mots de passe)** : (**BitWarden**) Outils pour stocker et gérer les mots de passe.
  *Informations* : Ils aident à sécuriser et organiser les mots de passe, réduisant le risque d'oubli ou d'exposition.

- **TPM (Trusted Platform Module)** : **Hardware intégré à la carte mère d'un ordinateur**, pour stocker des informations de sécurité comme les clés.
  *Informations* : Elle renforce la sécurité en offrant un stockage sécurisé et des fonctions cryptographiques.

- **HSM (Hardware Security Module)** : Dispositif physique qui gère, génère et stocke des clés cryptographiques.
  *Technique* : Utilisé par les entreprises et les infrastructures à clé publique (PKI)* pour renforcer la sécurité.

- **Knowledge-based authentication (Authentification basée sur la connaissance)** : Authentification basée sur ce que l'utilisateur sait, comme les questions de sécurité.
  *Technique* : Souvent utilisé comme second facteur ou pour la récupération de compte.

**Authentication/authorization (Authentification/autorisation)** : Processus de vérification de l'identité et d'attribution des droits.

- **EAP (Extensible Authentication Protocol)** : Protocole d'authentification utilisé dans les réseaux sans fil. utilisé pour WPA2.
  Lorsqu'un employé tente de se connecter au réseau Wi-Fi d'une entreprise, il pourrait être invité à entrer un nom d'utilisateur et un mot de passe. Cette authentification est souvent gérée par EAP avec un serveur RADIUS en arrière-plan

- **Challenge-Handshake Authentication Protocol (CHAP)** : Protocole d'authentification où le serveur envoie un défi à l'utilisateur (penser à un captcha).
  *Informations* : Protège contre les attaques de replay* en utilisant un défi variable.

- **Password Authentication Protocol (PAP)** : (**nul**, username/password) Protocole d'authentification simple où le mot de passe est envoyé en texte clair.
  *Informations* : Moins sécurisé car le mot de passe peut être intercepté.

- <mark class="hltr-blue">IEEE 802.1X</mark> : (Contrôle, Accès, Réseau, utilise EAP) (Connexion dans une **bibliotheque** avec username & MDP = **IEEE 802.1X** qui contrôle l'accès au réseau en vérifiant vos identifiants via un serveur d'authentification central (comme un serveur **RADIUS**)) Utilisé pour l'authentification sur des réseaux tels que les réseaux LAN ou WLAN, il controle les accès.

- **RADIUS**: (Serveur, Authentification, Centralisé.) Le serveur qui vérifie les informations d'identification de l'utilisateur.

- **Single sign-on (SSO)** : (**Federation**, 1 login = Gmail, maps, drive...) Méthode d'authentification permettant de se connecter une seule fois pour accéder à plusieurs applications.
  Dans une université, un étudiant pourrait se connecter une fois à son portail étudiant et avoir accès à son emploi du temps, sa plateforme d'e-learning et d'autres ressources sans avoir à se reconnecter.

- **Security Assertion Markup Language (SAML)** : (SSO, XML, Échange) Format XML pour échanger des données d'authentification et d'autorisation entre deux parties (par exemple, entre un fournisseur d'identité et un fournisseur de services). Concu pour le SSO 

- **Terminal Access Controller Access Control System Plus (TACACS+)** : (Comme RADIUS mais plus secure et flexible) Protocole de contrôle d'accès distant pour les réseaux.
  *Informations* : Lorsqu'un utilisateur tente de s'authentifier, le client envoie une requête au serveur TACACS+. Le serveur vérifie ensuite les informations d'authentification, autorise l'accès en fonction des permissions de l'utilisateur et suit toute l'activité de l'utilisateur pour la comptabilité.
  *Technique* : TACACS+ utilise le port TCP 49 pour communiquer avec le serveur d'authentification.

- **OAuth** : (Autoriser Notion a, autoriser Canva a...) Permet d'autoriser ou non une application à accéder à des ressources spécifiques sans connaitre nos IDs.
  *exemple:*
   - Si vous autorisez **Calendly à accéder à votre agenda Google**, c'est OAuth.
   - Lorsque vous autorisez une application à accéder à vos photos Google ou à publier sur votre compte Twitter, c'est OAuth2 en action.
   - Lorsque vous utilisez une application pour poster une photo sur votre compte Instagram sans donner à l'application votre mot de passe Instagram.
	

- **OpenID** : (Se connecter avec google, se connecter avec Github) Permet une authentification unifiée sur différentes applications.
  *Technique* : OpenID Connect est une couche d'identité simple construite sur OAuth 2.0.

**OAuth vs OpenID** : 
- **OAuth2** se concentre sur l'autorisation: "Quelles actions sont autorisées?"
- **OpenID Connect** se concentre sur l'authentification: "Qui êtes-vous?"
Dans la pratique, si vous cliquez sur "Se connecter avec Google" sur un site web, c'est probablement OpenID Connect qui est utilisé pour l'authentification, tandis qu'OAuth2 est utilisé en arrière-plan pour autoriser le site à accéder à certaines informations de votre compte Google.


- **Kerberos** : (**42**, ticket-based, SSO) Protocole d'authentification réseau qui utilise des billets (ticket-based) pour prouver l'identité.
  Kerberos uses a ticket-based system to provide SSO (Single Sign-On)
  functionality. You only need to authenticate once with Kerberos to gain access to multiple resources.

<mark class="hltr-blue">Access control models (Modèles de contrôle d'accès) </mark> : Méthodes utilisées pour déterminer les droits d'accès des utilisateurs à des ressources.
*Informations* : Ils garantissent que seuls les utilisateurs ou entités autorisés peuvent accéder aux ressources ou effectuer des actions.

- **ABAC** : Attribute-based access control (Attribut localisation, age, poste...)
  Contrôle d'accès basé sur des attributs ou des propriétés d'utilisateurs, d'environnements et de ressources.
  *Informations* : Donne des droits d'accès en fonction des attributs et des politiques.

- **RBAC** : Role-based access control (Selon ton poste dans l'entreprise)
  Attribue des droits d'accès en fonction du rôle de l'utilisateur.
  Dans une entreprise, un "gestionnaire des RH" pourrait avoir accès à des documents sensibles sur les employés, tandis qu'un "développeur" n'y aurait pas accès.

- **Rule-based access control (Contrôle d'accès basé sur les règles)** : Attribue des droits d'accès basés sur des règles ou des politiques spécifiques.
  *Informations* : Les accès sont accordés ou refusés selon des règles définies.
  *Technique* : Souvent utilisé dans les pare-feux pour autoriser ou refuser le trafic en fonction des règles.

- **MAC** : Mandatory Access Control (Etiquette, top secret, confidentiel)
  Utilise des étiquettes (labels) pour déterminer l'accès
  **LE PLUS SÉCURISÉ des ACCESS CONTROL**
  Dans les environnements gouvernementaux, un document classé "Top Secret" ne peut être accessible qu'aux personnes ayant une autorisation "Top Secret".

- **DAC** : Discretionary access control (fichier Google Drive, **je décide qui peux voir**)
  Le propriétaire de la ressource décide qui peut accéder à la ressource et quels droits ils peuvent avoir.
  Un utilisateur partageant un document sur Google Drive et choisissant qui peut le voir ou le modifier.

- **Conditional access (Accès conditionnel)** : Accès accordé en fonction des conditions définies, comme la localisation ou l'heure.
  *Informations* : Les conditions peuvent être basées sur une variété de facteurs, comme le type d'appareil ou le risque associé à une connexion.
  *Technique* : Souvent mis en œuvre dans les solutions d'accès à distance pour sécuriser les connexions des employés mobiles.

- **Privileged access management (Gestion des accès privilégiés)** : Solutions pour gérer et auditer les accès avec des droits élevés.
  *Informations* : Essentiel pour contrôler les comptes avec des droits étendus, comme les administrateurs.
  *Technique* : Les solutions comme CyberArk* ou BeyondTrust* offrent des capacités de gestion des accès privilégiés.

- **Filesystem permissions (Permissions du système de fichiers)** : (**chmod**) Droits définissant qui peut lire, écrire ou exécuter des fichiers.
  *Informations* : Permettent de contrôler l'accès aux fichiers sur un ordinateur ou un réseau.
  *Technique* : Les systèmes d'exploitation comme Linux* ou Windows* ont leurs propres mécanismes de gestion des permissions.

---

**Termes techniques** (mise à jour) :
- *Chiffrement* : Processus de conversion des informations en un code pour éviter les accès non autorisés.
- *LastPass* : Gestionnaire de mots de passe basé sur le cloud.
- *KeePass* : Gestionnaire de mots de passe open-source.
- *PKI* : Infrastructure à clé publique, ensemble de rôles, politiques et procédures pour gérer la création, la distribution et la révocation des clés et des certificats numériques.
- _Replay_ : Attaque où des données sont interceptées et retransmises pour un gain frauduleux.
- _Diameter_ : Protocole d'authentification, d'autorisation et de comptabilité, successeur de RADIUS.
- *CyberArk* : Solution de gestion des accès privilégiés.


## 3.9 - implement public key infrastructure

D'accord, je vais suivre la structure exacte que vous avez fournie :

---


**Certificat Numérique** : (Certificat SSL pour HTTPS (valide, révoqué, invalide...)) Fichier électronique qui fonctionne comme une carte d'identité numérique. Il est utilisé pour prouver l'identité d'une entité (que ce soit une personne, un serveur, un site web, ou même un dispositif) dans le monde numérique, en particulier pendant les communications sécurisées.
1. **Émission** :
    - Une entité (par exemple, un site web) demande un certificat auprès d'une autorité de certification (CA).
    - La CA vérifie l'identité de cette entité (ce processus varie selon la rigueur de la CA).
    - Une fois validée, la CA émet un certificat numérique pour l'entité.
2. **Utilisation** :
    - Lorsqu'un utilisateur visite ce site web, le serveur du site envoie son certificat numérique au navigateur de l'utilisateur.
    - Le navigateur vérifie le certificat : est-il expiré ? Est-il révoqué ? La signature correspond-elle à une CA de confiance ?
    - Si le certificat est valide, une connexion sécurisée est établie.
3. **Example :** 
```pem
-----BEGIN CERTIFICATE-----
MIIDXTCCAkWgAwIBAgIJAJC1HiIvGv5UMA0GCSqGSIb3DQEBCwUAMEUxCzAJBgNV
BAYTAkFVMRMwEQYDVQQIDApTb21lLVN0YXRlMSEwHwYDVQQKDBhJbnRlcm5ldCBX
9O8hU2fJomUyljUyFpZ1YndFJ3+d2/S5bBDb8M3p4bU4fKRHekVHg0GsIepEeNgV
5on/ZyETUExE1bC5+wT4YCLugjcikPzlI5jL1SCzoQEhqz1o+3qvlOEH4zihcEH2
qkSeqZXBZG0JbzU8iWr3hZ4N/UedMkGMoJ102WUyD/8/PhlvRJIKD9ZGpTAimKjB
Gz9ZK8WUX32yUBCIJk2ev183Lu630GG8Zk4I16q1+fOoPl3eMK1GCRBL7NKb8vma
xStapxV8Rh9jViPv2PsaZY32IFVX6IWWzRLJ6U/AwS7z2A5c7mJW9Eob2W9gA1W4
tw==
-----END CERTIFICATE-----
```

**Public key infrastructure (PKI) (Infrastructure à clés publiques)** : (Gérer les certificat numériques) Système pour la création, le stockage, la distribution et la vérification de certificats numériques.
_Informations_ : La PKI est essentielle pour établir des communications sécurisées sur Internet. Elle permet aux entités de prouver leur identité et de chiffrer les données.
_Technique_ : Repose sur des certificats numériques signés par des autorités de certification (CA*).

- **Key management (Gestion des clés)** : Processus par lequel les clés cryptographiques sont générées, distribuées, stockées, tournées et supprimées. Sans la clé appropriée, les données restent inaccessibles
	_Technique_ : Les clés doivent être stockées en toute sécurité, souvent dans des dispositifs physiques tels que les **HSM***

- **Certificate authority (CA) (Autorité de certification)** : Entité de confiance (organisation comme DigiCert) qui délivre et manage les certificats numériques.
	_Informations_ : Attestent de l'identité des entités et garantissent que les titulaires de certificats sont bien ceux qu'ils prétendent être.

- **Intermediate CA (CA intermédiaire)** : CA qui est certifiée par une CA racine et qui peut à son tour certifier d'autres entités.
	_Informations_ : Ils forment un pont entre les CA racines hautement sécurisées et les utilisateurs finaux, en émettant des certificats pour les utilisateurs finaux ou d'autres CA.
	_Technique_ : Dans une chaîne de certificats, les certificats intermédiaires lient un certificat d'utilisateur final à une CA racine de confiance.

- **Registration authority (RA) (Autorité d'enregistrement)** : Entité qui valide les demandes de certificat avant que la CA ne les signe.
	_Informations_ : sert d'intermédiaire, vérifiant les informations fournies par les demandeurs avant que les certificats ne soient délivrés.
	_Technique_ : Bien qu'il valide les informations, c'est la CA qui signe et émet le certificat.

- **Certificate revocation list (CRL)** : Liste des certificats révoqués par une CA.
	_Informations_ : Les certificats peuvent être révoqués pour diverses raisons, la compromission de la clé privée, le changement d'information dans le certificat, ou le retrait du certificat par le demandeur.
	_Technique_ : : Lorsqu'un client ou un serveur reçoit un certificat, il peut la vérifier pour s'assurer que le certificat n'a pas été révoqué.

- **Certificate attributes (Attributs de certificat)** : Informations contenues dans un certificat numérique. 
  _Technique_ : Des attributs courants incluent le Common Name (CN), la période de validité, l'algorithme de signature et l'extension du certificat.
    
- **Online Certificate Status Protocol (OCSP)** : Obtenir le statut de révocation d'un certificat en temps réel dans le navigateur web. 
  _Informations_ : Conçu pour être une **alternative plus rapide aux CRL**, permettant aux applications de vérifier l'état actuel d'un certificat sans télécharger une CRL complète. 
    
- **Certificate signing request (CSR)** : (Demande de signature de certificat) Demande envoyée à une CA pour obtenir un certificat signé. 
  _Technique_ : Généré à l'aide d'outils comme **OpenSSL**. Une fois signé par la CA, il devient un certificat numérique.
    
- **CN (Common Name)** : Attribut du certificat qui identifie le nom de l'entité. 
  _Informations_ : Pour les certificats SSL/TLS, le CN est généralement le nom de domaine.

---

**Types de certificats** :

- **Wildcard (Certificat générique)** : Certificat qui couvre tous les sous-domaines d'un domaine. 
  _Informations_ : Très utile pour les entreprises ayant de nombreux sous-domaines, car un seul certificat peut sécuriser tous ces sous-domaines. 
  _Technique_ : Un certificat pour `*.example.com` couvrirait `blog.example.com`, `store.example.com`, etc.
    
- **Subject alternative name (Nom alternatif du sujet)** : Certificat qui peut sécuriser plusieurs noms de domaine et sous-domaines. 
  _Informations_ : Permet aux entreprises de sécuriser plusieurs domaines avec un seul certificat, simplifiant la gestion.

- **Code signing (Signature de code)** : Certificat utilisé pour confirmer que le logiciel n'a pas été altéré depuis sa publication. 
  _Informations_ : Important pour garantir l'intégrité du logiciel et **assurer aux utilisateurs qu'ils téléchargent un logiciel légitime et non altéré**.
    
- **Self-signed (Auto-signé)** : Certificat qui n'est pas signé par une CA externe, mais plutôt par l'entité elle-même. 
  _Informations_ : Bien qu'ils puissent établir une connexion chiffrée, ils ne garantissent pas l'identité de l'entité, car il n'y a pas de tiers de confiance. _Technique_ : Souvent utilisés pour les environnements de test ou internes
    
- **Machine/computer (Machine/ordinateur)** : Certificat utilisé pour identifier une machine ou un ordinateur sur un réseau. _Informations_ : Aide à sécuriser les communications entre les machines et à garantir l'identité des machines sur un réseau.

- **Extended Validation (EV) Certificate** : (Domain Validation plus approfondi) Certificat SSL avec une vérification approfondie de l'entité demandant le certificat. Permettant d'obtenir le dabge HTTPS.
  Pour les Banques ou grandes entreprises qui veulent une confiance maximale avec leurs utilisateurs.

---

**Formats de certificat** :

- **Distinguished encoding rules (.der)** : **Format binaire pour les certificats.**
    
- **Privacy enhanced mail (.pem)** : (format clé ssh, --begin certificate--) Format texte pour les certificats, clés privées, et d'autres structures. 
  _Informations_ : L'un des formats les plus courants, souvent utilisé pour les certificats SSL/TLS.
```plaintext
-----BEGIN CERTIFICATE-----
...
(encoded data)
...
-----END CERTIFICATE-----
```

    
- **Personal information exchange (.pfx ou .p12)** : Format binaire utilisé pour stocker le certificat de serveur, les clés intermédiaires et la clé privée dans un seul fichier.
  **Usage**: Export et import de certificats et clés privées sur Windows.

- **.cer (Certificate File)** : (clés publiques) Format de fichier pour les certificats publics (clé publique).

- **.p7b** : Format utilisé pour stocker la chaîne de certificats mais pas les clés privées.
---

**Concepts** :

- **Online vs. offline CA (CA en ligne vs. hors ligne)** : Distingue si une CA est connectée (en ligne) ou non connectée (hors ligne) à un réseau.
  _Technique_ : Les CA racines sont souvent conservées hors ligne pour garantir leur sécurité, tandis que les CA intermédiaires sont en ligne pour émettre des certificats.
  
- **Stapling (Agrafage)** : Technique permettant à un serveur de fournir des preuves de validité d'un certificat lors de la connexion. 
  _Informations_ : Réduit la nécessité pour les clients de contacter la CA pour vérifier le statut du certificat, accélérant ainsi la négociation SSL/TLS. 
  _Technique_ : Le serveur obtient régulièrement une réponse OCSP* de la CA et la "agrafe" à la poignée de main SSL/TLS.
    
- **Pinning (Épinglage)** : Technique où les applications ou les navigateurs sont configurés pour associer un hôte à un certificat ou une clé publique spécifique. 
  _Informations_ : Augmente la sécurité en réduisant le risque d'attaques Man-in-the-Middle (MitM) avec des certificats frauduleux. 
  _Technique_ : Communément utilisé dans les applications mobiles pour éviter que des proxies malveillants ne fournissent des certificats invalides.
    
- **Trust model (Modèle de confiance)** : Système par lequel les utilisateurs et les appareils déterminent s'ils doivent faire confiance à un certificat. 
  _Technique_ : Les navigateurs et les systèmes d'exploitation sont livrés avec une liste de CA de confiance, mais cette liste peut être modifiée par l'utilisateur ou l'administrateur.
    
- **Key escrow (Conservation de clé)** : (copie de clés, backup) Processus par lequel une copie d'une clé cryptographique est stockée de manière sécurisée. 
  _Informations_ : Utilisé pour récupérer des données si la clé originale est perdue ou pour des raisons légales (par exemple, les enquêtes gouvernementales).
    
- **Certificate chaining (Chaînage de certificats)** : Processus par lequel un certificat est lié à une CA racine de confiance par l'intermédiaire de certificats intermédiaires. 

---
**Termes Techniques** :

- _CA (Certificate Authority)_ : Entité qui émet et gère les certificats numériques, servant de "tiers de confiance".
- _OCSP (Online Certificate Status Protocol)_ : Protocole utilisé pour obtenir le statut de révocation d'un certificat en temps réel.

