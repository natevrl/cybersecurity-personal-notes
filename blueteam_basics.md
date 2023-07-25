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

