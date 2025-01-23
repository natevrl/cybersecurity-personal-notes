# <mark class="hltr-blue">5.0 Governance, Risk, and Compliance 14%</mark> 

## 5.1 Compare and contrast various types of controls.

**security control (contrôle de sécurité)** : mesure technique ou organisationnelle mise en place pour réduire les risques de sécurité et assurer la CIA (confidentialité, intégrité et la disponibilité des ressources)

- **Control Managerial** : Contrôles liés à la **gouvernance et à la gestion de la sécurité**.  _Technique_ : Exemples : politiques de sécurité, formation et sensibilisation, évaluations des risques.

- **Control Operational** : (**human element**) Contrôles liés aux opérations quotidiennes. 
  _Technique_ : Exemples : audits de sécurité, procédures de réponse aux incidents, sauvegardes régulières.

- **Control Technical** : (**hardware & software**) Contrôles mis en œuvre à l'aide de la technologie. 
  _Technique_ : Exemples : pare-feu, chiffrement, authentification multi-facteurs.

**Control type**
- **Preventive (Préventif)** : (Barrage) limite physiquement (fencing/lock) ou techmologique (pare-feu, IDS) les accès a une zone ou un appareil. 

- **Detective (Détectif)** : Contrôles conçus pour détecter les incidents.
  Exemples : systèmes de détection d'intrusion, surveillance de la sécurité, audits.

- **Corrective (Correctif)** : (Réparation, Post-incident) Contrôles conçus pour corriger les incidents.
  Exemples : patchs de sécurité, plans de restauration après sinistre.

- **Deterrent (Dissuasif)** : Contrôles conçus pour décourager les incidents.
   Exemples : affichages de notifications de surveillance, politiques disciplinaires.

- **Compensating (Compensatoire)** : (Alternatif, rechange) Mesures de rechange qui compensent les lacunes des autres contrôles.
 Exemples : UPS (Uninterruptible power supply)
- 
- **Physical (Physique)** : Contrôles liés à la sécurité physique. 
  Exemples : serrures, cartes d'accès, caméras de surveillance.



## 5.2 Regulations, standards, or frameworks


**Regulations, standards, and legislation (Régulations, normes et législation)** : Règles ou directives établies par des entités gouvernementales ou des organismes de normalisation. Le non-respect peut entraîner des sanctions, des amendes ou des poursuites judiciaires.

- **General Data Protection Regulation (GDPR)** : **Règlement européen** sur la protection des données. 
 Impose des règles strictes aux entreprises comme : le droit d'accéder à leurs données, le droit de les rectifier, le droit de les supprimer (demande COOKIES, suppression données sous 72h...)
    
