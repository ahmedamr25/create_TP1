<img width="1372" height="845" alt="1" src="https://github.com/user-attachments/assets/7dc1451e-df0b-4215-a819-22a59cfd11aa" />

Cette image est très probablement la page d'accueil ou de bienvenue d'un environnement de formation ou d'un système d'exploitation nommé "Mobexler". Le slogan "FOR HACKERS BY HACKERS" (Pour les hackers, par des hackers) indique clairement qu'il s'agit d'une plateforme dédiée à la cybersécurité, au pentesting (tests d'intrusion) et au hacking éthique. C'est l'interface de démarrage avant de passer aux actions techniques

<img width="1260" height="688" alt="2" src="https://github.com/user-attachments/assets/edcf6833-ec61-452b-8b0d-83466c44d218" />
ip a (équivalent moderne de ifconfig). Cela permet de lister toutes les interfaces réseau de la machine et leurs configurations.

lo (loopback) : L'interface virtuelle locale (127.0.0.1) utilisée pour la communication interne de la machine.

enp0s8 : Une interface Ethernet. Le statut <NO-CARRIER> signifie qu'aucun câble n'y est branché ou qu'elle ne reçoit pas de signal.

enp0s17 : L'interface principale connectée. On voit qu'elle a reçu une adresse IP en DHCP : 10.0.2.15/24. C'est l'adresse de la machine sur le réseau local.


<img width="1320" height="193" alt="3" src="https://github.com/user-attachments/assets/80d81943-a322-4b2d-bafe-d28a3c70e420" />
La commande ip route affiche le chemin que les paquets réseau vont emprunter pour sortir de la machine.

La route par défaut : default via 10.0.2.2. Cela signifie que tout le trafic destiné à Internet (qui ne fait pas partie du réseau local) est envoyé vers la passerelle 10.0.2.2.

Le réseau local : 10.0.2.0/24 dev enp0s17. Cela confirme que l'interface enp0s17 est bien connectée au réseau 10.0.2.x et peut communiquer directement avec les machines de cette plage sans passer par la passerelle.

<img width="1151" height="366" alt="4" src="https://github.com/user-attachments/assets/1ccc8730-a507-4d86-bde2-09c1b33a310d" />
 un ping vers l'adresse IP 8.8.8.8.

8.8.8.8 est le serveur DNS public de Google, très utilisé pour tester la connexion Internet.

Résultat : Les deux paquets sont revenus avec un temps de réponse d'environ 30 ms.

Conclusion : La connectivité IP fonctionne parfaitement (0% de perte). Cela confirme que la configuration IP et la passerelle par défaut (vue dans l'image 3) sont correctes.

<img width="1435" height="425" alt="5" src="https://github.com/user-attachments/assets/ebe51c23-e87c-4c26-a1cd-8ca82409a934" />


un ping vers google.com.

Résolution DNS : La commande a automatiquement traduit le nom de domaine google.com en adresse IP : 142.250.200.142. C'est le rôle du serveur DNS.

Connectivité : Les pings sont réussis.

Conclusion : Non seulement la connexion Internet fonctionne (comme vu avec le ping sur 8.8.8.8), mais en plus, le service de résolution de noms (DNS) est opérationnel. La machine peut donc naviguer sur le web en utilisant des noms de domaine.




