# TP2 RE16
### Recréer le Data View dans Kibana

```
Dans Kibana → Stack Management → Data Views :

Name : nginx-*

Time field : @timestamp

```

Si Kibana te propose des champs → c’est gagné 🎯

### Observer les logs

👉 Menu → Discover

Data View : nginx-*

Time range (en haut à droite) : Last 15 minutes

Recharge la page DVWA (http://localhost) plusieurs fois

Tu dois voir :

des lignes de logs apparaître

avec des champs comme remote_addr, request, status, etc.

👉 Si tu ne vois rien ici, STOP : un dashboard ne pourra rien afficher.

![alt text](image.png)

### Créer son dashboard

👉 Menu → Visualize Library → Create visualization

```
Choix

Type : Line

Data view : nginx-*

Configuration

X-axis : @timestamp

Y-axis : Count
```

👉 Clique Save

Name : DVWA – Traffic over time

![alt text](image-1.png)