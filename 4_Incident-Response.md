# <mark class="hltr-purple">4.0 Operations and Incident Response 16%</mark>

## 4.1 - Use the appropriate tool to assess organizational security.


**Network reconnaissance and discovery**

**tracert/traceroute** : Outil pour tracer la route que les paquets prennent pour atteindre une destination.
_Technique_ : Utilise des paquets ICMP* pour découvrir les routeurs entre la source et la destination.
```bash
user1$ traceroute openai.com
traceroute to openai.com (13.107.213.42), 30 hops max, 60 byte packets
1  192.168.0.1 (192.168.0.1)  2.327 ms  2.288 ms  2.259 ms
... (truncated for brevity)
13  13.107.213.42 (13.107.213.42)  32.768 ms  32.738 ms  32.709 ms
```

**nslookup/dig** : Interrogent les serveurs DNS pour obtenir des informations sur les domaines.
_Informations_ : Essentiel pour résoudre ou diagnostiquer les problèmes DNS.
_Technique_ : Peut interroger n'importe quel type d'enregistrement (par exemple, A, MX, NS).
```bash
user1$ dig openai.com

; <<>> DiG 9.10.3-P4-Ubuntu <<>> openai.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 53535
... (truncated for brevity)
```

**ipconfig/ifconfig** : Affiche les configurations réseau d'une machine.
_Informations_ : Aide à identifier les détails IP, les masques de sous-réseau, les passerelles, etc.
_Technique_ : `ipconfig` est spécifique à Windows, tandis que `ifconfig` est utilisé sur UNIX/Linux.
```bash
user1$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.1.2  netmask 255.255.255.0  broadcast 192.168.1.255
... (truncated for brevity)
```

**nmap** : Identifie les ports ouverts et les services en cours d'exécution sur une machine.
_Technique_ : Possède des capacités de scan avancées, y compris la détection d'OS et la détection de version.
```bash
user1$ nmap -p 80,443 openai.com
Starting Nmap ... 
Nmap scan report for openai.com (13.107.213.42)
Host is up (0.0040s latency).
PORT    STATE  SERVICE
80/tcp  open  http
443/tcp open  https
```

**ping/pathping** : Outil pour vérifier la connectivité réseau.
_Informations_ : `ping` vérifie la connectivité, tandis que `pathping` fournit également des statistiques sur la route.
_Technique_ : Utilise des paquets ICMP*.
```bash
user1$ ping -c 3 openai.com
PING openai.com (13.107.213.42) 56(84) bytes of data.
64 bytes from 13.107.213.42 (13.107.213.42): icmp_seq=1 ttl=56 time=5.00 ms
... (truncated for brevity)
```

**hping** : Outil de test réseau avancé.
_Informations_ : Peut être utilisé pour tester des pare-feux, des IDS*, et d'autres équipements de réseau.
_Technique_ : Permet de créer des paquets personnalisés avec n'importe quel ensemble de flags TCP/UDP/ICMP.
```bash
user1$ hping3 -c 3 -S openai.com
HPING openai.com (eth0 13.107.213.42): S set, 40 headers + 0 data bytes
len=46 ip=13.107.213.42 ttl=56 DF id=0 sport=80 flags=SA seq=0 win=8192 rtt=5.0 ms
... (truncated for brevity)
```

**netstat** : Affiche les connexions réseau, les tables de routage, les statistiques d'interface, etc.
_Informations_ :  Permet d'observer en temps réel les connexions entrantes et sortantes.
```bash
user1$ netstat -tan
Active Internet connections (servers and established)
Proto Recv-Q Send-Q Local Address           Foreign Address         State
tcp        0      0 127.0.0.50:53           0.0.0.0:*               LISTEN
```

**netcat** : Outil de lecture et d'écriture de données à travers des connexions réseau.
_Informations_ : Parfois surnommé le "couteau suisse" pour le réseau.
_Technique_ : Peut être utilisé pour créer des connexions TCP/UDP, écouter sur des ports arbitraires, transférer des fichiers, etc.
```bash
user1$ echo "Hello OpenAI" | netcat openai.com 80
```


**IP scanners** : Outils pour scanner et identifier les appareils actifs dans un réseau.
_Informations_ : Ils permettent d'identifier rapidement les hôtes actifs, leurs adresses IP, et parfois les services en cours d'exécution.
_Technique_ : Les scanners IP peuvent utiliser des paquets ICMP, ARP ou TCP pour détecter les hôtes.
```bash
user1$ nmap -sn 192.168.1.0/24
Nmap scan report for 192.168.1.1
Host is up (0.0040s latency).
... (truncated for brevity)
```

**arp** : Affiche et modifie les entrées dans la table ARP*.
_Informations_ : La table ARP lie les adresses IP aux adresses MAC sur un réseau local.
_Technique_ : C'est un composant essentiel pour le fonctionnement des réseaux IP.
```bash
user1$ arp -a
? (192.168.1.1) at aa:bb:cc:dd:ee:ff [ether] on eth0
... (truncated for brevity)
```

