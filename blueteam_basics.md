# Le triptyque CIA 
`représente les trois principes fondamentaux de la sécurité de l'information (Confidentialité, Intégrité, Disponibilité)`

### Confidentialité (Triptyque CIA)
Protection des informations sensibles contre un accès ou une divulgation non autorisés.
Garantit que seules les personnes autorisées ont accès à des données spécifiques.

**Méthodes** : chiffrement, les contrôles d'accès, l'authentification des utilisateurs et la classification des données

### Intégrité (Triptyque CIA)
L'intégrité vise à maintenir l'exactitude et la cohérence des données tout au long de leur cycle de vie. Elle garantit que les données restent inchangées et conservent leur état d'origine depuis leur création jusqu'au traitement et au stockage.

**Méthodes** : hashing, digital signatures, and access controls to prevent unauthorized alterations.

### Disponibilité (Triptyque CIA)
Elle garantit que les systèmes, les données et les services sont disponibles et fonctionnent correctement lorsque cela est requis.

**Méthodes** : redundancy, failover mechanisms, load balancing, and disaster recovery plans

# Risk & Risk management

## Threat, Vulnerability, and Risk

**Vulnerability** : faiblesse dans le système, lacune dans la sécurité de l'entreprise (unpatched system, employees without Security Awareness training, bad firewall config...)
**Threat** : Cyber menace/indicent plausible due à une vulnerabilité (cyber criminals, threat actors...)
**Risk** : vulnerability + threat = risk. Le risque est à la jonction entre les potentiels vulnérabilité et les menaces

## Managing Risk

**Risk appetite** : what level of risk is "acceptable", les actions mises en place pour  contrer le risque ne devraient pas coûer plus cher à la companie que faire directement face à ce risque

 1. Avoid : stop the activity that is generating risk
 2. Mitigate : Implement control to reduce risk to an "acceptable" level
 3. Transfer : Move the risk to a different asset or share the risk with a 3rd party
 4. Accept : Risk is within "acceptable" agreed levels and will be acknowledged

## Measuring Risk


Mesurer le risque **selon la probabilité à faire des degats et la valeur de ce qui contient le risque** (database with financial info > serveur not connected to the intern network / sysadmin with high access > restricted employee)

>!Le risk measuring peut énormement varier selon les priorités et la situation actuelle de l'entreprise.
>
> Remember that part of your growth as an Analyst will be to learn to identify what is important for your company and how to respond accordingly.
> 
>> **Se rappeller qu'un bon cyber Analyst sait identifier ce qui est important pour l'entreprise et comment y répondre en concéquence.**

# Frameworks and controls

> Les frameworks (ou cadres de travail) sont des ensembles de lignes directrices (guidelines) et de normes établies pour aider à mettre en œuvre des stratégies de sécurité efficaces. (Define, Control, & Mitigate Risks)

## Les types de frameworks

### NIST Framework
Développé par le National Institute of Standards and Technology (NIST) des États-Unis, ce cadre fournit une approche globale de la gestion des risques en cybersécurité. Il se compose de cinq fonctions principales : Identifier, Protéger, Détecter, Répondre et Récupérer.

### ISO 27001
Il s'agit d'une norme internationale pour la gestion de la sécurité de l'information. Elle fournit des directives pour établir, mettre en œuvre, maintenir et améliorer un système de gestion de la sécurité de l'information (SMSI) au sein d'une organisation.

### CIS Controls
Les CIS (Center for Internet Security) Controls sont un ensemble de meilleures pratiques de sécurité informatique qui aident les organisations à protéger leurs systèmes et leurs données contre les cybermenaces courantes.

### MITRE ATT&CK
Ce cadre, développé par MITRE Corporation, fournit une base de connaissances des tactiques, techniques et procédures (TTP) utilisées par les cyberattaquants. Il aide les organisations à mieux comprendre et à se défendre contre les menaces avancées.

### OWASP Top 10
Le Top 10 des vulnérabilités de l'OWASP (Open Web Application Security Project) est une liste des dix principales vulnérabilités de sécurité affectant les applications web, donnant aux développeurs un guide pour les éviter.

# ## Security Operations and the Defense Analyst

> Un **SOC** (Security Operations Center) est un centre  de sécurité qui assure une surveillance continue et proactive des systèmes informatiques et des réseaux d'une organisation pour détecter et répondre rapidement aux menaces  grâce à un processus de "continuous monitoring cycle" (souvent 24/7).

**Security Posture** : The Security Posture of an organization represents how well an organization can  **predict, prevent  and respond to** ever-changing cyber threats.


## Common Protection Technologies

