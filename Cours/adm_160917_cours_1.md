Administration des systèmes sous Linux

Introduction

Système d’exploitation multi-tâches
créé aux États-Unis au début des années 1970
historiquement le premier système moderne multi-utilisateurs

Variantes du noyau UNIX
(HP/UX, AIX, SOLARIS, SCO, FreeBSD, NetBSD, OpenBSD)
Linux s’inspire d’UNIX : il possède son propre noyau créé de toutes pièces par un Finlandais (Linus Torvalds) au début des années 1990
Linus Torvalds a créé un noyau linux libre .

Depuis, des centaines de versions de Linux ont vu le jour, toutes ces versions avec leurs spécificités.

On associe souvent le fait que Linux soit gratuit à Linus alors que, en réalité, l’inventeur de la « Licence libre » et du développement communautaire est Richard Stallman
Août 1991 : 1ere version libre code source : 63 Ko

Sous unix, tout est fichier :
fichier
répertoires
devices
liens
pipes
sockets
Sous unix, les fichiers doivent être : 
Lisibles par l’homme
exploitables simplement par la machine ….
Donc sous Unix :
tous les fichiers de configuration sont textes …
.. ou générés à partir de fichiers texte
pas de binaire : les fichiers de configuration 
doivent être éditables simplement (≠registry)
pas de formats exotiques (≠xml)
pas de formats fermés (≠doc,byo,…)
10 milliards d’unités connectées dans le monde ( Ordinateurs, Smartphones, Tablettes, GPS…)
certains ont fatalement envie de nuire ou de jouer
Facteurs de motivation des pirates
le goût du defi
l’appât du gain
la volonté de s’octroyer des moyens informatiques dont on rêve (débit, puissance, disque, etc)
la méconnaissance des risques et des conséquences
Choix de la distribution

Plus de 350 distributions sur le « marché »

Points commun :
kernel 
outils GNU							
Différences :
kernel
outils GNU
système de packages
fichiers de configuration
 fichiers de démarrage
organisation et type du filesystem
philosophie
canaux de distributionsméthode d’installation, de configuration
outils
….
Linux Mint
Le plus populaire de toutes les distributions
Facile d’utilisation et d’installation

Ubuntu

Distribution préférée pour l’utilisateur débutant
Fournit un environnement agréable grâce une sélection de programmes installés par défaut
Bénéficie d’un bon support matériel et de la meilleure communauté française, très active et compétente
Environnement par d »fait : Unity (GNOME) 

Kubuntu

Idem, mais avec l’environnement graphique KDE

Xubuntu
Dérivée d’Ubuntu
Facile d’utilisation mais moins maniable qu’Ubuntu pour les utilisateurs novices
Environnement par défaut : Xfce 

Debian

Distribution non commerciale
Crée en 1993 par Ian Murdock
Souvent utilisée pour les serveurs
Utilisée comme base pour de nombreuses autres distributions

Archlinux

Inspirée par Crux Linux
Conçue pour les utilisateurs avancés
Reste simple et léger
Pas d’outils graphiques de base

Fedora

Basée sur la distribution Red Hat
Projet débuté en fin 2003
Toujours à la pointe de l’innovation
Cycle de version très court 

Suse

Très bon programme de configuration centralisé
Bon support matériel
Principal défaut : Une communauté francaise plus réduite
Environnement par défaut : KDE

Mandriva

Large gamme de matériel supporté, beaucoup d’outils d’administration
Une communauté active pour aider à affronter les débuts difficiles
Environnement par défaut : KDE

Kali Linux ( ex BackTrack)

Système orienté sécurité (ex : John the ripper pour tester les mdp )
Prisée par les pirates et administrateurs systèmes
Nombreux outils de tests de sécurité
Environnement par défaut : KDE
Basée sur Debian 


Les menaces

Les maliciels

Définition : portion de code informatique inoffensif ou destructeur capable de se reproduire et de se propager caché dans le corps d’un autre programme.

Propagation : par infiltration des programmes chargés en mémoire pour exécution ou de ceux stockés sur le disque dur puis diffusion su rle net souvent via les courriels

Action : lors de leur phase active ils peuvent provoquer un simple affichage sur l’écran ou  supprimer des fichiers

Programme malveillant, leur but est de perturber, détruire ou altérer le bon fonctionnement d’un système informatique.

4 types : les virus, les vers, les chevaux de troie et les bombes logiques

Les virus

de secteur d’amorcage
à infection de fichiers
résidents en mémoire
non résidents en mémoire
multiformes
furtifs
polymorphes ( ou mutants )
fibustiers

Les vers ( worms )

Ce sont les plus fréquents depuis la généralisation de l’accès a l’internet haut débit et le manque de conscience sécuritaire

Les chevaux de troie

Les chevaux de troie permettent la prise de contrôle d’une machine, ils sont installés par l’utilisateur lui même car emballés dans un logiciel dont il a besoin.




Les bombes logiques

Les bombes logiques sont déclenchées par un événement déterminé par le programmeur malveillant :
Combinaison de otuches, date, ensemble de conditions (ex : employé mal intentionné)

