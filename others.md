# <mark class="hltr-green">Hors-catégorie</mark> :

**resilience** : Capacité d'un système informatique, d'un réseau ou d'une organisation à résister et à se rétablir rapidement après avoir subi une cyberattaque (ou autre type catastrophe naturelle)

**Ports**
- **21** = FTP (File Transfer Protocol)
- 22 = SSH
- 23 = Telnet (**not secure, sending cleartext**)
- 25 = SMTP (Simple Email Transfer Protocol)
- 53 = DNS
- 80, 443 = HTTP/HTTPS
- 389 = LDAP (Active Directory)
- 3389 = RDP (Remote Desktop Protocol)
- 3306 : MySQL
- **Private IP** :  **192.168**.x.x, **172.16**-**31**.x.x, **10**.x.x.x
	- if **192.186** == NOT PRIVATE !! (example)

**Phases in the Incident Response Plan** 
1. Preparation: The organization plans out how they will respond to attack, this can involve: 
2. Identification: Detecting and determining whether an incident has occurred. 
3. Containment: Once a threat has been identified, the organization must limit or prevent any further damage. 
4. Eradication: The removal of the threat 
5. Recovery: Restoring systems affected by the incident 
6. Lessons Learned: Where the organization reviews their incident response and prepare for a future attack

### DISK RAID :

**Striping** : (performance, pas de redondance (backup)) les données sont divisées en blocs, et chaque bloc est écrit sur un disque dur séparé. Augmente les performances car plusieurs disques peuvent être lus ou écrits simultanément.

**Mirroring** : (redondance) Les données sont clonées sur deux disques ou plus. Offre une redondance complète des données. Si un disque échoue, aucune donnée n'est perdue car une copie existe sur un autre disque.

**Parité** : (redondance) Reconstruire les données d'un disque qui aurait échoué. Les données de parité sont calculées et stockées sur un ou plusieurs disques.

- **DISK 0 (Striping)** :
	- **Objectif**: Augmentation des performances
	- **Minimum de disques**: 2
	- **Striping**: Oui
	- **Mirroring**: Non
	- **Parité**: Non
	- **Informations importantes**: Aucune redondance; si un disque échoue, toutes les données sont perdues.
- **DISK 1 (Mirroring)** : le seul avec mirroring, si non c'est parité pour la redondance
	- **Objectif**: Redondance
	- **Minimum de disques**: 2
	- **Striping**: Non
	- **Mirroring**: Oui
	- **Parité**: Non
	- **Informations importantes**: Duplique les données sur chaque disque pour la redondance.
- **DISK 5 (Striping avec parité)**:
	- **Objectif**: Performance et redondance
	- **Minimum de disques**: 3
	- **Striping**: Oui
	- **Mirroring**: Non
	- **Parité**: Oui (sur un seul disque)
	- **Informations importantes**: Vous pouvez vous permettre de perdre un disque et toujours récupérer les données.
- **DISK 6 : (pareil que 5 mais avec 1 disque en plus)** : 4 disques
- **DISK 10 (1+0, Mirroring et Striping)** :
	- **Objectif**: Performance et redondance
	- **Minimum de disques**: 4
	- **Striping**: Oui
	- **Mirroring**: Oui
	- **Parité**: Non
	- **Informations importantes**: Combinaison de RAID 1 et RAID 0.



**GPO** : (Windows System, Credentials) Group Policy Object (GPO) can include many settings related to credentials, such as password complexity requirements, password history, password length, and account lockout settings.


**Product Development Phases**: Dont Throw Sausage Pizza 
- **Development >> Testing >> Staging >> Production**