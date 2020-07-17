# TD_client_serveur

  RAPPORT MINI PROJET


                 SUJET :  CLIENT SERVEUR


                                                      


                                                                                  INTRODUCTION

 L'environnement client–serveur désigne un mode de communication à travers un réseau entre plusieurs programmes : l'un, qualifié de client, envoie des requêtes ; l'autre ou les autres, qualifiés de serveurs, attendent les requêtes des clients et y répondent. Notre but dans ce projet est de faire communiquer un client et un serveur pour le faire nos allons utiliser la programmation en c pour établir cette communication 
Dans ce programme le serveur doit pouvoir répondre au client s’il reçoit une requête 

    1) CHOIX DU MODE DE SERVEUR

Il existe deux type de mode de serveur de serveur TCP/IP et UDP/IP
             Le mode de serveur qui a été realiser dans notre projet est le TCP/IP
             Il est passé par plusieurs étapes 
    2) FONCTIONNEMEMNT ET ETAPES DE REALISATION DU CLIENT/SERVEUR AVC LE MODE TCP/IP
         2-1) FONCTIONNEMEMNT


Le mode TCP (Stream sockets) est solide. Il garantit la transmission des données. Il nécessite l'établissement d'une connexion. Ensuite, les blocs de données peuvent être échangés.

2-2) ETAPES

    • serveur
Etape ou Les opérations à réaliser sont:


Son utilisee les sockets .

Initialisation:


Ouverture d'un socket en mode flux (TCP/IP): socket(AF_INET, SOCK_STREAM, 0)
Configurer l'adresse et le port : bind()
Configurer le nombre d’écoutes : listen()

Dans une boucle:

Accepter une connexion: accept()
Tester la réception : select() [Facultatif]
Recevoir des données: recv()
Émettre des données: send()
Déconnecter : shutdown()

fin:

Fermeture du socket : closesocket()


    • client 


initialisation:

ouverture d'un socket en mode flux (TCP/IP): socket(AF_INET, SOCK_STREAM, 0)
connexion: connect()
            selon la demande
émettre des données: send()
tester la réception : select() [Facultatif]
recevoir des données: recv()
fin
déconnecter : shutdown()
fermeture du socket : closesocket()


    3) CODE DU PROGRAMME

Voir la branche master


## compilation : gcc client.c -o client , gcc server.c -o server

## execution : on lance en premiere le serveur avec ./server
 et apres on lance  le client  ./client

il faut le faire en ouvrant 2 terminales  
des que on met un caractere  chez le client vue que apres son lancement  il va rester en attente 

le serveur vas repondre - le meme caractere 