Les fork bombes

Une fork bombes créée un grand nombre de processus afin de saturer l’espace disponible dans la liste des processus (while (true) {fork} )

Les porte dérobée (backdoor)

Permet d’ouvrir un accès réseau frauduleux sur un système informatique. Il est ainsi possible d’exploiter à distance la machine

Les logiciels espion (spyware)

Fait de la collecte d’informations personnelles sur l’ordinateur d’un utilisateur sans son autorisation. Ces informations sont ensuite transmises à un ordinateur tiers

L’enregistreur de frappe (keylogger)

Programme généralement invisible installé sur le poste d’un utilisateur et chargé d’enregistrer à son insu ses frappes clavier, pour intercepter des mots de passe par exemple

L’exploit

Programme permettant d’exploiter une faille de sécurité d’un logiciel

Le rootkit

Ensemble de logiciels permettant généralement d’obtenir les droits d’administrateur sur une machine, d’installer une porte dérobée, de truquer les informations susceptibles de révéler la compromission, et d’effacer les traces laissées par l’opération dans les journaux système.

Le pourriel (spam)

Un courrier électronique non sollicité, la plupart du temps de la publicité. Ils encombrent le réseau, et font perdre du temps à leurs destinataires



L’hameçonnage (phishing)

Un courrier électronique dont l’expéditeur se fait généralement passer pour un organisme fiancier et demandant au destinataire de fournir des informations confidentielles
Le canular informatique (hoax)

Un courrier électronique incitant généralement le destinataire à retransmettre le message à ses contacts sous divers prétextes. Ils encombrent le réseau, et font perdre du temps à leurs destinataires. Dans certains cas, ils incitent l’utilisateur à effectuer des manipulations dangereuses sur son poste (suppression d’un fichier prétendument lié à un virus par exemple)  

Les écoutes (sniffing)

(Snort sur kali)
Technique permettant de récupérer toutes les informations transitant sur un réseau (on utilise pour cela un logiciel sniffer). Généralement utilisée pour récupérer les mots de passe des applications et pour identifier les machines qui communiquent sur le réseau

L’usurpation d’identité (spoofing)

(copie de cookie)
Technique consistant à prendre l’identité d’une autre personne ou d’une autre machine. Généralement utilisée pour récupérer des informations snesibles, que l’on pourrait pas avoir autrement

Le déni de service (denial of service ou DoS)

Technique visant à provoquer des interruptions de service, et ainsi d’empecher le bon fonctionnement du système.
DoS (att aque solo )
DDoS (attaque a plusieurs )

Les rancongiciels 

Consiste, via des bannières publicitaires, à infecter les ordinateurs, et plus particulièrmeent, les ordinateurs dont les logiciels, principalement JAVA et ADOBE FLASH


Configuration, commandes et Filesystems

Responsabilité de l’administrateur

Trois grandes familles de taches incombent à l’administrateur Unix :
gérer le système, les services et la sécurité

Surveiller et assurer la bonne marche du système quotidien :
Surveiller les ressources (disque, mémoire, CPU, etc)
planifier l’ajout des ressources

Administrer les services déployés :
Gérer les utilisateurs
Installer et configurer les applications
planifier les migrations

Prévoir et gérer les incidents et intrusions (tâches transversales)
Installer les correctifs de sécurité
« Durcir » le système et les applications
Superviser le système et les applications 
Mettre en œuvre un plan de sauvegarde

Les paquetages ( packages )

Un paquetage contient :
les fichiers ( exécutables, librairies, fichier de configuration, ressources, etc) nécessaires pour exécuter un programme 
Un ensemble de scripts qui configurent le programme automatiquement après sont installation
Les informations sur le propriétaire et permissions d’accès de chaque fichiers
Des informations optionnelles sur les paquetages dépendants et services fournis
Une description du paquetage
L’ensemble des informations de tous les paquetages installés sont stockés dans une bases

Packages rpm
Le nom d’un fichier de paquetage est constitué du nom du paquetage, du numéro de version du logiciel et du numéro de version du paquetage séparés par des caractères « - »
Par exemple : openssl-0.9.7a-35.rpm


Packages dpkg
Le nom d’un fichier de paquetage est constitué :
du nom du paquetage suivi
du numéro de version du logiciel et du numéro de version du paquetage

Les dépôts de logiciels apt

Un depot Debian est un ensemble organisé et indexé de paquetages Debian et que l’infrastructure apt ( Advanced Packaging Tool) de gestion des paquetages Debian sait utiliser pour installer des applications

Un dépôt Debian peut être stocké sur différents supports :
CD
DVD
Un répertoire sur un système de fichiers
un emplacement sur le réseau accessible en HTTP ou FTP
…

Il existe plusieurs types de dépôts Debian :
Dépôts officiels de la distribution
Dépôt officiel contenant les correctifs de sécurité
Dépôt « volatile »
Dépôts Debian non officiels

L’utilisation des quatre premiers répertoires est simple:il suffit d’y copier un fichier exécutable (ou de créer un lien ) afin d’en activer l’exécution périodique

Le planificateur de taches ( cron) 

