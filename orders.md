# Orders Manager

## Config

**Documents/Kiosk**

```text
--fetchDelay : récupérer les commandes qui viennent d'arriver
--syncDelay : synchronisation timespan
--purgeDelay : 
--outdatedDelay : le client n'a jamais arrivé pour collecter sa commande (1j->3j) 
--Configuration Base (creation, lastModification, lastSave, timezone)
```


## Manager Logic

This text below describes the `order manager logic`.

```text
--Le manager maintient une liste des commandes de la consigne, il ouvre une boucle Run dans laquelle il fait les init
--il charge les commande qui sont sur le serveur (data orders)
--il fait un boucle while jusqu'a ce que le programme s'arrete ou il appelle un fetch ou un fetch delay si fetch not called(fetch delay: toute les 2min il fallait chercher dans le serveur (order incoming ou cancel))
--Quand il y a un changement d'état sur la consigne il synchronize (force syncronize)
```

!> **Ensure lockers** : réservation casier(pas automatiquemet).

