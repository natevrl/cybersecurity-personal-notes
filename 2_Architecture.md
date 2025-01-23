# <mark class="hltr-green">2.0 Architecture and Design 21%</mark>

## 2.1 - Security concepts in an enterprise environment

**Configuration management**: Processus de gestion et de contrôle des configurations des systèmes, des réseaux et des logiciels pour assurer leur cohérence, leur sécurité et leur conformité.

- **Diagrams**: Ce sont des représentations graphiques des configurations des systèmes et des réseaux pour faciliter leur compréhension et leur gestion.
    
- **Baseline configuration**: (Config de base) **Configuration de référence sécurisée** qui sert de modèle pour les autres systèmes.
    
- **Standard naming conventions**: Ce sont des règles et des normes pour donner des noms cohérents aux éléments d'un réseau.
    
- **Internet protocol (IP) schema**: C'est un plan d'adressage IP qui définit la manière dont les adresses IP sont attribuées aux différents appareils sur un réseau.

**Data sovereignty (souveraineté des données)**: (Comment les datas sont soumises aux lois du pays où elles sont stockées). Principe selon lequel les données sont soumises aux lois et réglementations du pays dans lequel elles sont stockées.

**Data protection**: Ensemble des mesures prises pour protéger les données contre les accès non autorisés, les fuites ou les pertes.

- **DLP (Data Loss Protection)**: Solutions pour empêcher la fuite de données sensibles.
	  _Informations_: Détecte et bloque les transferts non autorisés de données.
	  _Technique_: Peut être basé sur des règles, des empreintes digitales de données ou des modèles de comportement.
	- **Exemples** de mesures : (Surveillance et blocage des e-mails, Contrôle des périphériques de stockage...)

- **Masking**: Technique de remplacement de données réelles par des données fictives dans un environnement de test ou de développement.
    
- **Encryption (chiffrement)**: Processus de conversion de données en un format illisible pour protéger leur confidentialité. **Contrairement à la tokenisation, le chiffrement est réversible**, ce qui signifie que les données d'origine peuvent être déchiffrées à l'aide de la clé de déchiffrement appropriée.

- **Tokenization**: Consiste à remplacer des données sensibles par des tokens uniques. Ces tokens servent de substituts aux données réelles. Le processus de tokenisation est irréversible, ce qui signifie que les données d'origine ne peuvent pas être récupérées à partir du token. (**contrairement au chiffrement** via des algortihme mathematiques)

- **data At rest**: Lorsque les données sont stockées sur un support de stockage.
- **data In transit/motion**: Lorsque les données sont en déplacement sur un réseau.
- **data In processing**: Lorsque les données sont en cours de traitement par un système.

- **Rights management**: C'est le contrôle des droits d'accès aux données pour s'assurer que seules les personnes autorisées peuvent y accéder.

**Geographical considerations**: C'est la prise en compte des aspects géographiques dans la conception et la gestion des systèmes, tels que la localisation des datas centers et les réglementations locales.

**Response and recovery controls**: Ce sont les mesures mises en place pour répondre aux incidents de sécurité et pour assurer la reprise des opérations après un incident.

**Secure Sockets Layer (SSL)/Transport Layer Security (TLS) inspection**: C'est l'inspection du trafic chiffré SSL/TLS pour détecter et prévenir les menaces.

**Hashing**: C'est le processus de conversion de données en une valeur de hachage fixe, utilisée notamment pour vérifier l'intégrité des données. (SHA256, MD5)