**route** : Affiche ou modifie la table de routage IP.
_Informations_ : Essentiel pour déterminer comment les paquets sont acheminés à travers un réseau.
_Technique_ : La table de routage contient des informations sur les réseaux accessibles et les routes pour y parvenir.
```bash
user1$ route -n
Kernel IP routing table
Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
0.0.0.0         42.17.16.1     0.0.0.0         UG    0      0        0 eth0
42.17.16.0     0.0.0.0         255.255.240.0   U     0      0        0 eth0
```

**curl** : Outil en ligne de commande pour transférer des données avec des URL.
_Informations_ : Utilisé pour faire des requêtes HTTP, HTTPS, FTP et autres. Peut être utilisé pour tester des sites web, des API, etc.
_Technique_ : Supporte une multitude de protocoles et de méthodes.
Requete **GET** par defaut
```bash
user1$ curl http://example.com

<!doctype html>
<html>
<head>
    <title>Example Domain</title>
</head>
<body>
    <h1>Example Domain</h1>
    <p>This domain is for use in illustrative examples in documents. You may use this domain in literature without prior coordination or asking for permission.</p>
</body>
</html>

```

**theHarvester** : Outil pour collecter des informations sur un domaine.
_Informations_ : Utilisé pour la reconnaissance lors des tests d'intrusion.
_Technique_ : Il recherche des e-mails, des noms, des sous-domaines associés à un domaine.
```bash
user1$ theHarvester -d example.com -b google

=====================================
Emails found:
-------------------------------------
admin@example.com
contact@example.com
support@example.com

=====================================
Hosts found:
-------------------------------------
www.example.com 93.184.216.34
ftp.example.com 93.184.216.35

```

**sn1per** : Outil d'automatisation des tests de pénétration.
_Informations_ : Effectue la reconnaissance, le scan, l'exploitation et plus encore.
_Technique_ : Il s'appuie sur plusieurs autres outils pour effectuer des scans complets.
_Commande_ :
(Note: Sn1per est un outil interactif et complexe, donc une commande simple pourrait ne pas refléter toutes ses capacités.)
```bash
user1$ sniper -t openai.com -m recon
```

**scanless** : Outil pour effectuer des scans de ports en ligne.
_Informations_ : Utilise des services publics de scan en ligne pour vérifier les ports ouverts, sans déclencher d'alarmes.
_Technique_ : S'appuie sur des services comme HackerTarget, Spyse, etc.
```bash
user1$ scanless -t hackertarget example.com

Starting scanless scan on example.com...

PORT      STATE   SERVICE
21/tcp    closed  ftp
22/tcp    open    ssh
23/tcp    closed  telnet
25/tcp    closed  smtp
80/tcp    open    http
443/tcp   open    https

Scan complete for example.com
```

**dnsenum** : Outil Perl pour énumérer les informations DNS d'un domaine.
_Informations_ : Aide à obtenir des informations sur les sous-domaines, les adresses IP, les serveurs de noms, etc.
_Technique_ : Peut également rechercher des informations WHOIS.
```bash
user1$ dnsenum example.com

example.com has NS record ns1.example.com.
example.com has MX record mail.example.com.
example.com has A record 93.184.216.34
```

**Nessus** : Outil de scan de vulnérabilités.
_Informations_ : L'un des scanners de vulnérabilités les plus populaires. Il identifie les vulnérabilités, les erreurs de configuration, etc.
(Note : Nessus est principalement une interface graphique, donc la commande peut ne pas refléter toutes ses capacités.)
```bash
user1$ nessus
... (GUI-based tool)
```

**Cuckoo** :
- Plateforme d'analyse de malwares.
_Informations_ : Analyse les fichiers suspects dans un environnement isolé pour observer leur comportement.
_Technique_ : Génère des rapports détaillés sur le comportement du malware.
_Commande_ :
```bash
user1$ cuckoo submit sample_malware.exe

Task #1 has been submitted with file "sample_malware.exe"
```

**File manipulation**

**head** :
- Affiche le début d'un fichier.
_Informations_ : Utile pour obtenir un aperçu rapide d'un fichier sans l'ouvrir entièrement.
_Technique_ : Par défaut, montre les 10 premières lignes d'un fichier.
_Commande_ :
```bash
user1$ head -n 5 sample.txt

Line 1: This is the first line.
Line 2: This is the second line.
Line 3: Another line here.
Line 4: And yet another line.
Line 5: This is the fifth line.
```

**tail** : Affiche la fin d'un fichier.
_Technique_ : Avec l'option `-f`, il peut afficher les nouvelles lignes ajoutées à un fichier en temps réel.
```bash
user1$ tail sample.txt

Line 96: Almost there.
Line 97: This is the ninety-seventh line.
Line 98: Penultimate line.
Line 99: One before the last.
Line 100: This is the last line.
```

**cat** :
- Affiche le contenu d'un ou plusieurs fichiers.
_Technique_ : Peut être utilisé avec des redirections pour créer ou ajouter à des fichiers.
```bash
user1$ cat file1.txt file2.txt
... (contents of both files)
```