**Firewall** : contrôle et filtre le trafic réseau pour protéger les systèmes et les données contre les menaces potentielles.

**IDS (Intrusion Detection System)** : système de détection d'intrusion qui surveille le trafic réseau ou les activités système pour identifier les comportements suspects ou les attaques potentielles.
 Envoie des alerts et logs lorsque qu'il detecte des anomalies
App : Snort, Suricata

**IPS (Intrusion Prevention System)** : comme IDS + prend des mesures pour bloquer ou prévenir les attaques en temps réel (real-time)

**FIREWALL vs IDS vs IPS** : En résumé, le pare-feu agit comme une barrière de filtrage entre les réseaux, l'IDS surveille le trafic pour détecter les anomalies, tandis que l'IPS détecte et prend des mesures actives pour bloquer ou prévenir les attaques en temps réel.

**Email gathering** : scrapping d'adresse email, souvent utilisé a des fins marketing

**web proxies / web gateways** : serveur intermediaire entre client et serveur (utilise sa propre IP pour demander au serveur)

**Email gateways** : passerelle e-mail, serveur-logiciel qui agit en tant qu'intermédiaire entre différents ssystèmes de messagerie électronique (filtrage & sécurité, auth. archivage et stockage...)

**DLP (Data Loss Prevention)** : Approche de sécurité informatique visant à protéger les données sensibles et confidentielles d'une organisation en empêchant leur divulgation, leur fuite ou leur accès non autorisé.
Exemples de mesures : (Surveillance et blocage des e-mails, Contrôle des périphériques de stockage. Chiffrement des données, Surveillance des accès aux bases de données...)
Logiciels : McAfee Data Loss Prevention (DLP), Symantec Data Loss Prevention (DLP)

**Nessus** : vulnerability scanner
**Wireshak, TCPdump** : analyse de paquets réseau
**honeypot (appat, piège)** : dispositif de sécurité informatique mis en place dans le réseau d'une organisation pour attirer et piéger les attaquants potentiels.

**SIEM (Security Information and Event Management)** : Plateforme de sécurité informatique qui collecte, corrèle (normalize), centralise et  analyse les données de sécurité pour détecter et répondre aux menaces potentielles.

**SOAR (Security Orchestration, Automation, and Response)** : **Le SOAR complète le SIEM en automatisant et en orchestrant les actions de réponse aux incidents de sécurité**. Il peut exécuter des tâches telles que la quarantaine d'un appareil compromis, le blocage d'une adresse IP malveillante ou l'envoi de notifications d'alerte aux équipes de sécurité.
sandboxes

## SOC : Roles and Responsibilities

### **SOC Team** : 

**Tier l (Junior)**
-  surveille let network traffic, logs et events
- Gère les tickets, close les alerts
- réalise des investigations basiques
**Tier ll (Senior)**
- Execute des investigations plus poussées
- Chasse les adversaires proactivement
- Surveille et résout les alertes plus complexes
**Tier lll (Principale)**
- Malware reversing
- Threat hunting & adversary research
- investigation avancée
**SOC MANAGER** 
- Supervise la SOC
- plafinie des opérations, coordonne les activié
- Gère les incidents
- Analyse et rapport
**CISO (Chief Information Security Officer)**
- responsable de la stratégie globale
- supervise et représente la SOC face aux autres secteurs
- Planification et budgétisation (approves budget)
- Gestion des partenariats externes

### SOC Roles

- Defense Analyst : Investigates Notable Events
- Engineer : Creates and tests detections
- Architect : Chooses and implements tools

### Analyst SOC Tasks

1. Goal ultime d'un SOC Analyst : identifier les security incidents le plus tot possible
	1. **security Incident** : the CIA triad  of an asset (network, ststem...) has been broken
	2. **Security/data breach** : confirmation of data disclosure to unauthorized parties.
2. **Alert Triage :** Catégoriser et gérer les events/alert pour identifier les menaces potentielles
	1. Reconnaitre les **True Positive** and **False Positive** events
	2. **Incident Analysis** : Methode organisé pour **detecter** les incidents, **minimiser** les pertes, atténuer (**mitigating**) les faiblesses et maintenance la disponiblité des services liés
	3. **Incident Response** : Plan claire etablie par les entreprise indiquant les demarches a suivre lorsque qu'un incident se produit. 
3. **Threat Hunting** : Chercher/trouver de nouvelles menaces/attaques en utilisant des techniques d'investigation avancées

Autres taches d'un SOC Analyst :
1. **Reports or notes** : detailler les incidents trouvés lors de Threat Hungting ou Incident Analysis
2. **Suggestions** : aider a améliorer des outils, automatiser. améliorer des settings...

separer les fichiers selon les categories de la security+


