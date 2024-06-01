CheatSheet Cybersécurité 

## Les commandes essentielles en cybersécurité
En tant que professionnel de la cybersécurité, il est essentiel de maîtriser les commandes de base pour effectuer des tâches courantes. Dans cet article, nous allons explorer les commandes les plus importantes que tout le monde devrait connaître, y compris les commandes spécifiques à Windows.


### ping
La commande `ping` permet de vérifier la connectivité réseau entre votre ordinateur et une adresse IP ou un nom de domaine. Elle envoie des paquets ICMP et attend la réponse pour déterminer si la connexion fonctionne.

Exemples d'utilisation :
- `ping www.google.com`
- `ping -c 5 www.google.com` (envoyer 5 paquets)
- `ping -i 2 www.google.com` (intervalle de 2 secondes entre les paquets)
- `ping -t www.google.com` (ping en continu jusqu'à l'arrêt)

### traceroute
La commande `traceroute` (ou `tracert` sur Windows) permet de suivre le chemin emprunté par les paquets pour atteindre une destination. Elle affiche les différents routeurs traversés et le temps de réponse de chaque saut.

Exemples d'utilisation :
- `traceroute www.example.com` (sur Linux/macOS)
- `tracert www.example.com` (sur Windows)
- `traceroute -m 20 www.example.com` (limiter à 20 sauts)
- `traceroute -n www.example.com` (afficher les adresses IP au lieu des noms de domaine)

### nslookup
La commande `nslookup` permet d'interroger un serveur DNS pour obtenir des informations sur un nom de domaine, comme son adresse IP.

Exemples d'utilisation :
- `nslookup www.example.com`
- `nslookup -type=mx www.example.com` (rechercher les enregistrements MX)
- `nslookup -type=ns www.example.com` (rechercher les enregistrements NS)
- `nslookup -debug www.example.com` (mode débogage)

### netstat
La commande `netstat` affiche les connexions réseau actives sur votre système, ainsi que les ports ouverts et les processus associés.

Exemples d'utilisation :
- `netstat -antp` (sur Linux/macOS)
- `netstat -ano` (sur Windows)
- `netstat -antp | grep ESTABLISHED` (afficher les connexions établies)
- `netstat -antp | grep LISTEN` (afficher les ports en écoute)

### ssh
La commande `ssh` permet de se connecter de manière sécurisée à un serveur distant en utilisant le protocole SSH.

Exemples d'utilisation :
- `ssh user@example.com`
- `ssh -p 2222 user@example.com` (se connecter sur le port 2222)
- `ssh -i /path/to/key.pem user@example.com` (se connecter avec une clé privée)
- `ssh -L 8080:localhost:80 user@example.com` (créer un tunnel SSH)

### nmap
La commande `nmap` est un outil puissant de découverte de réseau et d'analyse de ports. Elle permet de scanner des hôtes et des réseaux pour identifier les systèmes actifs, les services en cours d'exécution et les vulnérabilités potentielles. 

Exemples d'utilisation :
- `nmap -sV www.example.com` (détection des versions de services)
- `nmap -sS -p- www.example.com` (scan TCP SYN de tous les ports)
- `nmap -sU -p123,161,500 www.example.com` (scan UDP de ports spécifiques)
- `nmap -sC www.example.com` (utiliser des scripts Nmap par défaut)

### tcpdump
La commande `tcpdump` est un analyseur de trafic réseau en ligne de commande. Elle permet de capturer et d'analyser les paquets qui transitent sur un réseau, ce qui peut être utile pour le dépannage et l'analyse de la sécurité.

Exemples d'utilisation :
- `tcpdump -i eth0 -n` (sur Linux/macOS)
- `tcpdump -i any -s0 -w capture.pcap` (capturer le trafic dans un fichier)
- `tcpdump -i eth0 -n tcp port 80` (capturer le trafic HTTP)
- `tcpdump -i eth0 -n src host 192.168.1.100` (capturer le trafic d'une adresse IP)

## Commandes Windows

### ipconfig
La commande `ipconfig` permet d'afficher les paramètres de configuration IP de votre système Windows, comme l'adresse IP, le masque de sous-réseau et la passerelle par défaut.

Exemples d'utilisation :
- `ipconfig`
- `ipconfig /all` (afficher toutes les informations)
- `ipconfig /renew` (renouveler l'adresse IP DHCP)
- `ipconfig /flushdns` (vider le cache DNS)

### arp
La commande `arp` (Address Resolution Protocol) permet d'afficher et de manipuler la table ARP de votre système Windows, qui contient les correspondances entre les adresses IP et les adresses MAC.

Exemples d'utilisation :
- `arp -a` (afficher la table ARP)
- `arp -d 192.168.1.100` (supprimer une entrée de la table ARP)
- `arp -s 192.168.1.100 00-11-22-33-44-55` (ajouter une entrée statique)

### route
La commande `route` permet d'afficher et de modifier la table de routage de votre système Windows, qui contient les informations sur les itinéraires utilisés pour acheminer le trafic réseau.

Exemples d'utilisation :
- `route print` (afficher la table de routage)
- `route add 192.168.2.0 mask 255.255.255.0 192.168.1.1` (ajouter une route statique)
- `route delete 192.168.2.0` (supprimer une route)

## Wireshark
Wireshark est un puissant analyseur de protocoles réseau avec une interface graphique. Il permet d'intercepter, de décoder et d'analyser en détail le trafic réseau, ce qui en fait un outil essentiel pour les professionnels de la cybersécurité.

Exemples d'utilisation :
- Lancer l'application Wireshark et commencer à capturer le trafic réseau
- Filtrer le trafic par protocole, adresse IP, port, etc.
- Analyser les paquets capturés et décoder les protocoles
- Exporter les données capturées dans différents formats