**grep** :
- Recherche de motifs dans les fichiers.
_Informations_ : Puissant outil de recherche de texte utilisé pour trouver des correspondances spécifiques dans des fichiers ou des flux.
_Technique_ : Supporte des expressions régulières pour des recherches complexes.
_Commande_ :
```bash
user1$ grep "search_term" file.txt
... (lines containing the search term)
```

**chmod** :
- Modifie les permissions d'un fichier ou d'un répertoire.
_Informations_ : Essentiel pour la gestion des droits d'accès aux fichiers et dossiers.
_Technique_ : Utilise des valeurs numériques pour définir les permissions (ex : 755 pour rwxr-xr-x).
_Commande_ :
```bash
user1$ chmod 755 file.txt
```

**logger** :
- Ajoute des messages au journal du système.
_Informations_ : Utilisé pour la journalisation manuelle ou pour ajouter des messages personnalisés aux journaux du système.
_Technique_ : Les messages peuvent être dirigés vers différents journaux selon leur importance.
_Commande_ :
```bash
user1$ logger "Custom log message"
```


---

**Shell and script environments**

**SSH** :
- Protocole pour se connecter de manière sécurisée à des machines distantes.
_Informations_ : Permet d'exécuter des commandes à distance et de transférer des fichiers tout en garantissant la confidentialité et l'intégrité des données.
_Technique_ : Utilise la cryptographie à clés publiques pour l'authentification.
_Commande_ :
```bash
user1$ ssh user@remote-host
... (establishes a secure connection to the remote host)
```

**PowerShell** :
- Environnement de script et de gestion des tâches automatisées pour Windows.
_Informations_ : Plus puissant que l'invite de commandes traditionnelle, avec des capacités avancées de gestion des systèmes.
```bash
PS C:\> Get-Process
... (lists all running processes on the system)
```

**Python** :
- Langage de programmation de haut niveau, utilisé pour l'automatisation, le développement web, l'analyse de données, etc.
```bash
user1$ python -c "print('Hello, OpenAI!')"
Hello, OpenAI!
```

**OpenSSL** :
- Boîte à outils pour travailler avec le protocole SSL/TLS* et les certificats.
_Informations_ : Utilisé pour générer des certificats, établir des connexions sécurisées, tester la sécurité SSL/TLS, etc.
_Technique_ : Est à la base de nombreux serveurs web et clients pour fournir une communication sécurisée.
_Commande_ :
```bash
user1$ openssl s_client -connect openai.com:443
... (establishes a SSL connection and displays the certificate information)
```

---

**Packet capture and replay**

**Tcpreplay** :
- Outil pour rejouer des captures de trafic réseau.
_Informations_ : Utilisé pour reproduire des scénarios réseau spécifiques ou tester des dispositifs de sécurité.
_Technique_ : Peut modifier les paquets à la volée pendant la relecture.
_Commande_ :
```bash
user1$ tcpreplay -i eth0 capture.pcap
... (replays the captured packets on eth0 interface)
```

**Tcpdump** :
- Captureur de paquets en ligne de commande.
_Informations_ : Permet d'intercepter et d'afficher les paquets réseau. Très utile pour le dépannage réseau.
_Technique_ : Peut filtrer les paquets selon des critères spécifiques pour isoler le trafic d'intérêt.
_Commande_ :
```bash
user1$ tcpdump -i eth0 port 80
... (captures packets on eth0 interface for port 80)
```

**Wireshark** :
- Analyseur de paquets avec interface graphique.
_Informations_ : Il permet d'inspecter le trafic réseau en détail, avec des capacités de filtrage et d'analyse.
```bash
user1$ wireshark
... (GUI opens showing real-time packet capture)
```


---

**Forensics**

**dd** :
- Outil de copie et de conversion de fichiers.
_Commande_ : Pour créer une image disque de `/dev/sda1` vers un fichier appelé `backup.img`
```bash
user1$ dd if=/dev/sda1 of=backup.img bs=4M status=progress
100+0 records in
100+0 records out
419430400 bytes (419 MB, 400 MiB) copied, 10.1234 s, 41.4 MB/s
```

**Memdump** :
- Outil pour extraire le contenu de la mémoire.  **Peut être utilisé pendant une réponse à incident pour capturer des preuves**.
_Informations_ : Aide à analyser le contenu de la mémoire d'un système pour la recherche de malwares ou d'autres artefacts.
Supposons que vous souhaitiez dumper la mémoire d'un processus avec l'ID 1234 vers un fichier `process_dump.bin` :
```bash
user1$ memdump 1234 > process_dump.bin
Memory dump completed for process 1234.
```

**WinHex** :
- Éditeur hexadécimal pour Windows.
_Informations_ : Permet d'inspecter et de modifier des fichiers ou des disques au niveau des bytes.
```bash
user1$ winhex
... (GUI-based tool)
```

**FTK imager** :
- Outil d'imagerie et d'analyse forensique.
_Informations_ : Capture des images de disques, de mémoire et réalise des analyses forensiques.
```bash
user1$ ftkimager
... (GUI-based tool)
```

**Autopsy** :
- Plateforme d'analyse forensique numérique.
_Informations_ : Utilisé pour effectuer des investigations approfondies sur des images disque, des fichiers, etc.
_Technique_ : Fournit des modules pour l'analyse de registres, de journaux, d'artefacts de fichiers, et plus encore.
```bash
user1$ autopsy
... (GUI-based tool)
```

