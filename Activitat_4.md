# StorageEgines

*	Crea un tablespace anomenat 'ts1' situat a /discs-mysql/disc1/ i col·loca les taules actor, address i category de la BD Sakila.

  ![image](https://user-images.githubusercontent.com/80846119/161982093-5cb9407f-e9a1-4b13-9ba6-75f169b7d6e5.png)

* Crea un altre tablespace anomenat 'ts2' situat a /discs-mysql/disc2/ i col·loca-hi la resta de taules.

  ![image](https://user-images.githubusercontent.com/80846119/161982147-3021e071-ac94-400f-9000-5ce885c4cdf7.png)
  
  ![image](https://user-images.githubusercontent.com/80846119/161982177-59ec107c-0a15-4387-85b2-4ed64d656148.png)

* Comprova que pots realitzar operacions DML a les taules dels dos tablespaces.
  
  Ara inserirem dades dins de les taules, i després les consultrem, aixins comfirem el seu funcionament correcta.
  
  ![image](https://user-images.githubusercontent.com/80846119/161982400-1c5fa231-8479-4323-a6b6-bca3f3249b7b.png)

  Ara consultarem.
  
  ![image](https://user-images.githubusercontent.com/80846119/161982442-01c3a0a8-cb72-4f67-a2fb-0ff7f65a54a1.png)

  L’anterior era el TS1, ara em de fer el mateix amb el TS2
  
  ![image](https://user-images.githubusercontent.com/80846119/161982479-7ab51c91-d84e-465f-8537-bacbcabb09c8.png)

* Quines comandes i configuracions has realitzat per fer els dos apartats anteriors?
  
  Per fer aquesta activitat he fet el següent:

    1.	Primer em de configurar el nostre arxiu “/etc/my.conf” en el meu cas l’he deixat com a default (amb la ruta de /var/lib/mysql), una vegada que tot estigui configurat, és a dir, haguem creat la ruta de disk 1 i disk 2  i el s Tablespace.

    2.	Segon, haurem de crear els Tablespace, en el meu cas ho he fet amb el Workbench.

    3.	Tercer pas, hem de reconfigurar les taules de sakila perquè en comptes d’anar a la seva ruta default, l’hem d’emagatzemar a la ruta dels nostres Tablespaces.
    4.	Per últim, fem diversos passos per veure el seu funcionament, amb un Insert i un Select.