**API considerations**: Ce sont les mesures de sécurité à prendre en compte lors de la conception et de l'utilisation d'API (interfaces de programmation d'applications).

**Site resiliency**: Ce sont des sites de secours configurés pour assurer la continuité des opérations en cas de sinistre.
- **Hot site**: Un site de secours entièrement opérationnel et prêt à l'emploi en cas de sinistre.
- **Cold site**: Un site de secours vide sans équipements actifs, qui nécessite une configuration avant de devenir opérationnel.
- **Warm site**: Un site de secours partiellement équipé, nécessitant une configuration supplémentaire avant d'être pleinement opérationnel.

**Deception and disruption**:
- **Honeypots**: Ce sont des systèmes ou des réseaux factices conçus pour attirer les attaquants et les garder occupés loin des systèmes réels.
    
- **Honeyfiles**: Ce sont des fichiers fictifs placés dans des dossiers sensibles pour attirer les attaquants.
    
- **Honeynets**: Ce sont des réseaux isolés et factices conçus pour attirer et surveiller les activités des attaquants.
    
- **Fake telemetry**: C'est la diffusion de fausses données pour tromper les attaquants sur les activités du système.
    
- **DNS sinkhole**: (Redirection DNS vers fake IP) C'est une technique pour rediriger le trafic DNS malveillant vers une adresse IP inexistante ou contrôlée.


## 2.2 - Virtualization and cloud computing concepts



<mark class="hltr-blue">Cloud models</mark> :
- **Infrastructure as a service (IaaS)** (Infrastructure en tant que service) : Fournit des ressources informatiques virtualisées via Internet, telles que des machines virtuelles, du stockage et des réseaux. (**AWS, Azure, GCP**)

- **Platform as a service (PaaS)** (Plateforme en tant que service) : (Développement, Cloud) Environnements de développement et d'hébergement dans le cloud pour construire, tester et déployer des applications. (**Heroku, RedHat OpenShift**, **Google App Engine**)

- **Software as a service (SaaS)** (Logiciel en tant que service) : 
 Propose des applications logicielles via Internet en abonnement, éliminant ainsi le besoin d'installation et de maintenance locale. (**Mailchimp, system.io, O365, slack**)

- **Anything as a service (XaaS)** (Tout en tant que service) : Regroupe différentes offres de services cloud, dont IaaS, PaaS, SaaS ou d'autres types de services.

- **Public cloud** (Cloud public) : (**AWS, Google, Azure**) Services fournis via Internet par des fournisseurs tiers et accessibles à tous.

- **Community cloud** (Cloud communautaire) : Infrastructure partagée entre des organisations ayant des intérêts ou des exigences communes.

- **Private cloud** (Cloud privé) : (pas accessible à tous) Cloud sur internet ou réseau interne mais selectionne ses clients 

- **Hybrid cloud** (Cloud hybride) : Combine deux ou plusieurs modèles de déploiement cloud (public, privé, communautaire) qui restent des entités distinctes mais sont liés par la technologie.

**Cloud service providers** (Fournisseurs de services cloud) : Entreprises proposant des services cloud, tels qu'Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform (GCP), etc.

**Managed service provider (MSP) / <mark class="hltr-blue">managed security service provider (MSSP)</mark>** (Fournisseur de services gérés / fournisseur de services de sécurité gérés) : Entreprises qui fournissent des services informatiques et cybersécurité, pour d'autres organisations. (**Accenture, Trustwave**)

**On-premises vs. off-premises** (Sur site vs. hors site) : Réfère à l'endroit physique où se trouvent les ressources ou les services, avec "on-premises" étant dans l'infrastructure de l'organisation elle-même et "off-premises" étant hébergé à l'extérieur, souvent dans un environnement cloud.
<mark class="hltr-blue">EXAM TIPS</mark> : A poorly implemented security model at a physical location will still be a poorly implemented security model in a cloud location. 

**Fog computing** (Informatique en brouillard) : (Réduction latence, intermédiaire entre le réseau local et le cloud) Fog = brume, donc plus proche que le cloud (nuage). Le fog computing offre une approche plus distribuée que le **Edge computing**, traitant les données à différents niveaux entre la source et le cloud central.

**Edge computing** (Informatique en périphérie) : (Réduction latence, local, traitement des données) Similaire à la fog computing mais traite les données localement , et seules les données pertinentes ou nécessaires peuvent être envoyées au centre de données central.
exemple : Un exemple courant serait une caméra de sécurité intelligente qui utilise l'"edge computing" pour analyser les images. Au lieu d'envoyer chaque image capturée à un centre de données pour analyse, la caméra elle-même analyse les images, détecte si une personne est présente et n'envoie des données au centre que lorsqu'une activité suspecte est détectée.

**Thin client** (Client léger) : (Minimaliste, Dépendant, Économique) Un ordinateur léger qui s'appuie sur un serveur central pour le traitement et le stockage.

**Containers** (Docker/kurbernetes) : Environnements légers, portables et autonomes qui regroupent une application et ses dépendances, permettant un déploiement cohérent sur différents environnements.

**Microservices/API** (Microservices/Interface de programmation d'applications) : Approche architecturale consistant à créer des applications sous forme de petits services indépendants qui communiquent via des API.

**Infrastructure as code** (Infrastructure en tant que code) : Pratique de gestion et de provisionnement de l'infrastructure par le biais de code et d'automatisation.

- **Software-defined networking (SDN)** : (Flexible, Centralisé, Programmable.) 
  Avec le SDN, le réseau peut être programmé pour s'adapter automatiquement à l'augmentation du trafic, en dirigeant les ressources là où elles sont le plus nécessaires

- **Software-defined visibility (SDV)**: Contrôle centralisé et programmable de la visibilité sur les réseaux pour la surveillance et la sécurité.

**Serverless architecture** (Architecture sans serveur) : (Firebase) Un modèle d'exécution en cloud où le fournisseur cloud gère l'infrastructure et alloue automatiquement les ressources pour exécuter les applications.

**Services integration** (Intégration des services) : Processus de combinaison de différents services cloud ou applications pour qu'ils fonctionnent ensemble de manière transparente.

**Resource policies** (Politiques de ressources) : Ensemble de règles et d'autorisations définissant comment les ressources cloud peuvent être accédées et utilisées.

**Transit gateway** (Passerelle de transit) : Un hub de transit réseau qui relie plusieurs réseaux privés virtuels (VPC) et réseaux locaux.

**Virtualization** (Virtualisation) : Le processus de création d'une version virtuelle (basée sur un logiciel) d'une ressource, telle qu'un ordinateur, un serveur, un réseau ou un système d'exploitation, pour permettre l'exécution de plusieurs instances ou environnements sur le même matériel physique.

**Virtual Machine (VM)** :
- <mark class="hltr-blue">Hypervisor</mark> : (VMWare ou VirtualBox)virtual machine monitor, is a process that creates and runs virtual machines (VMs).

- **Virtual machine (VM) sprawl avoidance** : (Controler les VM contre la création excessive) la pratique de gérer et de limiter la création excessive et non réglementée de machines virtuelles dans un environnement de virtualisation.
    
- **VM escape protection**: Mesure de sécurité qui empêche un utilisateur ou un logiciel malveillant de s'échapper d'une machine virtuelle pour accéder à l'hôte sous-jacent ou à d'autres VM.

## 2.3 - Secure application development, deployment, and automation concepts. 

**Environment** (Environnement) :
- **Development** (Développement) : Où les développeurs créent et testent le code d'application.
- **Test** (Test) : Où les tests sont effectués pour s'assurer que l'application fonctionne correctement.
- <mark class="hltr-blue">Staging</mark>  (Staging) : Un environnement de pré-production pour simuler la production avant le déploiement.
- **Production** (Production) : L'environnement de déploiement réel où l'application est utilisée par les utilisateurs finaux.
- **Quality assurance (QA)** (Assurance qualité) : Où les tests de qualité sont effectués pour s'assurer que l'application répond aux exigences.

**Provisioning and deprovisioning**  : Attribution et Retrait de Ressources necessaires.

**Integrity measurement** (Mesure d'intégrité) : (check for the secure baseline) Le processus de vérification de l'intégrité du code et des données pour s'assurer qu'ils n'ont pas été modifiés de manière non autorisée.
check for the secure baseline of firewall settings, patch levels, operating system versions, and any other
security components associated with the application. 

**Secure coding techniques** (Techniques de codage sécurisé) :

- **Normalization** (Normalisation) : En normalisant on élimine les redondances des données, ce qui permet de réduire les risques d'incohérences et d'erreurs
```sql

-- not normalized code
CREATE TABLE clients (
    id INT PRIMARY KEY,
    nom VARCHAR(50),
    adresse VARCHAR(100),
    ville VARCHAR(50),
    code_postal VARCHAR(10),
    telephone VARCHAR(15),
    email VARCHAR(100),
    commande1 VARCHAR(100),
    commande2 VARCHAR(100),
    commande3 VARCHAR(100)
);

-- normalized code
CREATE TABLE clients (
    id INT PRIMARY KEY,
    nom VARCHAR(50),
    adresse_id INT,
    telephone VARCHAR(15),
    email VARCHAR(100)
);

CREATE TABLE adresses (
    id INT PRIMARY KEY,
    adresse VARCHAR(100),
    ville VARCHAR(50),
    code_postal VARCHAR(10)
);

CREATE TABLE commandes (
    id INT PRIMARY KEY,
    client_id INT,
    commande VARCHAR(100)
);
```

- **Stored procedures** (Procédures stockées) : Les stored procedures sont des blocs de code SQL (et parfois d'autres langages de programmation) qui sont stockés dans la base de données pour exécuter des opérations sur la base de données plutôt que du code directement dans l'application.
```sql
-- creation de la stored procedure
DELIMITER //
CREATE PROCEDURE GetEmployee(IN employeeId INT)
BEGIN
    SELECT * FROM employees WHERE id = employeeId;
END //
DELIMITER ;


-- on appel la Stored procedure
CALL GetEmployee(101);

```


- **Obfuscation/camouflage** (Obfuscation/camouflage) : Dissimuler le code source pour rendre difficile la compréhension par des tiers non autorisés.
```python
# code simple
def add(a, b):
    result = a + b
    return result

x = 5
y = 10
sum = add(x, y)
print(sum)
```

```python

# code obfusqué (difficile a comprendre)
a0a = 7
a0b = 12

def a1a(a1b, a1c):
    a1d = a1b + a1c
    return a1d

a2a = a1a(a0a, a0b)
print(a2a)
```

- **Code reuse/dead code** (Réutilisation de code/code mort) : Éviter la réutilisation de code non utilisé (code mort) pour réduire les vulnérabilités potentielles.

- **Server-side vs. client-side execution and validation** : Limiter les traitements et les validations côté client pour éviter les manipulations malveillantes.

- **Memory management** (Gestion de la mémoire) : Assurer une gestion sécurisée de la mémoire pour prévenir les attaques de type **buffer overlow, memory leak**.

- **Use of third-party libraries and software development kits (SDKs)** (Utilisation de bibliothèques tierces et kits de développement logiciel (SDK)) : S'assurer de la sécurité des bibliothèques et SDK utilisés pour éviter les vulnérabilités.

- **Data exposure** (Exposition des données) : Protéger les données sensibles pour éviter les fuites d'informations.

• **Open Web Application Security Project (OWASP)** (Projet de sécurité des applications Web ouvertes) : Une organisation fournissant des ressources et des outils pour aider au développement d'applications Web sécurisées.

**Software diversity** (Diversité des logiciels) :
- **Compiler** (Compilateur) : Utiliser différents compilateurs pour éviter les attaques ciblant un compilateur spécifique.
- **Binary** (Binaire) : Utiliser différentes versions binaires pour éviter les attaques ciblant une version spécifique.

 **Automation/scripting** (Automatisation/scripting) :
- **Automated courses of action** (Actions automatisées) : Automatiser des actions de sécurité en réponse aux événements.
- **Continuous monitoring** (Surveillance continue) : Surveiller en permanence et de manière automatisé les environnements pour détecter les incidents de sécurité.
- **Continuous validation** (Validation continue) : (Vérifier et Assurer la Qualité via tests (unitaires etc.))
  Processus de vérification régulière et automatisée que les programmes fonctionnent comme prévu
  Automatiser via **tests unitaires, des tests d'intégration**...
- **Continuous integration** (Intégration continue) : (Git Merge, main branch, automatiser)
  Les développeurs intègrent leur travail fréquemment, généralement plusieurs fois par jour puisdes tests sont déclenchés pour vérifier l'intégration.
- **Continuous delivery** (Livraison continue) : (Déployer Directement sur Décision, manuellement) Garantit que le code est toujours dans un état prêt à être déployé, mais le déploiement lui-même est déclenché manuellement.
- **Continuous deployment** (Déploiement continu) : (Déploiement automatique sans intervention manuelle, plus rapide, faire confiance aux tests)
  Le *** continu va un pas plus loin que la livraison continue, chaque changement validé dans le code base est automatiquement déployé en production sans intervention humaine.

**Elasticity** (Élasticité) : La capacité d'ajuster automatiquement les ressources pour répondre à la demande croissante ou décroissante. 
Par exemple, si une application web connaît une augmentation soudaine de trafic en raison d'une campagne marketing, un système élastique pourra automatiquement augmenter ses ressources de calcul (par exemple, machines virtuelles ou conteneurs) pour faire face à la charge accrue. Une fois que le trafic revient à la normale, le système réduira automatiquement ses ressources pour économiser des coûts.

**Scalability** (Évolutivité) : La capacité d'un système à gérer une augmentation de la charge de travail, du trafic ou des données, sans compromettre les performances.
- **Scalabilité verticale (Vertical Scalability)** : augmenter la capacité d'une ressource unique (processeur, RAM)
- **Scalabilité horizontale (Horizontal Scalability)** :Consiste à ajouter plus de ressources, comme des serveurs supplémentaires ou des nœuds, 

**Version control** (**GIT**) : Contrôle de version pour gérer les modifications du code et collaborer en équipe.


## 2.4 - Authentication and authorization design concepts

**Authentication methods** (Méthodes d'authentification) :

- **Directory services** (Services d'annuaire) : (**Microsoft Active Directory**) Utilisés pour stocker et gérer les informations d'identification des utilisateurs au sein d'une organisation (**MDP, PRIVILEGES...**)

- **Federation** (Fédération) : (**Connectez-vous avec Google**) Permettre l'authentification auprès d'un fournisseur d'identité tiers.

- **Attestation** (Attestation) : Le processus de vérification de l'identité d'un utilisateur ou d'un appareil. (Ex : Lorsqu'un appareil se connecte à un réseau Wi-Fi sécurisé, **l'accès peut être restreint jusqu'à ce que l'appareil fournisse un certificat numérique valide**, attestant de son appartenance à l'organisation.)

- **Technologies** (Technologies) :
    - **TOTP** : (Time-based one-time password) Génère des mots de passe uniques qui expirent après une certaine période de temps. (**Google Authenticator**)
      Lorsque Google me donne 30sec pour lui donner 6 chiffres recu par message
    - **HOTP** : (HMAC-based one-time password) (Moins populaire de TOTP, Incrementation, **moins sécurisé car reste actif**) Contrairement au TOTP, le HOTP utilise une fonction de hachage HMAC (Hash-based Message Authentication Code) avec un compteur qui s'incrémente coté serveur pour générer les mots de passe uniques. Moins sécurisé que TOTP car le code reste ne s'expire pas
    - **Short message service (SMS)** (Service de messagerie courte) : Envoi de codes d'authentification via SMS.
    - **Token key** (Clé de jeton) : Utilisation de jetons matériels (**cle usb avec ecran**) ou logiciels pour générer des codes d'authentification. **Moins courant mais utile dans les secteurs hautement sensible comme la banque**
    - **Static codes** (Codes statiques) : (**Desjardins, activement carte credit**, **pas sécurisé car statique**) codes d'authentification pré-définis qui sont utilisés pour l'authentification. Ces codes sont généralement fournis à l'utilisateur au préalable et restent inchangés jusqu'à leur révocation ou leur expiration.
    - **Authentication applications** : (Authy) Utilisation d'applications mobiles pour générer des codes d'authentification.
    - **Push notifications** (Notifications push) : Envoi de notifications aux appareils mobiles pour l'authentification.
    - **Phone call** (Appel téléphonique) : Utilisation d'un appel téléphonique pour l'authentification.
- **Smart card authentication** : (Carte bancaire) Utilisation de cartes à puce physique pour l'authentification.

**Biometrics** (Biométrie) : L'utilisation de caractéristiques physiques ou comportementales uniques pour l'authentification.

- **Fingerprint** (Empreinte digitale)
- **Retina** (Rétine) : Retina se concentre sur le motif des vaisseaux sanguins à l'arrière de l'œil. Invasif, reservé pour la haute sécurité
- **Iris** (Iris) : Iris se concentre sur la partie colorée de l'œil. Moins Invasif que Retina et beaucoups plus utilisé
- **Facial** (Faciale) : mesure la **distance** entre les yeux, le nez...
- **Voice** (Voix)
- **Vein** (Veines)
- **Gait analysis** : (Analyse de la démarche, auth biomectric) Analyse du mouvement de marche d'une personne.
- **Efficacy rates** (Taux d'efficacité) : Mesure de la précision d'une méthode de biométrie.
- **False acceptance** (Acceptation fausse) : Erreur d'authentification où une personne non autorisée est acceptée.
- **False rejection** (Rejet fausse) : Erreur d'authentification où une personne autorisée est rejetée.
- **Crossover error rate** (Taux d'erreur de croisement) : Le point où les taux d'acceptation fausse et de rejet fausse sont égaux.

• **Multifactor authentication (MFA) factors and attributes** (Facteurs et attributs d'authentification multifactorielle) :

- **Factors** (Facteurs) :
    - **Something you know** (Quelque chose que vous savez) : Comme un mot de passe ou un code PIN.
    - **Something you have** (Quelque chose que vous avez) : Comme un jeton physique, un téléphone portable **ou une ID**.
    - **Something you are** (Quelque chose que vous êtes) : Comme une caractéristique biométrique (**retina, fingerprint, vocal**...).
- **Attributes** (Attributs) :
    - **Somewhere you are** (Lieu où vous êtes) : Vérification basée sur l'emplacement de l'utilisateur (**Addresse IP, coord GPS...**).
    - **Something you can do** (Quelque chose que vous pouvez faire) : Vérification basée sur les actions de l'utilisateur (**gestes sur un écran tactile, repondre a des questions**...).
    - **Something you exhibit** (Quelque chose que vous présentez) : Vérification basée sur les comportements de l'utilisateur (**vitesse de frappe, les habitudes de navigation**).
	    - Exemple concret : Certaines applications de sécurité peuvent analyser vos habitudes de navigation sur leur site web pour détecter tout comportement suspect qui pourrait indiquer une activité non autorisée.
    - **Someone you know** (Quelqu'un que vous connaissez) : Vérification basée sur la connaissance d'une autre personne. (**questions personnelles auxquelles seuls vous et une personne de confiance connaissez les réponses.**)

**Authentication, authorization, and accounting (AAA)** (Authentification, autorisation et comptabilité) : Un cadre pour contrôler l'accès aux ressources et enregistrer les activités des utilisateurs.
	1. **Authentication (Authentification)** : vérifier l'identité d'un utilisateur  (ID, MDP, SMS Auth).
	2. **Authorization (Autorisation)** : Après l'authentification réussie, déterminer quelles ressources, données ou fonctionnalités l'entité authentifiée est autorisée à accéder. (**droits et privilèges**)
	3. **Accounting (Comptabilité)** : La collecte et l'enregistrement des informations sur les activités de l'entité authentifiée (**heures de connexion des employés**...).

• **Cloud vs. on-premises requirements** (Exigences du cloud par rapport à celles sur site) : Les différences dans les exigences de sécurité entre les environnements cloud et sur site.


## 2.5 - Implement cybersecurity resilience


**Redundancy** : (Redondance) Avoir des doublons ou des alternatives en cas de défaillance.
- **Geographic dispersal (Disparité géographique)** : Éloigner les systèmes ou les données à des endroits géographiquement différents pour les protéger contre des incidents majeurs.
- **Disk (Disque)** : Le stockage physique des données.
    - **Redundant array of independent (or inexpensive) disks (RAID) levels (Niveaux de RAID - Matrice redondante de disques indépendants ou bon marché)** : Technologie de stockage qui permet de combiner plusieurs disques durs physiques en un seul groupe logique pour améliorer les performances, la redondance et la résilience des données.

    - **Multipath (Multipath)** : également appelé MPIO (Multipath Input/Output). Lorsqu'un système utilise le multipath, il peut disposer de plusieurs chemins physiques pour accéder à un même dispositif de stockage. Ces chemins peuvent être constitués de câbles, de commutateurs, de contrôleurs ou de liaisons réseau, et ils offrent des routes alternatives pour les opérations de lecture et d'écriture de données.
			       ![[F13-01.jpg|300]]
-  **Network (Réseau)** : Un ensemble d'appareils connectés qui communiquent entre eux.
        - **Load balancers** : (Répartiteur de charge) Distribuer équitablement la charge de travail sur plusieurs serveurs pour éviter les surcharges.
        - **Network interface card (NIC) teaming (Association de cartes réseau)** : Regrouper plusieurs cartes réseau pour améliorer les performances et la redondance.

    - **Power (Alimentation)** : Fournir de l'électricité aux appareils.
        - **Uninterruptible power supply (UPS) (Alimentation sans interruption)** : (Boitier physique) qui fournis une alimentation de secours en cas de coupure électrique.
        - **Generator (Générateur)** : Source d'alimentation de secours à partir d'un générateur électrique.
        - **Dual supply (Alimentation double)** : Utiliser deux sources d'alimentation pour assurer la redondance.
        - **Managed power distribution units (PDUs) (Unités de distribution d'alimentation gérées)** : (**une multi-prise avec des fonctions de securite supplementaire**) Distribuer l'alimentation électrique aux équipements informatiques

**Replication (Réplication)** : Faire des copies identiques de données ou de systèmes.
    - **Storage area network (SAN) (Réseau de stockage)** : Un réseau dédié pour le stockage des données (on y connecte des dispositifs de stockage (HDD, des baies de stockage...) à des serveurs.
    - **VM (Machine virtuelle)** : Un environnement informatique émulé à partir d'un ordinateur physique. **Exemple** : Une VM (on y connecte des dispositifs de stockage (comme des disques durs, des baies de stockage ou des unités de stockage) à des serveurs exécutant une application critique peut être répliquée sur un autre serveur physique du cluster.

**On-premises vs. cloud (Sur site vs. cloud)** : Comparaison entre le stockage des données localement ou dans le cloud.

**Backup types (Types de sauvegarde)** : Différents moyens de sauvegarder les données.

- **Full** : (Sauvegarde complète, le plus lourd, le plus de temps) Copier toutes les données à chaque sauvegarde (y compris les données qui ont déjà été sauvegardées précédemment).
  **Temps de restauration**: Plus rapide car tout provient d'une seule source.

- **Incremental** : (Rapide, Cumulatif)Sauvegarde que les données qui ont changé depuis la dernière sauvegarde, qu'elle soit **complète ou incrémentielle**.
  **Temps de restauration** : Plus lent que full car il faut restaurer la sauvegarde complète suivie de toutes les sauvegardes incrémentielles.

-  **Differential** : (**Depuis-complet**, Intermediaire) Copier les données modifiées depuis la dernière sauvegarde complète.
  **Temps de restauration**: Plus rapide que l'incrémentielle, car elle nécessite seulement la dernière sauvegarde complète et la dernière sauvegarde différentielle.

- **Snapshot** : Capture d'un état spécifique d'une **VM** à un moment donné.

- **Tape (Sauvegarde sur bande)** : Stockage de sauvegarde sur bande magnétique. (utilisées pour les sauvegardes à **long terme** et les archives en raison de leur capacité de **stockage élevée**.)

- **Disk (Sauvegarde sur disque)** : Stockage de sauvegarde sur disque dur. (**plus rapides** que les sauvegardes sur **Tape** et sont utilisées pour les sauvegardes plus fréquentes et les récupérations rapides.)
  Nécessitant de parcourir toute la bande pour trouver des données spécifiques.

- **Copy (Copie)** : Dupliquer/copier les données pour la sauvegarde.

- **Network-attached storage (NAS) (Stockage connecté au réseau)** : Stockage de données partagé sur le réseau grâce a un NAS.

- **Cloud (Sauvegarde dans le cloud)** : Stockage de sauvegarde dans le cloud.

- **Image (Image)** : (Utile pour non-persistence) (Snapshot version système) Une copie complète d'un système ou d'un disque.

- **Online vs. offline (En ligne vs. hors ligne)** : Disponibilité ou accessibilité des sauvegardes. (Les sauvegardes en ligne sont accessibles en temps réel via le réseau, tandis que les sauvegardes hors ligne sont stockées sur des supports physiques)

- **Offsite storage (Stockage externe)** : Stockage des sauvegardes en dehors de l'emplacement principal (protection contre les sinistres ou les catastrophes).
	- **Distance considerations (Considérations de distance)** : Prendre en compte la distance pour le stockage externe (éviter que les mêmes événements ou catastrophes n'affectent à la fois le site principal et le site de sauvegarde.).

**Non-persistence (Non-persistance)** : (Navigation privée, temporaire, réinitialisé) La non-persistence fait référence à un état où les données ou les configurations ne sont pas conservées au-delà de la session actuelle.
    - **Revert to known state (Revenir à un état connu)** : Retourner à un état stable et connu du système.
    - **Last known-good configuration (Dernière configuration connue stable)** : Revenir à la dernière configuration stable connue du système (Ex : si un système rencontre un problème lors du démarrage).
    - **Live boot media (Média de démarrage en direct)** : Utilisation d'un périphérique de démarrage pour exécuter un système d'exploitation sans installation permanente.

**High availability (Haute disponibilité)** : Assurer la disponibilité continue des systèmes et des services.
    - **Scalability (Scalabilité)** : Capacité à s'adapter à des charges de travail croissantes.

**Restoration order (Ordre de restauration)** : Séquence pour restaurer les systèmes ou les données après une panne.

**Diversity (Diversité)** : Utiliser des technologies, fournisseurs ou contrôles différents pour améliorer la sécurité.

## 2.6 - Embedded and specialized systems. (Système embarqués)

**Systèmes embarqués** :Systèmes informatiques intégrés dans des dispositifs ou appareils pour fournir des fonctionnalités particulières.
- **Raspberry Pi** : Un petit ordinateur monocarte utilisé pour divers projets.
- **Field-programmable gate array (FPGA)** :Un circuit intégré qui peut être reconfiguré après sa fabrication pour effectuer différentes tâches spécialisées.
- **Arduino** : Une plateforme de développement de microcontrôleurs pour des projets électroniques.

**SCADA/ICS : Supervisory control and data acquisition & industrial control system** :
(Surveillance, Industriel, Automatisation). Systèmes utilisés pour contrôler et surveiller des processus industriels à grande échelle
- **Facilities, Industrial, Manufacturing, Energy, Logistics** : Secteurs où les SCADA/ICS sont utilisés. (Exemple : surveiller et contrôler les centrales électriques, chauffage, de ventilation et de climatisation (CVC), équipements industriels, robots, convoyeurs...)

**Internet of Things (IoT)** : Les appareils connectés

- **Sensors (capteurs)** : Des dispositifs qui détectent et transmettent des informations. (température, l'humidité, la lumière, le mouvement, etc)
- **Smart devices** : Des appareils intelligents connectés à Internet (smartphone, smart TV...). 
- **Wearables** : Des dispositifs électroniques portables (smartwatches, fitness tracker...).
- **Facility automation** : L'automatisation des systèmes dans des bâtiments, des installations, des usines... (contrôle des éclairages, du chauffage, de la climatisation, de la sécurité, etc., pour améliorer l'efficacité énergétique et la commodité.)
- **Weak defaults (Paramètres par défaut faibles)** : Risque de sécurité lorsque les appareils IoT utilisent des configurations par défaut peu sécurisées.

**Systèmes spécialisés** :
- **Medical systems** : Des systèmes utilisés dans le domaine médical.
- **Vehicles** : Des systèmes embarqués dans des véhicules.
- **Aircraft** : Des systèmes spécifiques pour les avions.
- **Smart meters** : Des compteurs intelligents pour mesurer la consommation d'énergie. (eau, gaz, électricité)

**Voice over IP (VoIP) (Voix sur IP)**: (**Whatsapp, skype...**)Technologie permettant de transmettre des appels vocaux via des réseaux IP (Internet Protocol). **VoIP convertit la voix en paquets de données numériques qui sont transmis sur le réseau IP**. Cela permet de combiner la voix et les données sur le même réseau, offrant ainsi une communication plus efficace.

**HVAC**:  (Heating, ventilation, air conditioning) Systèmes de contrôle utilisés pour réguler la température, l'humidité et la qualité de l'air dans les bâtiments.

**Drones**: Véhicules aériens sans pilote contrôlés à distance ou autonomes pour diverses applications.

**Multifunction printer (MFP) (Imprimante multifonction)**: Une imprimante capable d'effectuer des tâches d'impression, de numérisation, de copie et parfois de télécopie.

**RTOS**: (Real-time operating system) (OS Réactif, 0ms, ABS véhicules) Contrairement aux systèmes d'exploitation classiques tels que Windows ou Linux, les RTOS sont optimisés pour répondre à des contraintes de temps strictes et garantir une exécution prédictible des tâches en temps réel. (Ex: Utilisé pour gérer l'ABS véhicules)

**Surveillance systems (Systèmes de surveillance)**: Systèmes utilisés pour surveiller et enregistrer des activités ou des événements spécifiques.

**System on chip (SoC) (Système sur puce)**: Un circuit intégré qui intègre tous les composants nécessaires pour un système informatique complet sur une seule puce.

**Communication considerations (Considérations de communication)**:

- **5G**: Cinquième génération de technologies de communication mobile, offrant des vitesses plus rapides et une connectivité améliorée.
    
- **Narrow-band (Bande étroite)**: Une gamme étroite de fréquences utilisée pour la communication sans fil.
    
- **Baseband radio (Radio à bande de base)**: Transmission de signaux sur une seule fréquence sans modulation.
    
- **Subscriber identity module (SIM) cards (Cartes SIM d'abonné)**: Cartes utilisées dans les téléphones mobiles pour identifier et authentifier les abonnés du réseau.
    
- **Zigbee**: Protocole de communication sans fil à faible consommation d'énergie pour les appareils IoT.
    

**Constraints (Contraintes)**: Limitations ou conditions spécifiques qui doivent être prises en compte lors de la conception ou de l'utilisation de systèmes ou de technologies.

- **Power (Alimentation)**: Contraintes liées à la disponibilité ou à la consommation d'énergie.
    
- **Compute (Calcul)**: Limitations de puissance de calcul ou de traitement.
    
- **Network (Réseau)**: Contraintes liées aux capacités ou à la disponibilité du réseau.
    
- **Crypto (Cryptographie)**: Contraintes de sécurité liées à la cryptographie.
    
- **Inability to patch (Incapacité de mise à jour)**: Incapacité de mettre à jour ou de corriger les vulnérabilités de sécurité.
    
- **Authentication (Authentification)**: Processus de vérification de l'identité des utilisateurs ou des systèmes.
    
- **Range (Portée)**: Portée maximale de communication sans fil.
    
- **Cost (Coût)**: Contraintes budgétaires ou financières.
    
- **Implied trust (Confiance implicite)**: Niveau de confiance implicite accordé à certains systèmes ou acteurs sans vérification explicite.


## 2.7 - Explain the importance of physical security controls. 
- **Bollards/barricades (Bollards/barrières)**: Obstacles physiques pour contrôler l'accès ou empêcher l'accès non autorisé.
    
- **Access control vestibules**: (SAS d'entrée, anti tailgating) Espaces d'entrée sécurisés qui permettent de vérifier l'identité des personnes avant de leur accorder l'accès.
    
- **Badges**: Cartes d'identification utilisées pour vérifier l'accès autorisé aux installations.
    
- **Alarms (Alarmes)**: Systèmes de sécurité qui détectent les intrusions ou les incidents non autorisés.
    
- **Signage**: (Signalisation) Panneaux ou indications pour guider et informer les personnes des règles de sécurité et des zones restreintes.
    
- **Cameras (Caméras)**: Dispositifs de surveillance vidéo pour surveiller les activités.
    - **Motion recognition (Reconnaissance de mouvement)**: Capacité des caméras à détecter les mouvements et à réagir en conséquence.
        
    - **Object detection (Détection d'objets)**: Capacité des caméras à détecter des objets spécifiques dans leur champ de vision.

- **Closed-circuit television (CCTV)**: Système de caméras de surveillance connectées à des écrans de contrôle privés (surveillance en temps reelle).
    
- **Industrial camouflage (Camouflage industriel)**: Technique utilisée pour masquer les infrastructures critiques des regards non autorisés.
    
- **Personnel (Personnel)**: Personnel chargé de la sécurité et du contrôle d'accès.
    
    - **Guards (Gardiens)**: Personnel humain chargé de la sécurité.
        
    - **Robot sentries (Sentinelles robotisées)**: Robots utilisés pour surveiller et patrouiller les zones.
        
    - **Reception (Réception)**: Personnel d'accueil qui peut également jouer un rôle de contrôle d'accès.
        
    - **Two-person integrity/control (Contrôle/Intégrité à deux personnes)**: Pratique où **deux personnes doivent travailler ensemble pour effectuer des tâches sensibles**. Réduisant les risques liés à la fraude, aux erreurs humaines et aux actes malveillants.
        
- **Locks (Serrures)**: Dispositifs de verrouillage pour sécuriser les portes, les armoires, etc.
    
    - **Biometrics (Biométrie)**: Utilisation de caractéristiques physiologiques uniques pour l'authentification, telles que les empreintes digitales ou la reconnaissance faciale.
        
    - **Electronic (Électronique)**: Serrures contrôlées par des systèmes électroniques.
        
    - **Physical (Physique)**: Serrures traditionnelles utilisant des clés physiques.
        
    - **Cable locks (Serrures pour câbles)**: (empeche le vol de laptopet pc) cable avec cadena integré permettant d'attacher un appareil
        
- **USB data blocker**: (Bouclier de données USB) Le fonctionnement d'un USB data blocker est simple. Il s'insère entre le câble USB d'un périphérique et le port USB de la source d'alimentation (comme un ordinateur portable, un chargeur mural public ou un port USB de voiture). Le bloqueur de données USB bloque les connexions de données tout en autorisant seulement l'alimentation électrique à passer à travers, permettant ainsi de charger le périphérique sans risque de transfert de données non autorisé.
    
- **Lighting**: (Éclairage) Éclairage de sécurité pour illuminer les zones sensibles.
    
- **Fencing**: (Clôture) Clôture physique pour délimiter les zones et restreindre l'accès.
    
- **Fire suppression**: (Extinction d'incendie) Systèmes utilisés pour éteindre les incendies et limiter les dégâts.
    
- **Sensors (Capteurs)**: Dispositifs pour détecter les événements ou changements spécifiques dans l'environnement.
    
    - **Motion detection (Détection de mouvement)**: Capteurs pour détecter les mouvements dans une zone.
        
    - **Noise detection (Détection de bruit)**: Capteurs pour détecter les sons inhabituels ou alarmants.
        
    - **Proximity reader (Lecteur de proximité)**: Capteurs pour vérifier la proximité d'une carte ou d'un badge.
        
    - **Moisture detection (Détection d'humidité)**: Capteurs pour détecter les fuites d'eau ou l'humidité excessive.
        
    - **Cards (Cartes)**: Cartes d'accès utilisées pour l'identification.
        
    - **Temperature (Température)**: Capteurs pour surveiller les changements de température dans des environnements sensibles.
        
- **Drones**: Véhicules aériens sans pilote utilisés pour la surveillance et l'inspection.
    
- **Visitor logs (Journaux des visiteurs)**: Registres pour enregistrer les informations des visiteurs entrant dans les installations.
    
- **Faraday cages**: (**Bloque les onde radio WIFI & Cellular, Imaginer une cage de perroquet géante qui bloque l'électricité**) Structures métalliques qui bloquent les signaux électroniques pour protéger les dispositifs sensibles.
    
- **Air gap (Coupure d'air)**: mesure de sécurité physique utilisée pour isoler complètement un système informatique ou un réseau sensible du reste du monde, en le déconnectant physiquement de tout autre réseau ou appareil, y compris l'internet. (**Evite les attaques transversales**)
    
- **Screened subnet (previously known as demilitarized zone, DMZ)**: (SAS de sécurité, isolation réseaux) Zone de sécurité neutre, isolée des réseaux internes et externes, où sont placés les services exposés au public pour réduire le risque d'attaques sur le réseau interne.
  Exemple : Si un pirate informatique parvient à compromettre le serveur web, il se retrouvera dans la DMZ et non sur le réseau interne de l'entreprise.
  **Deux pare-feu**: L'un entre Internet et la DMZ, l'autre entre la DMZ et le réseau interne.
  **Services dans la DMZ**: Seuls les services nécessaires à l'interaction publique (serveurs web, serveurs de courrier, serveurs DNS, etc.) sont placés dans la DMZ.
    ![[F19-02.jpg|400]]
- **Protected cable distribution (Distribution de câbles protégée)**: Méthode pour sécuriser les câbles de communication contre les manipulations non autorisées.
    
- **Secure areas (Zones sécurisées)**:
    - **Air gap (Coupure d'air)**: Désigne un système informatique ou réseau qui est isolé physiquement de tout autre réseau ou système, en particulier d'Internet. (**Evite les attaques transversales**)
        
    - **Vault (Coffre-fort)**: Espace sécurisé pour protéger les objets de valeur.
        
    - **Safe (Coffre-fort)**: Un coffre-fort utilisé pour stocker des objets de valeur.
        
    - **Hot aisle (Allée chaude)**: Espace dans un centre de données où l'air chaud des serveurs est évacué.
        
    - **Cold aisle (Allée froide)**: Espace dans un centre de données où l'air frais est aspiré pour refroidir les serveurs.
        
- **Secure data destruction (Destruction sécurisée des données)**:

    - **Burning**: Incinérer en poudre    
    - **Shredding**: Déchiqueter un support en morceaux
    - **Pulping (Broyage)**: Méthode de destruction physique des supports de stockage.
    - **Pulverizing (Pulvérisation)**: Méthode de destruction physique des supports de stockage.


    - **Degaussing (Démagnétisation)**: (purge, ne détruit pas le support) Méthode pour effacer les données des supports magnétiques.
        
    - **Third-party solutions (Solutions tierces)**: Services spécialisés de destruction sécurisée des données


Bien sûr. Prenons un exemple simple pour illustrer comment fonctionne le salting.


Lorsque l'utilisateur tente de se connecter, le système récupère le sel associé à cet utilisateur, combine le sel avec le mot de passe fourni, hache le résultat et vérifie si le hachage correspond à celui stocké dans la base de données.

**Note**: Les valeurs ci-dessus sont purement illustratives et ne représentent pas de véritables hachages ou sels. Dans la réalité, les hachages et les sels seraient beaucoup plus complexes et utiliseraient des fonctions de hachage robustes et sécurisées.

## 2.8 - Basics of cryptographic concepts

• **Digital signatures (Signatures numériques)**: (Authentification, Intégrité, Non-répudiation) Technique cryptographique qui permet de prouver l'authenticité, l'intégrité et la non-répudiation d'un message ou d'un document numérique.
exemple : 
Pour vérifier une signature, le récepteur du message calcule une nouvelle valeur mathématique à partir du message reçu et de la clé publique correspondante. Si cette nouvelle valeur mathématique correspond à la signature, le message est valide. Cela garantit que le message est authentique (il provient bien de l'expéditeur prévu), qu'il est intègre (il n'a pas été modifié en transit) et qu'il ne peut pas être répudié (l'expéditeur ne peut pas nier l'avoir envoyé).

• **Key length (Longueur de clé)**: Taille de la clé utilisée dans un algorithme de chiffrement, généralement plus la clé est longue, plus la sécurité est renforcée.

• **Key stretching**: (Renforcer une clé ou un mdp en le faisant passer dans un algo qui itère des millers de fois, souvent avec un salt) Rend les attaques par brut-force et dictionnaire beaucoups plus longue !

• **Salting**: Ajout d'une valeur aléatoire unique (sel) à des données avant de les hacher pour rendre les attaques par dictionnaire plus difficiles.
Exemple de Salt :

| UserID | Username | PasswordHash                        | Salt     |Salt+pwd|
|--------|----------|-------------------------------------|----------|---|
| 1      | Alice   | 9a8b7c6d5e4f3g210j9i8h7g6f5d4s3a | aBcD1234 |pass123aBcD1234|


• **Hashing**: Transformation d'une donnée en une valeur de hachage, généralement utilisée pour vérifier l'intégrité des données. (**SHA256, MD5**)

• **Key exchange (Échange de clé)**: Processus permettant à deux parties de s'échanger des clés secrètes pour sécuriser leur communication. (**PGP** par exemple)

• **Perfect forward secrecy (PFS)**: Clé de chiffrement éphémère. assurant qu'une clé compromise ne compromettra pas les clés précédemment utilisées

**Quantum**: Branche de la cryptographie qui exploite les propriétés de la mécanique quantique pour sécuriser les communications et protéger les informations sensibles
- **Communications**: Domaine de la cryptographie concernant la sécurité des communications dans un contexte quantique.
- **Computing**: Domaine de la cryptographie concernant les algorithmes résistants aux attaques quantiques.

**Post-quantum**: Cryptographie résistante aux attaques quantiques.

**Ephemeral (Éphémère)**: Clés générées temporairement pour une session spécifique et qui ne sont pas réutilisées.

**Modes of operation (Modes de fonctionnement)**:
- **Authenticated (Authentifié)**: Modes de chiffrement qui fournissent également une vérification d'authenticité des données.
- **Unauthenticated (Non authentifié)**: Modes de chiffrement sans vérification d'authenticité des données.
- **Counter (Compteur)**: Mode de chiffrement où un compteur est utilisé pour générer une séquence de chiffres uniques.

**Blockchain (Chaîne de blocs)**: La cryptographie joue un rôle essentiel dans la technologie de la blockchain. La blockchain est une technologie de registre distribué qui permet de stocker des données de manière sécurisée, transparente et décentralisée.

- **Public ledgers (Registres publics)**: Registres de transactions accessibles publiquement et sécurisés par cryptographie. C'est le type de blockchain le plus décentralisé et transparent.

**Cipher suites (Suites de chiffrement)**: Suite d'algorithmes de chiffrement, de méthodes d'échange de clés et de fonctions de hachage utilisés dans les protocoles de communication sécurisés tels que **SSL/TLS**. Une **"cipher suite" spécifie la manière dont les données seront chiffrées et sécurisées lorsqu'elles sont transférées entre un client et un serveur.**

- **Stream (Flux)**: Chiffrement par **flux**, où les données sont traitées **bit par bit**.
- **Block (Bloc)**: Chiffrement par **bloc**, où les données sont traitées en **blocs de taille fixe**.


<mark class="hltr-blue">**Cryptographic algorithms**</mark> 

Encryption Comparison Chart (this chart is not all inclusive - it is a place to get started as you research and add your own entries) - Note all of the symmetric algorithms end in a number, an "s" or "sh"

Algorithm Type (Sym/Asym) Method (block/stream) Key Size

AES Symmetric 128-bit Block cipher 128, 192, or 256

DES Symmetric 64-bit Block cipher 56

3DES Symmetric 64-bit Block cipher 56, 112, or 168

Blowfish Symmetric 64-bit Block cipher 32 to 448

Twofish Symmetric 128-bit Block cipher 128, 192, or 256

RC4 Symmetric Stream cipher 40 to 2048

Add your own additional Stream, Block, Symmetric and Asymmetric ciphers

ECC Asymmetric

RSA Asymmetric

DSA Asymmetric 1024 (larger keys are now supported)

El Gamal Asymmetric (DSA is based on El Gamal aka Elgamal)

Public/Private Keys Asymmetric

Diffie-Hellman key Asymmetric


**Symmetric vs. asymmetric (Symétrique vs asymétrique)**:
1. **Noms des Algorithmes** :
    - **Symétrique** :  end in a number, an "s" or "sh"
    - **Asymétrique** : Souvent plus longs ou plus complexes (Diffie-Hellman, RSA, Elliptic Curve).
2. **Nombre de Clés** :
    - Symétrique : Une seule clé pour chiffrement et déchiffrement.
    - Asymétrique : Deux clés (publique (chiffrement) et privée (déchiffrement)).
3. **Utilisation** :
    - Symétrique : Chiffrement de données en masse (bulk) (**messages et appels**).
    - Asymétrique : Echange de clés, signatures numériques (**MAJ & signatures logiciels, services en ligne**).
#### Algorithmes Symétriques:
- **AES (Advanced Encryption Standard)** : (128, 192 ou 256 bits) Un chiffrement par blocs largement utilisé qui prend en charge des tailles de clés de 128, 192 ou 256 bits. Il est considéré comme très sécurisé et est le successeur de DES.
    
- **DES (Data Encryption Standard)** : (56 bits, considéré comme non sécurisé aujourd'hui) Un ancien chiffrement par blocs qui utilise une clé de 56 bits. En raison de sa clé plus courte et de ses vulnérabilités, il est largement considéré comme obsolète.
    
- **3DES (Triple DES)** : (112 bits) Une amélioration du DES qui applique l'algorithme DES trois fois à chaque bloc de données. Il est plus sécurisé que DES, mais moins efficace que AES.
    
- **RC4 (Rivest Cipher 4)** : Un chiffrement de flux autrefois largement utilisé dans des protocoles tels que SSL et WEP. Il est maintenant considéré comme non sécurisé en raison de vulnérabilités connues.
    
- **Blowfish & Twofish** : (256bits) Ce sont tous deux des chiffrements par blocs. Blowfish a une taille de bloc de 64 bits et des longueurs de clé allant de 32 à 448 bits. Twofish est son successeur, avec une taille de bloc de 128 bits et des tailles de clé allant jusqu'à 256 bits. 
#### Algorithmes Asymétriques:
- **RSA (Rivest–Shamir–Adleman)** : (2048 bits) L'un des premiers cryptosystèmes à clé publique pratiques et largement utilisé pour la transmission sécurisée des données.
    
- **DSA (Digital Signature Algorithm)** : (2048 bits) Utilisé principalement pour les signatures numériques plutôt que pour le chiffrement. Il fait partie de la norme de signature numérique (DSS) approuvée par le gouvernement américain.
    
- **Diffie-Hellman** : Bien que ce ne soit pas un algorithme de chiffrement à proprement parler, c'est une méthode d'échange de clés cryptographiques sur un canal public.
    
- **ECC** : Cryptographie à courbes elliptiques (224 à 521 bits)  Une approche de la cryptographie à clé publique basée sur les courbes elliptiques sur les champs finis. Elle est plus efficace grâce à ses clés plus courtes pour le même niveau de sécurité que les méthodes traditionnelles.
- Elliptical Curve Cryptography (ECC) is used on **mobile devices**. 

**Lightweight cryptography (Cryptographie légère)**: Cryptographie optimisée pour être efficace sur des systèmes avec des ressources limitées.

**Steganography (Stéganographie)**: L'art de cacher des informations dans des supports numériques notamment grace au **LSB ( least significant bit, bit le plus à droite d'un nombre binaire)** est souvent utilisé pour cacher des informations à l'intérieur d'un fichier multimédia
- **Audio**: Cacher des informations dans des fichiers audio.
- **Video**: Cacher des informations dans des fichiers vidéo.
- **Image**: Cacher des informations dans des images.

**Homomorphic encryption**: (Opérations sur données ciffrée/hashées) Branche de la cryptographie qui permet de réaliser des opérations mathématiques sur des données chiffrées sans avoir besoin de les déchiffrer au préalable

**Common use cases (Cas d'utilisation courants)**:
- **Low power devices (Appareils à faible consommation d'énergie)**: Cryptographie adaptée aux appareils ayant des limitations d'énergie.
- **Low latency (Faible latence)**: Cryptographie permettant des opérations rapides sans délai excessif.
- **High resiliency (Haute résilience)**: Cryptographie offrant une protection robuste contre les attaques.
- **Supporting confidentiality (Confidentialité)**: Cryptographie assurant la protection des données contre les accès non autorisés.
- **Supporting integrity (Intégrité)**: Cryptographie garantissant l'intégrité et l'authenticité des données.
- **Supporting obfuscation (Obfuscation)**: Cryptographie utilisée pour rendre les données illisibles ou difficiles à comprendre.
- **Supporting authentication (Authentification)**: Cryptographie utilisée pour vérifier l'identité des parties impliquées dans une communication.
- **Supporting non-repudiation (Non-répudiation)**: Cryptographie permettant de prouver qu'un utilisateur a effectué une action et ne peut pas le nier.

**Limitations (Limitations)**:
- **Speed (Vitesse)**: L'efficacité du chiffrement peut affecter les performances globales du système.
- **Size (Taille)**: La taille des clés et des données chiffrées peut avoir un impact sur la mémoire et le stockage.
- **Weak keys (Clés faibles)**: Certaines clés peuvent être vulnérables à des attaques cryptographiques.
- **Time (Temps)**: Le temps nécessaire pour effectuer les opérations de cryptographie peut être critique dans certains cas.
- **Longevity (Longévité)**: La durée pendant laquelle une clé est considérée comme sécurisée.
- **Predictability (Prévisibilité)**: La cryptographie prévisible peut être vulnérable aux attaques.
- **Reuse (Réutilisation)**: Réutiliser des clés pour différentes opérations peut compromettre la sécurité.
- **<mark class="hltr-blue">Entropy</mark> (Entropie)**: (**add randomness**)Le niveau d'**aléatoire** utilisé dans la génération de clés.
- **Computational overheads**: La charge supplémentaire imposée par les opérations cryptographiques.
- **Resource vs. security constraints**: Les ressources limitées peuvent limiter le choix et l'efficacité des algorithmes de cryptographie.