**Exploitation frameworks** :
- Outils pour tester la pénétration et exploiter les vulnérabilités.
_Informations_ : Ces cadres fournissent des modules pour diverses attaques, évasions, post-exploitations, etc.
_Technique_ : **Metasploit** est un exemple populaire d'un tel cadre.
```bash
user1$ msfconsole
msf5 > 
... (Metasploit framework command line interface)
```

**Password crackers** :
- Outils pour tenter de deviner ou de casser des mots de passe.
_Technique_ : **John the Ripper et Hashcat** sont des exemples populaires.
```bash
user1$ john --wordlist=dict.txt hashes.txt
... (attempts to crack the passwords using the provided dictionary)
```

**Data sanitization** :
- Processus d'élimination définitive des données d'un dispositif de stockage.
_Informations_ : Assure que les données sensibles ne peuvent pas être récupérées une fois effacées.
_Technique_ : Peut impliquer plusieurs passes d'écriture de données aléatoires sur le dispositif.
```bash
user1$ shred -n 5 -z /path/to/file
... (overwrites the file 5 times with random data and then with zeros)
```

---

## 4.2 - Importance of policies, processes, and procedures for incident response.


**Incident response process (Processus de réponse aux incidents)** : Étapes structurées à suivre lors de la gestion d'un incident de sécurité. 

- **Preparation (Préparation)** : **Établir un plan** de réponse aux incidents. 
  _Informations_ : Inclut la **formation des employés, la mise en place d'outils** et la définition des rôles et responsabilités.
    
- **Identification (Identification)** : **Détecter un incident** de sécurité. 
  _Technique_ : Implique la **surveillance constante des systèmes** et des **logs** pour détecter les activités anormales.
    
- **Containment (Confinement)** : **Limiter l'impact de l'incident**. 
  _Technique_ : Peut être à court terme (par ex. **déconnecter un système du réseau**) ou à long terme (solutions plus permanentes).
    
- **Eradication (Éradication)** : **Trouver et éliminer la cause** de l'incident. _Technique_ : Cela pourrait impliquer la suppression de logiciels malveillants ou la correction de vulnérabilités.
    
- **Recovery (Récupération)** : **Restaurer les systèmes** pour la production. 
  _Informations_ : Retourner à la normale après que l'incident a été géré. 
  _Technique_ : **backup**
    
- **Lessons learned (Leçons apprises)** : **Examiner l'incident** pour éviter que des incidents similaires ne se reproduisent. _Technique_ : Cela implique généralement un **brainstorming** ou une revue de l'incident.


**Exercises (Exercices)** : Simulations pour tester et améliorer la préparation aux incidents. 
- **Tabletop** : Exercices basés sur la **discussion** pour évaluer les plans et les stratégies. 
  _Informations_ : Se concentre sur le dialogue entre les équipes et ne nécessite pas d'actions réelles. 
    
- **Walkthroughs (Parcours)** : Examen pas à pas des procédures et des réponses à un scénario. 
  _Informations_ : Ces exercices testent la compréhension des équipes des procédures.
    
- **Simulations** :  Exercices pratiques pour simuler un incident réel. 
  _Technique_ : Cela pourrait impliquer une attaque simulée sur l'environnement de l'organisation.
    