- **National, territory, or state laws (Lois nationales, territoriales ou d'État)** : Lois spécifiques à un pays ou à un territoire.

- **PCI-DSS (Payment Card Industry Data Security Standard)** : Norme pour la protection des données de carte de paiement. 
  Technique_ : Inclut des exigences telles que le cryptage, l'accès réglementé aux données de carte et des évaluations de sécurité régulières.

- **HIPAA (Health Insurance Portability and Accountability Act)** :HIPAA est la loi régissant la manière dont la **PHI (Protected Health Information)** doit être protégée.
	- **PHI (Protected Health Information)**: Toute information médicale qui peut être utilisée pour identifier un individu et qui a été créée, utilisée, ou partagée lors de la prestation de soins de santé.

- ****PII (Personally Identifiable Information)**** : (noms/email/adresse...) Informations qui peuvent être utilisées pour identifier, contacter, ou localiser une personne.

- **FERPA** : (Étudiant) Protection des données des **Etudiant**

---

**Key frameworks (Cadres clés)** : Modèles utilisés pour guider la mise en place et l'évaluation des programmes de sécurité. _Informations_ : Ces cadres fournissent une base pour développer, maintenir et améliorer continuellement les pratiques et politiques de sécurité. 

- **Center for Internet Security (CIS)**: (Framework, non lucrative, bonnes pratiques) Organisation a but non-lucrative qui fournit des directives pour sécuriser les systèmes et les réseaux. 
  _Informations_ : Fournit les "CIS Critical Security Controls", une série de meilleures pratiques pour améliorer la posture de sécurité. 
    
- **National Institute of Standards and Technology (NIST)** : (Normes, USA, framework) Une agence du gouvernement américain qui développe et promeut des normes et des mesures  pour améliorer la sécurité. 
  Il se compose de cinq fonctions principales : Identifier, Protéger, Détecter, Répondre et Récupérer.
	- **RMF (Risk Management Framework)** : (NIST, Risk Management, framework) Processus structuré pour gérer les risques, crée par le NIST
	- **CSF (Cybersecurity Framework)** : (NIST, framework) Ensemble de meilleures pratiques et de directives pour améliorer la cybersécurité, crée par le NIST.
    
- **ISO 27k** : Security framework qui doit etre acheter. Séries de normes pour les systèmes de gestion de la sécurité de l'information (ISMS)
	- 27002 classifies security controls 
	- 27701 focuses on personal data and privacy.
	- 27017 and 27018 : cloud security
	- <mark class="hltr-blue">ISO 31k </mark> : spécialisé risk management
    
- **SSAE SOC 2 Type I/II** : System and Organization Controls, des rapports d'audit qui évaluent les contrôles internes d'une entreprise. 
  _Informations_ : Les rapports SOC 2 évaluent la manière dont une entreprise gère et protège les données des clients. 
  _Technique_ : Type I évalue les contrôles à un moment précis dans le temps, tandis que Type II évalue leur efficacité sur une période de temps.
    
- **Cloud security alliance (CSA)** : Organisation qui promeut les meilleures pratiques pour assurer la sécurité dans le cloud.
	- **CMM (Cloud Control Matrix)** : Un ensemble de critères de sécurité spécifiques créés par la **CSA** pour aider les entreprises à évaluer et établir un niveau de sécurité de leurs fournisseurs de services cloud.
	- **Reference Architecture** : garantir que les produits et solutions sont construits de manière cohérente et supportable

---

**Benchmarks/secure configuration guides** : (**mode d'emplois**) pour sécuriser spécifiquement des logiciels ou du matériel.
- **Web server (Serveur web)** : Guide pour sécuriser un serveur web. 
- **OS (Système d'exploitation)** : Guide pour sécuriser un système d'exploitation. 
- **Application server (Serveur d'application)** : Guide pour sécuriser un serveur d'application.
- **Network infrastructure devices** : Guide pour sécuriser les dispositifs qui composent l'infrastructure réseau.




---

## 5.3 policies to organizational security.

**Personnel (Personnel)**

- **Acceptable use policy (Politique d'utilisation acceptable)** : Définit ce que les employés peuvent et ne peuvent pas faire avec les ressources informatiques de l'entreprise.
    
- **Job rotation (Rotation des postes)** : Pratique qui consiste à faire tourner les employés entre différents postes pour éviter la fraude ou la collusion. 
    
- **Mandatory vacation (Congé obligatoire)** : Politique qui oblige les employés à prendre des congés pour permettre la détection d'activités frauduleuses.
  _Technique_ : Si un employé manipulateur est en vacances, et qu'une irrégularité est remarquée en son absence, cela pourrait indiquer une fraude.
    
- **Separation of duties** :  (Séparation des tâches) Nécessite plusieurs personnes pour accomplir une tâche (Mesure pour prévenir la fraude interne) 
  _Technique_ : Dans un processus de paiement, une personne pourrait être responsable de la création d'un bon de commande, une autre de l'approbation, et une troisième de la réalisation du paiement.
    
- **Least privilege (Principe du moindre privilège)** : Assure que les utilisateurs ont uniquement les droits nécessaires pour effectuer leurs tâches.
    
- **Clean desk space (Espace de bureau propre)** : Les documents contenant des informations financières ou personnelles ne doivent pas être laissés à la vue de tous sur un bureau.
    
- **Background checks (Vérifications des antécédents)** : Processus par lequel l'entreprise vérifie les antécédents d'un employé potentiel.
    
- **Non-disclosure agreement (NDA) (Accord de non-divulgation)** : Contrat légal qui oblige une partie à ne pas divulguer des informations confidentielles. 
  _Informations_ : Les NDA sont couramment utilisés pour protéger les secrets commerciaux.
    
- **Social media analysis (Analyse des médias sociaux)** : Examen des profils de médias sociaux d'un individu pour obtenir des informations. 
  _Technique_ : Une entreprise pourrait examiner le profil LinkedIn d'un candidat pour vérifier la véracité de son CV, ou son profil Twitter pour évaluer son professionnalisme.
    
- **Onboarding (Intégration)** : Processus par lequel de nouveaux employés sont intégrés dans l'entreprise. 
  _Informations_ : Cela comprend la formation, la familiarisation avec les politiques et procédures de l'entreprise, et d'autres étapes clés pour s'assurer que l'employé est prêt à travailler efficacement. 
    
- **Offboarding (Départ)** : Processus par lequel un employé quitte l'entreprise, volontairement ou non. 
  _Informations_ : Cela inclut généralement la restitution de tout équipement, la suppression des droits d'accès, et d'autres mesures pour sécuriser les actifs de l'entreprise après le départ de l'employé.
    
- **User training (Formation des utilisateurs)**
    
    - **Gamification (Ludification)** : Utilisation d'éléments de jeu dans la formation pour augmenter l'engagement.
        
    - **Capture the flag (Capture du drapeau)** : Compétition où les participants doivent trouver et exploiter des vulnérabilités pour "capturer" des drapeaux (informations).
        
    - **Phishing campaigns (Campagnes de phishing)** : Une entreprise pourrait envoyer un faux e-mail de phishing à ses employés pour voir combien d'entre eux cliquent sur le lien.
        
    - **Phishing simulations (Simulations de phishing)** : Simulations d'attaques de phishing utilisées pour former les employés à reconnaître et éviter les tentatives réelles. 
      _Technique_ : Après avoir cliqué sur un lien dans un e-mail de phishing simulé, un employé pourrait être dirigé vers une page de formation expliquant les signes d'une tentative de phishing.
        
    - **Computer-based training (CBT) (Formation basée sur ordinateur)** : Formation délivrée via ordinateur, généralement à travers des modules en ligne. 
        
    - **Role-based training (Formation basée sur le rôle)** : Formation adaptée au rôle spécifique d'un employé au sein de l'entreprise.
        
- **Diversity of training techniques (Diversité des techniques de formation)** : L'utilisation de différentes méthodes et approches pour former les employés. 
    

---

**Third-party risk management (Gestion des risques des tiers)** : Processus d'identification, d'évaluation, et de gestion des risques associés aux partenaires, fournisseurs, et autres tiers. 
  
- **Vendors (Fournisseurs)** : Entreprises ou individus qui fournissent des produits ou services à une organisation.

- **Supply chain (Chaîne d'approvisionnement)** : Ensemble des étapes nécessaires pour produire et livrer un produit ou un service à un client.
  _Technique_ : Assurer la traçabilité des composants utilisés dans un produit pour détecter et prévenir les altérations malveillantes.

- **Business partners (Partenaires commerciaux)** : Autres entreprises ou entités avec lesquelles une organisation a une relation commerciale.

- **<mark class="hltr-blue">Service level agreement (SLA) </mark>** : (Accord de niveau de service) Contrat entre un fournisseur de services et un client qui spécifie le niveau de service attendu.
  _Technique_ : Un fournisseur d'hébergement web promet une disponibilité de 99,9% du temps - si le service est en panne plus souvent, des pénalités peuvent être appliquées.

- **Memorandum of understanding (MOU) (Protocole d'accord)** : (Accord préliminaire et exploratoire (preliminary or exploratory), Non-contraignant) Accord préliminaire ou exploratoire pour exprimer les intentions entre deux ou plusieurs parties. 
  N'échangent pas de biens ou de services de valeur).
  _Technique_ : Deux entreprises pourraient signer un MOU définissant comment elles collaboreront sur un projet de recherche conjoint.

- **Measurement systems analysis (MSA)** :(Analyse des systèmes de mesure)
  _Technique_ : Une entreprise pourrait utiliser le MSA pour évaluer la précision de ses capteurs dans une chaîne de production.

- **Business partnership agreement (BPA) (Accord de partenariat commercial)** : 
  (Accord de partenariat commercial)
  Accord contractuel entre des entreprises partenaires définissant les termes de leur relation.
  _Technique_ : Deux entreprises collaborant sur un produit pourraient avoir un BPA définissant la répartition des revenus.

- **End of life (EOL) (Fin de vie)** : Point où un produit ne sera plus fabriqué, vendu ou officiellement pris en charge.

- **End of service life (EOSL) (Fin de vie du service)** : Point où un service ou un produit ne recevra plus de mises à jour ou de support officiel, bien qu'il puisse encore être utilisé.

---

**Data :**
- **Data Classification (Classification des données)** : (**"Public", "Interne", "Confidentiel" et "Secret"**) Processus de catégorisation des données en fonction de leur niveau de sensibilité.

- **Data Governance (Gouvernance des données)** : (Gestion, Qualité, Intégrité des donnés) Ensemble des processus qui garantissent la bonne gestion des données.
  Elle s'assure que les données sont stockées, archivées, sauvegardées et protégées de manière efficace et conforme.

- **Data Retention (Conservation des données)** : Politiques définissant combien de temps les données doivent être conservées.
  _Technique_ : Une entreprise peut avoir une politique stipulant que les données des clients sont supprimées après cinq ans d'inactivité.

---

**Credential Policies (Politiques de d'auth)** :
  - **Personnel** : Politiques concernant les informations d'identification du personnel.
    _Technique_ : Une politique pourrait exiger des mots de passe d'au moins 12 caractères avec une combinaison de lettres, chiffres et symboles.

  - **Third-party** : Politiques concernant les informations d'identification des tiers.
    _Technique_ : Les fournisseurs peuvent être tenus d'utiliser l'authentification à deux facteurs pour accéder aux systèmes de l'entreprise.

  - **Devices** : Politiques de référencement spécifiques aux appareils.
    _Technique_ : Les serveurs peuvent avoir des exigences de mot de passe plus strictes que les ordinateurs de bureau.

  - **Service accounts** : Comptes utilisés par les applications ou les services plutôt que par les individus.
    _Technique_ : Les comptes de service peuvent avoir des mots de passe plus longs et plus complexes qui sont rarement, voire jamais, changés manuellement.

  - **Administrator/root accounts** : Comptes avec des privilèges élevés utilisés pour gérer les systèmes.

---

**Organizational Policies (Politiques organisationnelles)** :
  - **Change management (Gestion des changements)** : Processus pour gérer les modifications apportées aux systèmes ou aux applications.
    _Technique_ : Les changements peuvent nécessiter l'approbation d'un comité et être testés dans un environnement séparé avant d'être déployés.
  - **Change control (Contrôle des changements)** : Supervision et approbation des modifications apportées.
    _Technique_ : Chaque changement peut nécessiter une documentation détaillée et une justification.
  - **Asset management (Gestion des actifs)** : Processus de suivi et de gestion des actifs physiques et logiciels d'une organisation.
    _Informations_ : Aide à garantir que tous les actifs sont connus, sécurisés et à jour.

  
## 5.4 Risk management processes and concepts.


**Risk types :**

- **External Risk (Risque externe)** : Risques provenant de sources extérieures à l'organisation.
- **Internal Risk (Risque interne)** : Risques provenant de sources à l'intérieur de l'organisation. (employé, système défaillant...)

- **Legacy Systems (Systèmes hérités)** : Anciens systèmes ou applications plus mises à jour

- **Multiparty Risk (Risque multipartite)** : Risques associés à plusieurs parties prenantes, telles que les fournisseurs ou les partenaires. _Informations_ : Si l'une des parties est compromise, cela peut affecter l'ensemble de la chaîne.

- **IP Theft (Vol de propriété intellectuelle)** : Vol d'informations ou de créations protégées, telles que des brevets, des marques déposées ou des droits d'auteur. .

- **Software Compliance/Licensing (Conformité/licence logicielle)** : Veiller à ce que tous les logiciels utilisés dans l'organisation soient correctement licenciés et conformes. 

**Risk Management Strategies (Stratégies de gestion des risques)** :

- **Acceptance (Acceptation)** : Accepter le risk sans prendre de mesures pour le réduire.
- **Avoidance (Évitement)** : (ff) Eviter le risque, arreter de jouer avec.
- **Transference (Transfert)** : (**assurance**) Transférer le risque à une autre partie, souvent en achetant une **assurance**
- **Mitigation (Atténuation)** : Prendre des mesures pour réduire la probabilité ou l'impact d'un risque.


**Risk Analysis (Analyse des risques)** : Évaluation des risques potentiels auxquels une organisation peut être confrontée.

- **Risk Register (Registre des risques)** : Document ou base de données où les risques identifiés sont enregistrés, y compris leur nature, leur impact, leur probabilité d'occurrence et les mesures prises pour les atténuer.

- **Risk Matrix/Heat Map** : Outil graphique utilisé pour représenter la probabilité et l'impact des risques.
  _Technique_ : Les risques dans la zone rouge (haut impact, haute probabilité) sont généralement traités en priorité.

- **Risk Control Assessment** : Évaluation sur l'efficacité des mesures de contrôle pour atténuer les risques.

- **Inherent Risk (Risque inhérent)** : Le niveau de risque présent dans une activité ou un processus sans tenir compte des mesures de contrôle en place. 
  _Informations_ : Une base pour comprendre le risque avant que toute mesure d'atténuation ne soit appliquée. 

- **Residual Risk (Risque résiduel)** : Le niveau de risque restant après que toutes les mesures de contrôle ont été appliquées. 
  _Technique_ : Si le risque résiduel est toujours trop élevé, des mesures de contrôle supplémentaires peuvent être nécessaires.

- **Risk Appetite** : Le niveau de risque qu'une organisation est prête à accepter pour atteindre ses objectifs.

- **risk awareness** : Éduquer et faire prendre conscience des risks potentiels

- **<mark class="hltr-blue">Risk Assessment Types</mark> (Types d'évaluation des risques)** :

	- **Qualitative** : (likelihood (probabilité), sans nombre, high/medium/low..) Évaluation basée sur des descriptions non numériques, telles que "faible", "moyen" ou "élevé".
	- **Quantitative** : (Chiffre, nombre précis...) Évaluation basée sur des chiffres, comme le coût potentiel d'une perte.

- **Likelihood of Occurrence (Probabilité d'occurrence)** : La chance qu'un risque se réalise. 
  _Informations_ : Habituellement exprimé en pourcentage.

- **Impact (Impact)** : Le dommage potentiel qui pourrait résulter de la réalisation d'un risque. 
  _Informations_ : Peut-être quantifié en termes financiers, de réputation, ou d'autres mesures pertinentes.

- **Asset Value (Valeur de l'actif)** : La valeur d'une ressource pour une organisation. 
  _Technique_ : Peut être basée sur le coût de remplacement, la valeur stratégique, ou d'autres facteurs.

- **Single-Loss Expectancy (SLE) (Espérance de perte unique)** : Le coût estimé d'une occurrence unique d'un risque. 
  _Informations_ : Utilisé dans l'analyse de risque quantitative pour évaluer l'impact financier d'un risque particulier. 
  _Technique_ : SLE = Valeur de l'actif × Exposition de l'actif (en pourcentage).

- **Annualized Loss Expectancy (ALE) (Espérance de perte annualisée)** : Le coût potentiel annuel d'un risque compte tenu de sa probabilité d'occurrence. _Informations_ : Aide à prioriser les risques en termes de coûts annuels potentiels pour l'organisation. 
  _Technique_ : ALE = SLE × Taux d'occurrence annualisé (ARO).

- **Annualized Rate of Occurrence (ARO)** : ("Combien de fois par An?") Représente le nombre de fois qu'un risque va se produire sur 12 mois

**Disasters (Catastrophes)** : Événements majeurs qui peuvent causer des perturbations significatives à une organisation.

- **Environmental (Environnementales)** : Catastrophes causées par des phénomènes naturels
    
- **Person-made (Causées par l'homme)** : Catastrophes qui sont le résultat direct ou indirect d'actions humaines. 
  _Technique_ : Exemples : attaques terroristes, incendies industriels, déversements de produits chimiques.
    
- **Internal vs. external (Interne vs externe)** : Distinction entre les catastrophes qui se produisent à l'intérieur d'une organisation et celles qui proviennent de sources externes. 
  _Technique_ : Exemple interne : une surtension électrique causant un incendie dans un centre de données. Exemple externe : une inondation causée par de fortes pluies affectant l'infrastructure de l'entreprise.


**Business Impact Analysis (Analyse d'impact sur l'activité)** : Processus qui détermine l'importance des ressources pour l'organisation et évalue l'impact d'une interruption. 

- **Recovery Time Objective (RTO) (Business Impact Analysis)** : (Délai, Restauration, Objectif) Durée maximale pendant laquelle un service peut être indisponible avant que cela n'ait un impact inacceptable.
  _Technique_ : L'objectif est de restaurer le service ou l'application avant d'atteindre le RTO.

- **Recovery Point Objective (RPO) (Business Impact Analysis)** : (Données, Perte, Objectif.)Quantité maximale de données pouvant être perdue sans conséquence grave pour l'entreprise.
  Si une entreprise a un RPO de 30 minutes, elle doit effectuer des sauvegardes toutes les 30 minutes.

- **Mean Time to Repair (MTTR) (Temps moyen de réparation) (Business Impact Analysis)** : Temps moyen nécessaire pour réparer un composant ou un système après une défaillance. 
  Si une entreprise a un MTTR de 2 heures pour un serveur, cela signifie que, en moyenne, il faut 2 heures pour le remettre en service après une panne.

- **Mean Time Between Failures (MTBF) (Temps moyen entre défaillances) (Business Impact Analysis)** : (Taux de pannes) Temps moyen qui s'écoule entre deux défaillances consécutives d'un système.
  Si un disque dur a un MTBF de 100 000 heures, cela signifie qu'en moyenne, il devrait fonctionner pendant 100 000 heures avant de tomber en panne.

- **Functional Recovery Plans (Plans de reprise fonctionnelle)** : Plans détaillant les étapes spécifiques à suivre pour restaurer des fonctions ou des services spécifiques après une interruption.
  _Technique_ : Par exemple, un plan de reprise pour le département des ressources humaines détaillerait comment reprendre les processus de paie et de recrutement.

- **Single Point of Failure (Point unique de défaillance)** : if Défaillance == arrêt complet d'un système.
  _Technique_ : Par exemple, un routeur qui est le seul moyen d'accéder à Internet pour une entreprise est un point unique de défaillance.

- **<mark class="hltr-blue">Disaster Recovery Plan (DRP)</mark> (Plan de reprise après sinistre)** : Un document détaillé qui décrit comment répondre et récupérer d'une catastrophe qui affecte les systèmes informatiques. _Informations_ : Le DRP se concentre sur la technologie et les systèmes, et non sur les processus métier (contrairement au FRP). 
  _Technique_ : Il comprend généralement des détails sur la sauvegarde des données, la restauration des systèmes et le basculement vers des sites de reprise après sinistre.

- **Mission Essential Functions (Fonctions essentielles de la mission)** : Les fonctions les plus critiques qui doivent être rétablies en priorité après une interruption. 

- **Identification of Critical Systems (Identification des systèmes critiques)** : Processus pour déterminer quels systèmes sont vitaux pour les opérations et la mission de l'organisation._Technique_ : Dans un hôpital, le système de dossiers médicaux électroniques serait considéré comme critique.

- **Site Risk Assessment (Évaluation des risques du site)** : Évaluation des risques associés à un emplacement physique spécifique, tels que les risques naturels, les menaces de sécurité ou les vulnérabilités structurelles.
  _Technique_ : Par exemple, un site situé dans une zone inondable aurait un risque plus élevé d'inondation.

## 5.5 - Explain privacy and sensitive data concepts in relation to security.

**Organizational consequences of privacy and data breaches** : Les effets négatifs qui peuvent découler d'une violation de la confidentialité ou de la sécurité des données.

- **Reputation damage (Dommage à la réputation)** : Confiance perdue à la suite d'une data breache.

- **Identity theft (Vol d'identité)** : Utilisation frauduleuse des informations personnelles d'une personne pour commettre une fraude.
    
- **Fines (Amendes)** : Sanctions pécuniaires imposées par les autorités réglementaires en cas de non-conformité aux lois sur la protection des données.
    
- **IP theft** : (Vol de propriété intellectuelle) Cela peut inclure des secrets commerciaux, des brevets, des droits d'auteur ou des marques déposées. 
    
**Notifications of breaches (Notifications de violations)** : Informer les parties concernées lorsqu'une data breache se produit.

- **Escalation (Escalade)** : Processus de communication d'un incident à des niveaux hiérarchiques supérieurs pour une action ou une prise de décision appropriée. 
    
- **Public notifications and disclosures (Notifications et divulgations publiques)** : Informer le grand public d'une data breache.
    

**Data types (Types de données)** : Catégories d'informations stockées, traitées ou transmises par une organisation.

- **Classifications (Classifications)** : Systèmes utilisés pour catégoriser les données en fonction de leur niveau de sensibilité. 
  _Technique_ : Exemples courants incluent Public, Privé, Sensible, Confidentiel, Critique et Propriétaire.
    
- **PII** : (Personally identifiable information ) Informations qui peuvent être utilisées pour identifier une personne. 
  _Informations_ : Cela peut inclure des éléments tels que le nom, l'adresse, le numéro de sécurité sociale, etc
    
- **PHI** : Health information **(PHI avec HIPAA)** Données relatives à la santé physique ou mentale d'une personne.
    
- **Financial information (Informations financières)** : Données relatives aux finances d'une personne ou d'une organisation.

- **Government data (Données gouvernementales)** : Informations détenues ou utilisées par les agences gouvernementales.
    
- **Customer data (Données client)** : Informations sur les clients d'une organisation. _Informations_ : Cela peut inclure des noms, des adresses, des préférences d'achat, etc.
    
**Privacy enhancing technologies (Technologies d'amélioration de la vie privée)** : Outils et méthodes utilisés pour protéger la confidentialité des données.

- **Data minimization (Minimisation des données)** : Réduire la quantité de données personnelles collectées à ce qui est strictement nécessaire (just email, nom et credit card pour un achat par exemple). 
    
- **Data masking (Masquage des données)** : (`123-45-6789` -> `XXX-XX-6789`) Technique qui remplace les données sensibles par des versions modifiées ou fictives.
    
- **Tokenization (Tokenisation)** : (CC : `1234-5678-9101-1121` -> `abcd-efgh-ijkl-mnop`) Remplacer les données sensibles par des identifiants uniques, appelés tokens, qui n'ont aucune valeur significative en dehors du système de tokenisation.
    
- **Anonymization (Anonymisation)** : Processus de suppression ou de modification des données personnelles d'une manière telle qu'il est impossible d'identifier une personne spécifique.
  _Technique_ : Les enregistrements médicaux peuvent être anonymisés pour la recherche en supprimant les noms, adresses, dates de naissance, etc.
    
- **Pseudo-anonymization (Pseudo-anonymisation)** : Processus de remplacement des données personnelles par des identifiants fictifs. 
  _Informations_ : Contrairement à l'anonymisation, la pseudo-anonymisation peut être inversée si l'identifiant original est disponible. 
  _Technique_ : Utilisé dans la recherche médicale où les données doivent être protégées, mais il peut être nécessaire de retrouver l'individu original.
    

**Roles and responsibilities (Rôles et responsabilités)** : Chaque rôle a des responsabilités spécifiques pour assurer la confidentialité, l'intégrité et la disponibilité des données.

- **Data owners (Propriétaires des données)** : (responsable, business decisions) Reponsable CIA des datas et prend des business decisions a propos des datas.
    
- **Data controller (Contrôleur de données)** : Entité qui détermine les finalités et les moyens du traitement des données personnelles.
  _Technique_ : Une entreprise qui collecte les informations des clients pour ses propres besoins est considérée comme un contrôleur de données.
    
- **Data processor (Processeur de données)** : Entité qui traite les données personnelles pour le compte du contrôleur. 
  _Technique_ : Une entreprise d'hébergement cloud qui stocke des données pour une autre entreprise est un processeur de données.
    
- **Data custodian/steward (Gestionnaire/tuteur de données)** : (access right & security) Manage les accès (access right) et protège les données.
    
- **Data protection officer (DPO)** : (privacy) Expert de la protection des données qui conseille l'entreprise sur la conformité avec les réglementations sur la protection des données. 
  _Informations_ : Obligatoire pour certaines organisations sous le RGPD. 
  _Technique_ : Le DPO évalue les risques, conseille sur les mesures de protection des données et est le point de contact pour les autorités de régulation.
  
    

**Information life cycle (Cycle de vie de l'information)** : Phases par lesquelles passent les données, de la création à la destruction.

**Impact assessment (Évaluation de l'impact)** : Évaluation des risques et des conséquences d'une violation potentielle de la protection des données. 

**Terms of agreement (Termes d'accord)** : Conditions auxquelles les deux parties conviennent, souvent en ce qui concerne l'accès ou l'utilisation des données. 

**Privacy notice** : (Avis de confidentialité) Document informant les individus sur la manière dont leurs données seront utilisées et protégées.
_Technique_ : Les avis de confidentialité sont souvent publiés sur les sites web et doivent être clairs et faciles à comprendre.

