# StorageEgines

## Activitat 8. Storage Engine MyRocks (1 punt)

* Documenta i posa exemple de com utilitzar ENGINE MyRocks. Crea una Base de dades amb 2 o 3 taules i inserta-hi contingut.

  ![image](https://user-images.githubusercontent.com/80846119/161984557-3cf92c95-c67f-4fed-ae57-57ff13fba2a1.png)
  
  En el meu cas he creat una base de dades amb 3 taules cadascuna amb contingut. Per fer servir l’engine ROCKSDB, només l’has d’inserir al final de la creació de cada taula.
  
* A quin directori es guarden els fitxers de dades? Fes un llistat de a on són els fitxers i què ocupen.

  ![image](https://user-images.githubusercontent.com/80846119/161984695-e4586aca-9976-447e-9a56-05ba62d3d4ee.png)

  L'arxiu hi estarà encriptat, però amb aquesta comanda és pot llegir.
  
  ![image](https://user-images.githubusercontent.com/80846119/161984777-8012768a-cf16-4a2c-8ed3-1d48e2579a38.png)

  En l’anterior captura es pot veure a on s’han emmagatzemat les dades de les taules.
  
* Quina és la compressió per defecte que utilitza per les taules? Com ho faries per canviar-lo. Per exemple utilitza Zlib o ZSTD o sense compressió.

  La compressió que ve per defecte és kLZ4Compression.
  
  ![image](https://user-images.githubusercontent.com/80846119/161985025-0e0a4417-9e76-4d61-a3cc-2e1116780834.png)

  Per poder canviar-lo has de fer la següent comanda dins de l’arxiu `/etc/my.cnf`.
  
  ![image](https://user-images.githubusercontent.com/80846119/161985145-703de284-3974-4d44-ad4e-1b1c185ece19.png)

  Reiniciem el sistema i fem un altre cop la comanda per veure amb que ho comprimeix.
  