Le planificateur de tâche cron permet à chaque utilisateur de configurer l’exécution périodique de commandes via l’utilisation de la commande crontab

L’utilisateur root dispose également de cette possibilité. Cependant, pour installer l’exécution périodique de tâches relatives à la gestion du système, on préférera l’utilisation des répertoires suivants :
/etc/cron.hourly pour une exécution toutes les heures
/etc/cron.daily pour une exécution tous les jours
/etc/cron.weekly pour une exécution hebdomadaires
/etc/cron.monthly pour une exécution mensuelles 
/etc/cron.d qui permet d’affiner plus précisement la planification

L’utilisation des quatre premiers répertoires est simple : il suffit d’y copier un fichier exécutable (ou de créer un lien) afin d’en activer l’exécution périodique
L’utilisation du répertoire /etc/cron.d est plus particulière. Les fichiers contenus dans ce répertoire sont des fichiers texte qui adoptent un format quasi-identique à celui des fichiers manipulés par la commande crontab

La seule information ajoutée est l’utilisateur qui sera utilisé pour exécuter la commandes

Par exemple :
MAILTO=root
#mn ht fzy month dow user command 
0 4 * * * postgres /usr/lib/postgresql/bin/do.maintenance-a

Le fichier /etc/crontab contrôle les jours et heures d’exécution des commandes présentes dans les répertoires /etc/cron.* (excepté /etc/cron.d)

Les planifications créées par les utilisateurs sont stockées à raison d’un fichier pour chaque utilisateur dans le répertoire /var/spool/cron

Collecte et journalisation de messages (syslog)

Le mécanisme Unix traditionnel pour la collecte des messages générés par le système ou les applications est Syslog

syslogd et klogd sont les programmes (démons) utilisés pour cela

syslogd se charge de la collecte et répartition des messages, klogd n’a pour tâche que de passer les messages du noyau à syslogd

Il est possible de rediriger ces messages selon leur origine et/ou leur niveau vers des fichiers, la console, etc

Voir vers Syslog d’une autre machine

Le fichier de configuration de syslogd est /etc/syslog.conf

Par défaut, la quasi-totalité des messages sont dirigés vers un ensemble de fichier situés dans le répertoire /var/log

Les sources des messages sont appelées « facilités »

auth		messages concernant la sécurité ou l’authentification
authpriv	comme auth mais susceptible de contenir des informations privées
cron		messages générés par les planificateurs de tâches cron
daemon	un des démons du système sans classification particulière
kern		messages du noyau
lpr		messages du sous-système d’impression
mail		messages du sous-système de messagerie
mark		marqueurs de temps générés par Syslog
news		messages du sous-système de gestion USENET
syslog		messages internes de Syslog
user		messages utilisateur génériques
uucp		messages du sous-système UUCP
local0-local7	facilités utilisées à la discrétion de l’utilisateur

Les niveaux de priorités (par ordre de gravité) :

debug			messages destinés au débuggage
information		informations notice normal mais significatif
warning		avertissement
err			conditions d’erreur
crit			conditions critique
alert			action à gérer immédiatement
emerg			système inutilisable 

priorité « none » = cacher les logs
priorité « * » = affiche tous les logs

le caractère « ! » utilisé devant la priorité indique de ne pas en tenir compte

Arrêter et démarrer des services

La commande service est utilisée pour arrêter ou démarrer les services

Elle s’utilise : # service nom action

Ou nom est le nom d’un service (tel que présent dans le répertoire /etc/init.d) et action le type d’action à entreprendre :
stop arrête le service
start démarre le service 
reload demande au service de relire sa configuration
status affiche l’état du service 

On peut également utiliser cette syntaxe :
# /etc/init.d/nom action

Déplacements dans le fs (Change Directory)

cd argument

« rentre » dans le répertoire argument
Après un changement de répertoire courant, l’ancien répertoire courant ests tocké dans ‘-’ permettant d’y revenir avec ‘cd’

Exemples :
cd (equivaut à ‘cd$HOME’)
cd ..
cd -
cd /tmp
cd tmp

Lister les fichiers d’un répertoire (List Sorted)

ls option argument

liste les fichiers/répertoires correspondant à argument ou dans le répertoire argument

Options :
-a : affiche tous les fichiers ( y compris ceux commençant par ‘.’ )
-l : listing étendu
-R : récursif
-S : tri par taille
-t : tri par date de modification
-1 : affichage sur une colonne

Exemples :
ls *.txt
ls /etc
ls /etc/host*
ls /etc/rc[1-3].d
ls /media/win/Program\ Files/
ls -laR ~

La commande manuel ( man )

man commande

affiche le manuel de la commande commande 


Option :
-t : produit une sortie postscript pour impression
Exemples :
man -t ls | lpr
man man 

man divise la documentation en 9 sections :
1. Exécutable programs or shell commands
2. System calls
3. Library calls
4. Special files
5. File formats and conventions
6. Games
7. Miscellaneous
8. System administration commands
9. Kernel.routines

man divise la documentation en 9 sections, cela permet d’éviter les ambiguïtés
 
