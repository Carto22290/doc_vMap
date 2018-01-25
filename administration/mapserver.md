# Mode Mapserver

Le mode MapServer permet la publication de flux WMS avec MapServer. 


## Utiliser des mots de passe cryptés dans les mapfile du flux privé (à partir de 2018.01.00)

Pour toute application ouverte à un certain nombre d'utilisateurs, il est utile voir indispensable de crypter les mots de passes situés à l'intérieur des mapfiles générés lors de l'utilisation de flux privés.

Pour faire ceci, Mapserver propose la librairie **msencrypt** qui va crypter le mot de passe pour qu'il ne soit accessible uniquement par Mapserver lui même.

### Générer un fichier la clé de cryptage

Tout type de cryptage nécessite une clé de cryptage, pour cela il faudra lancer la commence ci-dessous qui va générer un fichier contenant cette clé.

```
sudo /var/www/vmap/vas/server/mapserver/bin/msencrypt -keygen /var/www/vmap/vas/ws_data/vm4ms/map/msencrypt/vm4ms_key.txt
```

### Modifier la définition du flux privé

Pour dire à Mapserver d'utiliser la clé de cryptage il faudra indiquer le fichier précédemment généré dans la définition, pour cela écrire la ligne ci-dessous.

```
CONFIG "MS_ENCRYPTION_KEY" "/var/www/vmap/vas/ws_data/vm4ms/map/msencrypt/vm4ms_key.txt"
```

### Modifier les properties du module Mapserver

Pour activer le cryptage des mots de passe par le module Mapserver, il faudra modifier le fichier de properties vmap/vas/rest/conf/properties\_post.inc et mettre la propertie **use_msencrypt** à true