**<mark class="hltr-blue">Attack frameworks</mark> (Cadres d'attaque)** : Modèles offrant une compréhension des tactiques, techniques, et procédures couramment utilisées par les attaquants. 

- **MITRE ATT&CK** https://attack.mitre.org/: Site fournissant une base de connaissances des **TTPs** utilisées par les cyberattaquants. Il aide les organisations à mieux comprendre et à se défendre contre les menaces avancées. Trié grace au [[Cyber Kill Chain]] de Lockheed Martin

- **The Diamond Model of Intrusion Analysis** : (Modèle graphique) Modèle analytique pour représenter et évaluer les intrusions dans un réseau.
  _Technique_ : Les quatre points du diamant (adversaire, capacité, infrastructure, victime) sont utilisés pour représenter les aspects clés d'une intrusion.

- <mark class="hltr-blue">Cyber Kill Chain</mark> : Modèle décrivant les étapes qu'un attaquant doit franchir pour réussir une cyberattaque. [[Cyber Kill Chain]]


**Stakeholder management (Gestion des parties prenantes)** : Processus de gestion de la communication avec toutes les entités concernées lors d'un incident. 
_Informations_ : Essentiel pour maintenir la **confiance et la réputation pendant et après un incident**. 
_Technique_ : Les parties prenantes peuvent inclure des **employés, des clients, des partenaires**, des régulateurs et le grand public.

**Communication plan (Plan de communication)** : Stratégie pour gérer la communication interne et externe lors d'un incident. _Informations_ : Assure que les bonnes informations sont partagées avec les bonnes personnes au bon moment.

**Disaster recovery plan (DRP)** : Plan pour la reprise des opérations après un désastre majeur.  
_Technique_ : Le plan peut détailler les solutions de sauvegarde, les sites de secours et les procédures d'urgence.

**Business continuity plan (Plan de continuité des activités)** : Stratégie pour assurer la continuité des opérations critiques après un incident. _Informations_ : Se concentre sur la reprise des fonctions commerciales essentielles pendant et après un incident. _Technique_ : Peut inclure des plans pour la communication, la relocalisation des opérations et la gestion des ressources humaines.

**Continuity of operations planning (COOP) (Planification de la continuité des opérations)** : Plans pour garantir que les fonctions essentielles continuent après une urgence. _Informations_ : Priorise les fonctions et les opérations pour assurer la continuité en cas de perturbation majeure. _Technique_ : Les plans COOP peuvent inclure des solutions pour le personnel, les installations et les technologies.

**Incident response team (Équipe de réponse aux incidents)** : Groupe d'experts formés pour gérer et résoudre les incidents de sécurité.

**Retention policies (Politiques de rétention)** : Directives définissant **combien de temps les données doivent être conservées**. _Informations_ : Elles aident à gérer l'espace de stockage et à se conformer aux réglementations

---

## 4.3 - policies, processes, and procedures for incident response.

**Vulnerability scan output** : Résultats d'un scan indiquant les vulnérabilités détectées sur un système.

**SIEM (Security Information and Event Management)** : Plateforme de sécurité informatique qui centralise, normalise  et analyse les données pour détecter et répondre aux menaces potentielles.

- **Sensor (Forwarder Splunk)** : (**forwarder splunk**) Dispositif ou application qui collecte des données pour le SIEM. _Technique_ : Cela peut inclure des agents sur des serveurs, des sondes réseau, ou des collecteurs de journaux.
    
- **Sensitivity** : Réglage déterminant à quel point un capteur ou une alerte est réactif. _Informations_ : Un réglage trop sensible peut entraîner de nombreuses fausses alertes (**false positive**), tandis qu'un réglage pas assez sensible peut manquer des incidents.
    
- **Trends** : Analyse des données sur une période pour identifier les schémas ou les tendances. 
  _Technique_ : augmentation des tentatives de connexion échouées...
    
- **Alerts** : Notifications générées lorsque des événements spécifiques se produisent ou lorsque certains seuils (**threshold**) sont dépassés. 
    
- **Correlation** : Processus de liaison des événements provenant de différentes sources pour identifier des activités malveillantes. _Informations_ : La corrélation permet d'identifier des menaces qui ne seraient pas évidentes en examinant les événements individuellement. 

#### Log Files :

**Network Log** : Contient des informations sur le trafic du réseau.

```log
2023-08-09 12:15:23 SRC=192.168.1.5 DST=8.8.8.8 PROTO=TCP SPT=443 DPT=53
```

**System Log** : Registre des événements liés au système d'exploitation.

```log
2023-08-09 12:16:10 Kernel[0]: INFO: CPU0 temperature: 50°C
```

**Application Log** : Enregistre les événements d'une application spécifique.

```log
2023-08-09 12:18:04 MyApp: User 'admin' logged in successfully.
```

**Security Log** : Contient des informations liées à la sécurité, souvent des tentatives d'accès.

```log
2023-08-09 12:19:56 Failed password for root from 192.168.1.10 port 22 ssh2
```

**Web Log** : Journal des requêtes HTTP et des événements liés au serveur web.

```log
127.0.0.1 - - [09/Aug/2023:12:21:02 +0000] "GET /index.html HTTP/1.1" 200 2326
```

**DNS Log** : Enregistre les requêtes DNS.

```log
2023-08-09 12:22:08 client 192.168.1.5#5353: query: openai.com IN A + (10.0.0.1)
```

**Authentication Log** : Enregistre les tentatives d'authentification.

```log
2023-08-09 12:23:45 pam_unix(sshd:auth): authentication failure; logname= uid=0 euid=0 tty=ssh ruser= rhost=192.168.1.10
```

**Dump Files** : Ces fichiers capturent les données en mémoire lors d'une erreur système. Ils ne sont pas vraiment en format de journal, mais plutôt en format binaire.

```binary
...
Memory dump: 0x7ffa318c 8a b4 01 0a 00 00 00 00 ...
...
```

**VoIP and Call Managers Log** : Enregistre les événements de VoIP.

```log
2023-08-09 12:26:33 CallManager: New call from 1001 to 1002, CallID: 12345
```

**Session Initiation Protocol (SIP) Traffic Log** : Journal des requêtes SIP pour les appels VoIP.

```log
INVITE sip:user2@openai.com SIP/2.0
Via: SIP/2.0/UDP user1@openai.com;branch=z9hG4bK776asdhds
Max-Forwards: 70
From: "User1" <sip:user1@openai.com>;tag=1928301774
To: <sip:user2@openai.com>
Call-ID: a84b4c76e66710@openai.com
```


**syslog/rsyslog/syslog-ng** : (Logs Centralisés, serveur, protocoles port 514) Protocoles pour envoyer les logs vers un serveur qui **centralise** les logs de toute les sources du réseau.
_Technique_ : Syslog est le protocole standard, tandis que rsyslog et syslog-ng sont des améliorations offrant plus de fonctionnalités.

**journalctl** : (**Consulter les logs Linux**) Command Linux pour interroger le journal système de systemd.
_Technique_ : Permet d'afficher et de filtrer les entrées du journal système.

**NXLog** :  Outil pour collecter, traiter et transférer des événements de journalisation **(log event)**. _Informations_ : Similaire à syslog
_Technique_ : Peut être utilisé pour convertir des journaux dans **différents formats** ou pour **transférer des journaux** vers des destinations spécifiques.

**Bandwidth monitors** : Outils pour surveiller la quantité de bande passante utilisée. _Informations_ : Utile pour comprendre le trafic réseau et identifier les anomalies. 

**Metadata (Métadonnées)** : Données sur les données (horodatages, les emplacements, les tailles de fichier, etc.)

- **Email** : Métadonnées associées aux e-mails. l'expéditeur, le destinataire, la date et l'heure, l'objet, etc. 
  _Technique_ : Utile pour enquêter sur les campagnes de phishing ou les fuites d'informations.
    
- **Mobile** : Métadonnées liées à l'utilisation des appareils mobiles.
    
- **Web** : Métadonnées liées à l'activité web. _Informations_ : Cela peut inclure des URL visitées, des horodatages, des tailles de transfert, etc. 
    
- **File** : Métadonnées associées aux fichiers. _Informations_ : Cela peut inclure le type de fichier, la date de création, la date de modification, etc. 
    
**Netflow/sFlow** : (**Flow analysis = vue d'ensemble VS Packet analysis = Wireshark, précis**) Outils pour collecter des informations sur le trafic réseau.
 _Informations_ : Ils fournissent une vue de haut niveau du trafic réseau sans capturer le contenu réel des paquets.

- **Netflow** : Protocole développé par Cisco pour la collecte et la surveillance du trafic réseau. _Informations_ : Fournit des statistiques détaillées sur les flux IP dans un réseau. _Technique_ : Communément utilisé pour l'analyse de la performance, la facturation et la détection d'anomalies.
    
- **sFlow** : **(à mis-chemin entre Netflow & Wireshark, echantillonnage)** Standard pour la surveillance du trafic réseau. Il ne capture pas tous les paquets, mais seulement un échantillon de paquets, ce qui le rend plus scalable pour surveiller des réseaux à grande échelle.
    
- **IPFIX** : (**Successeur de Netflow, plus fexible**) Standard pour exporter des informations sur le trafic réseau. 
  _Informations_ : Permet une représentation plus flexible et extensible des données de trafic.

**Protocol analyzer output** : (**Wireshark**) Ces outils capturent et analysent les paquets réseau pour fournir des informations détaillées sur le trafic


---

## 4.4 - Given an incident, apply mitigation techniques or controls to secure an environment.

**Reconfigure endpoint security solutions** : Adapter les paramètres de sécurité pour protéger les dispositifs individuels (**antivirus, EDR**...).

- **Application approved list**: Liste des applications autorisées à s'exécuter sur un système.
- **Application blocklist/deny list**: Liste des applications interdites d'exécution. _Informations_: Bloque les applications non désirées ou potentiellement nuisibles.  
- **Quarantine (Mise en quarantaine)**: Isoler un élément suspect pour éviter qu'il ne cause des dommages. _Informations_: Les fichiers ou programmes mis en quarantaine ne peuvent pas s'exécuter tant qu'ils ne sont pas examinés ou supprimés. 
    
**Configuration changes (Modifications de configuration)**: Ajustements des paramètres pour renforcer la sécurité. 

- **Firewall rules (Règles de pare-feu)**: Instructions pour autoriser ou bloquer le trafic réseau (IP source, la destination, le port et le protocole.). 
    
- **MDM (Mobile Device Management)**: Outil pour gérer et sécuriser les dispositifs mobiles dans une entreprise. 
  _Informations_: Permet aux entreprises de contrôler les paramètres, les applications et les données sur les dispositifs mobiles. 
  _Technique_: Les solutions populaires incluent **AirWatch, MobileIron et Intune**.
    
- **DLP (Data Loss Prevention)**: Solutions pour empêcher la fuite de données sensibles. _Informations_: Détecte et bloque les transferts non autorisés de données. 
  _Technique_: Peut être basé sur des règles, des empreintes digitales de données ou des modèles de comportement.
    
- **Content filter/URL filter**: Bloque l'accès à des URL
    
- **Update or revoke certificates (Mettre à jour ou révoquer des certificats)**: Modifier ou retirer la validité d'un certificat.
  _Technique_: Utilisé dans la gestion de certificats pour garantir l'**intégrité et la confidentialité**.
    
**Isolation**: Séparer un élément potentiellement compromis des autres pour éviter la propagation. 
_Technique_: Peut être réalisé en **déconnectant physiquement un appareil** ou en utilisant des **solutions logicielles** pour le mettre en **"mode isolé"**.

**Containment (Confinement)**: Limiter l'impact d'une menace en la contenant dans une zone spécifique. 
_Technique_: Cela peut être fait en isolant les systèmes affectés, en bloquant le trafic réseau ou en désactivant les comptes compromis.

<mark class="hltr-blue">Segmentation</mark> : Diviser un réseau en segments distincts pour améliorer la sécurité et la performance. 
_Informations_: **Chaque segment fonctionne comme un réseau distinct**, limitant la portée des attaques ou des pannes. 
_Technique_: Souvent réalisé à l'aide de <mark class="hltr-blue">VLANs</mark> ou de sous-réseaux.

**SOAR (Security Orchestration, Automation, and Response)** : **Le SOAR complète le SIEM en automatisant et en orchestrant les actions de réponse aux incidents de sécurité**. Il peut exécuter des tâches telles que la quarantaine d'un appareil compromis, le blocage d'une adresse IP malveillante ou l'envoi de notifications d'alerte aux équipes de sécurité.
sandboxes

- **Runbooks**: (Opérationnel, tuto) Un runbook est un ensemble d'instructions étape par étape pour exécuter des tâches opérationnelles régulières.
  _Informations_: Permet une réponse standardisée et rapide à des types d'incidents courants. 
  Pour la maintenance régulière du serveur, pourrait avoir des étapes pour vérifier l'espace disque, optimiser la base de données, et redémarrer les services nécessaires.
    
- **Playbooks**: (letsdefend closing alert) Scénarios détaillés pour répondre à des incidents de sécurité.
  _Technique_: Peut être utilisé pour former des équipes de sécurité sur la manière de répondre à divers types d'incidents.
    

<mark class="hltr-blue">VLANs</mark> : Virtual Local Area Networks, réseaux logiques créés pour segmenter un réseau physique.

---
## 4.5 - key aspects of digital forensics

**Documentation/evidence (Documentation/preuve)** : Informations et preuves recueillies lors d'une enquête numérique.

- **Legal hold (Conservation légale)** : Obligation de conserver des informations pertinentes pour des litiges en cours ou à venir (émise par un tribunal ou une entité juridique). 
    
- **Video** : Enregistrements vidéo utilisés comme preuve (caméra, dashcams...). 
    
- **Admissibility (Admissibilité)** : Capacité d'une preuve à être acceptée dans une procédure judiciaire. _Informations_ : Pour qu'une preuve soit admissible, elle doit être pertinente, fiable et obtenue légalement.
    
- **<mark class="hltr-blue">Chain of custody </mark> (Chaîne de garde)** : Documentation qui enregistre la manipulation d'une preuve (assurer l'intégrité lors d'une procédure judiciaire)
  _Technique_ : Souvent un **formulaire physique ou numérique qui est rempli chaque fois que la preuve est manipulée ou transférée**.

- **Timelines of sequence of events (Chronologies des séquences d'événements)** : Ordre chronologique des événements relatifs à un incident (**logs, horodatages, metada...**). 
    
    - **Time stamps (Horodatages)** : Marques temporelles associées à un événement ou à une donnée.
        
    - **Time offset (Décalage temporel)** : Différence entre l'heure enregistrée et l'heure réelle (**fuseau horaire incorrects** ou d'autres facteurs).
        
- **Tags (Étiquettes)** : Marqueurs ou étiquettes utilisés pour catégoriser ou marquer des données. _Informations_ : Aide à l'organisation et à la recherche de preuves ou d'informations. 
    
- **Reports (Rapports)** : Résumés écrits des résultats d'une enquête ou d'une analyse. 
    
- **Event logs (Journaux d'événements)** : Enregistrements des activités sur un système ou un réseau. _Informations_ : Crucial pour comprendre ce qui s'est passé avant, pendant et après un incident.
    
- **Interviews** : Conversations avec des individus pour recueillir des informations. 

**<mark class="hltr-blue">Acquisition</mark>** : Processus de collecte de preuves ou de données numériques. 

- **Order of volatility (Ordre de volatilité)** : Priorisation de la collecte de preuves basée sur la durée de vie des données. 
  _Informations_ : **Les données les plus volatiles, comme la mémoire RAM, sont recueillies en premier car elles sont rapidement perdues**. 
    
- **Disk** : Stockage non volatil où les données sont conservées à long terme. 
    
- **Random-access memory (RAM)** : Mémoire volatile utilisée pour le stockage temporaire des données. 
  _Informations_ : Peut contenir des informations sur les processus en cours d'exécution, les connexions réseau et d'autres activités. 
  _Technique_ : Les outils comme **Memdump** peuvent être utilisés pour extraire le contenu de la RAM.
    
- **Swap/pagefile** : Espace sur le disque utilisé comme extension de la RAM. _Informations_ : Peut contenir des fragments de données qui étaient précédemment en mémoire. 
  _Technique_ : Analysé pour récupérer des informations qui ont été échangées hors de la RAM.
    
- **OS (Système d'exploitation)** : Les enquêteurs peuvent examiner les journaux système, les fichiers de configuration et d'autres ressources pour obtenir des informations.
    
- **Device (Dispositif)** : Tout équipement capable de traiter des données, comme un ordinateur, un smartphone ou un routeur. Les dispositifs sont souvent saisis et analysés lors d'enquêtes numériques.
    
- **Firmware** : **Logiciel intégré à un composant matériel**. _Informations_ : Peut contenir des informations sur le fonctionnement d'un dispositif ou d'autres détails techniques.
  **Driver** : logiciel qui permet à un OS de communiquer avec un périphérique
    
- **Snapshot** : Image d'un état spécifique d'un système à un moment donné. _Informations_ : Permet aux enquêteurs de revenir à un état précis pour l'analyse. 
    
- **Cache** : Stockage temporaire de données fréquemment utilisées pour accélérer l'accès. _Informations_ : Peut contenir des fragments d'informations précieuses pour une enquête. _Technique_ : Le cache du navigateur, par exemple, peut contenir des fragments de sites web visités.
    
- **Network** : Ensemble de dispositifs interconnectés pour partager des ressources. _Informations_ : Peut fournir des preuves sur la communication ou le transfert de données. _Technique_ : Les journaux de pare-feu, les journaux de serveurs et d'autres ressources réseau sont souvent examinés.
    
- **Artefacts** : Traces ou les éléments observables que les attaquants laissent sur le système. 
  _Informations_ : Peut fournir des indices sur les actions d'un utilisateur ou d'un programme. 
  _Technique_ : Les artefacts peuvent être trouvés dans de nombreux endroits, tels que le cache, les fichiers temporaires, ou les logs.

**On-premises vs. cloud (Sur site vs. cloud)** : Comparaison entre les données stockées localement (sur site) et celles stockées dans le cloud. 
_Informations_ : Le stockage dans le cloud peut présenter des défis en matière de juridiction et de contrôle. 

- Right-to-audit clauses : (Droit d'inspecter le respect des règles de ses fournisseurs) Clause contractuelle qui donne à une organisation le droit d'inspecter et d'examiner les activités d'un fournisseur pour assurer la conformité.
  _Informations_ : Assure que les fournisseurs de services respectent les normes et les réglementations. 
    
- **Regulatory/jurisdiction (Réglementation/juridiction)** : (Lois, Territoire, Conformité) Les réglementations et les lois spécifiques qui s'appliquent à une organisation en fonction de son emplacement géographique ou de son secteur d'activité.
  _Technique_ : Les enquêteurs doivent être conscients des lois applicables lors de l'accès ou de la collecte de données.
    
- **Data breach notification laws (Lois sur la notification des violations de données)** : Réglementations qui obligent les organisations à informer les parties concernées en cas de violation de données. 
  _Informations_ : Aide à assurer la transparence et à protéger les droits des individus. 
  _Technique_ : Les organisations doivent avoir des procédures en place pour détecter, signaler et répondre aux violations de données conformément à ces lois.
    

**Integrity (Intégrité)** : Assurance que les données n'ont pas été altérées de manière non autorisée.

- **Hashing** : Processus de conversion de données en une chaîne de caractères fixe, souvent utilisé pour vérifier l'intégrité des données. Si le hash d'un fichier change, cela indique que le fichier lui-même a été modifié.
    
- **Checksums** : Valeurs calculées à partir de données pour vérifier leur intégrité. _Informations_ : **Similaire au hachage, mais souvent utilisé pour de plus petits ensembles de données**. _Technique_ : Souvent utilisées pour vérifier l'intégrité des **téléchargements ou des transferts de fichiers**.
    
- **Provenance** : Origine ou source d'un élément ou d'une donnée. 
  _Technique_ : Les enquêteurs peuvent utiliser des métadonnées, des logs ou d'autres preuves pour déterminer la provenance des données.
    

**Preservation (Préservation)** : Protection et conservation des preuves pour s'assurer qu'elles restent intactes et non altérées. _Informations_ : Essentiel pour garantir que les preuves peuvent être utilisées dans une procédure judiciaire ou une enquête. _Technique_ : Les preuves peuvent être conservées en les stockant dans un environnement sécurisé, en les copiant sur des supports de stockage non modifiables ou en utilisant d'autres méthodes pour prévenir toute altération.

**E-discovery** : Processus de découverte de preuves électroniques dans le cadre d'une procédure judiciaire. _Informations_ : Les organisations peuvent être tenues de produire des documents électroniques comme preuve lors d'un litige. _Technique_ : Des outils et des processus spécialisés sont utilisés pour identifier, collecter, conserver et analyser des preuves électroniques pertinentes.

**Data recovery (Récupération de données)** : Processus de récupération de données à partir de supports de stockage endommagés ou inaccessibles. 
_Technique_ : Les outils comme ddrescue ou TestDisk peuvent être utilisés pour récupérer des données à partir de disques endommagés.

**Non-repudiation** : Assurance qu'une partie ne peut pas nier une action qu'elle a effectuée.  
_Technique_ : Souvent réalisé en utilisant des signatures numériques ou d'autres mécanismes d'authentification.

**Strategic intelligence/counterintelligence (Renseignement stratégique/contre-espionnage)** : Informations utilisées pour prendre des décisions stratégiques ou pour **protéger une organisation contre l'espionnage**. 
_Technique_ : Peut inclure l'analyse de tendances, la surveillance des menaces émergentes ou la collecte d'informations sur des adversaires potentiels.

---

