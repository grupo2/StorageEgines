<h2>Activitat 1. REALITZA I/O RESPON ELS SEGÜENTS APARTATS (obligatòria) (1 punts)</h2>

* Indica quins són els motors d’emmagatzematge que pots utilitzar (quins estan actius)? Mostra al comanda utilitzada i el resultat d’aquesta.

  Amb la seguent comanda és pot veure tots el motos, tan el actius, els no activats i els que estan per defecta, en el cas de InnoDB.
  
  ![image](https://user-images.githubusercontent.com/80846119/157502645-00a2b9ec-a37b-48f6-980f-22d277893bef.png)
  <br>
  
* Com puc saber quin és el motor d’emmagatzematge per defecte. Mostra com canviar aquest paràmetre de tal manera que les noves taules que creem a la BD per defecte utilitzin el
  motor MyISAM?
  
  En l'anterior comanda ens donarà el resultat de tots els motors, i és pot obsevar que a la part de <suport> hi ha el motor InnoDB que hi és per defecta.
  
  ![image](https://user-images.githubusercontent.com/80846119/157502968-7ef11269-b809-49c6-b17c-0749f10504ed.png)
  <br>
  
  Per poder canviar aquest paramatre has d'obrir l'arxiu de configuracío "my.cnf" i posar el següent escrit. I has de tornar a reiniciar el servei de mysql.
  
  <br>
  
  Tornar a fer un altre cop la comanda i veuràs els canvis.
  
  <br>
  
* Com podem saber quin és el motor d'emmagatzematge per defecte?
  
  Per saber quin és el motor d'emmagatzematge per defecte, has de fer una de les dos comandes següents:
  
  ![image](https://user-images.githubusercontent.com/80846119/157504853-1694be06-2349-4b61-8c9b-2a70b809d34a.png)

  <br>
  
* Explica els passos per instal·lar i activar l'ENGINE MyRocks. MyRocks és un motor d'emmagatzematge per MySQL basat en RocksDB (SGBD incrustat de tipus clau-valor). Aquest tipus d’emmagatzematge està optimitzat per ser molt eficient en les escriptures amb lectures acceptables.
  
  
  1. Primer haurem d'instal·lar el Percona MyRocks `sudo yum install percona-servidor-rocksdb`.
  
    ![image](https://user-images.githubusercontent.com/80846119/157505660-2cdc0cd3-1e8e-4a8a-b217-758d4c1c66c9.png)
    <br>
  
  2. Després de la instal·lació haurem d'activar el plugin a la nostre base de dades.
     
    ![image](https://user-images.githubusercontent.com/80846119/157506795-ebe2ade0-ea9d-43f5-9117-75b874584059.png)
    <br>
  
  3. Ara només em de tornar a posar la comanda de la priemra part i veurem que ens ha activat un altre engine.
  
    ![image](https://user-images.githubusercontent.com/80846119/157507257-e12449ed-dda9-4991-8b0c-03b780150d8b.png)
    <br>

  
* Importa la BD Sakila com a taules MyISAM. Fes els canvis necessaris per importar la BD Sakila perquè totes les taules siguin de tipus MyISAM.
  
  ![image](https://user-images.githubusercontent.com/80846119/161992323-695c4cc4-9ef7-41f7-b1e6-30d7e8882ac7.png)
  
* Mira quins són els fitxers físics que ha creat, quan ocupen i quines són les seves extensions. Mostra'n una captura de pantalla i indica què conté cada fitxer. Un     cop fet això torna a deixar el motor InnoDB per defecte.
  
  ![image](https://user-images.githubusercontent.com/80846119/161992346-74809161-df5b-4449-83c7-ffe7d2be1384.png)
  
  ![image](https://user-images.githubusercontent.com/80846119/161992356-927958a9-a00e-40da-83de-afbce79744ca.png)

  ![image](https://user-images.githubusercontent.com/80846119/161992373-83c3947e-dd62-41d5-8965-9258cefb4108.png)
  
* Mostra'n una captura de pantalla i indica què conté cada fitxer.

  ![image](https://user-images.githubusercontent.com/80846119/161992441-06de27ed-496b-481c-b720-0d93e3123852.png)

  
* Un cop fet això torna a deixar el motor InnoDB per defecte.
  
  ![image](https://user-images.githubusercontent.com/80846119/161992504-712bbe71-64f6-49e9-97c4-b80457e37ce9.png)

* A partir de MySQL apareixen els schemas de metadades i informació guardats amb InnoDB. Busca informació d'aquests schemas. Indica quin és l'objectiu de cadascun d'ells i posa'n un exemple d'ús.

  Podem consultar les metadades amb la següent comandes.
  
  ![image](https://user-images.githubusercontent.com/80846119/162065139-c22bef72-aeb8-4b64-aa81-562e0ba2b3a3.png)

  Ara explicarem les següents metadades:
  
  `INNODB_SYS_TABLES: Proporciona metadades sobre les taules d'InnoDB, que és equivalent a la informació de la taula SYS_TABLES al diccionari de dades d'InnoDB.

  INNODB_SYS_COLUMNS: Proporciona metadades sobre les columnes de la taula InnoDB, que és equivalent a la informació de la taula SYS_COLUMNS al diccionari de dades InnoDB.

  INNODB_SYS_INDEXES: Proporciona metadades sobre l'índex InnoDB, que és equivalent a la informació a la taula SYS_INDEXES al diccionari de dades InnoDB.

  INNODB_SYS_FIELDS: Proporciona metadades sobre les columnes (camps) clau de l'índex InnoDB, que és equivalent a la informació de la taula SYS_FIELDS al diccionari de dades InnoDB.

  INNODB_SYS_TABLESTATS: Proporciona una vista de la informació d'estat de baix nivell de la taula InnoDB, que deriva de l'estructura de dades en memòria. No hi ha una taula interna del sistema InnoDB corresponent.

  INNODB_SYS_DATAFILES: Informació proporcional de ruta de fitxer de dades per a cada taula i espai de taula general d'InnoDB, que és equivalent a la informació de la taula SYS_DATAFILES al diccionari de dades d'InnoDB.

  INNODB_SYS_TABLESPACES: Informació proporcional sobre InnoDBEspai de taula separadaYEspai de taula generalLes metadades són equivalents a la informació a la taula SYS_TABLESPACES al diccionari de dades InnoDB.

  INNODB_SYS_FOREIGN: Proporciona metadades sobre les claus externes definides a la taula InnoDB, que és equivalent a la informació a la taula SYS_FOREIGN al diccionari de dades InnoDB.

  INNODB_SYS_FOREIGN_COLS: Proporciona metadades sobre columnes de clau externa definides a la taula InnoDB, que és equivalent a la informació de la taula SYS_FOREIGN_COLS al diccionari de dades InnoDB.

  INNODB_SYS_VIRTUALLa taula proporciona metadades sobre la columna virtual produïda per InnoDB i la columna en què es basa la columna virtual produïda, equivalent a la informació de la taula SYS_VIRTUAL al diccionari de dades InnoDB.
`
  
* Posa un exemple que produeix un DEADLOCK i mostra-ho al professor.
  
  Un Deadlock succeeix quan dues o més transaccions intenten fer bloquejos de claus en ordre oposat, per exemple: consulta 1: bloquejar clau(1), bloquejar clau(2);       consulta 2: bloquejar clau(2), bloquejar clau(1);
  
  Sessió 1:
  
  ![image](https://user-images.githubusercontent.com/80846119/161992733-5f2dd5b9-3bd9-46d3-ae22-5686e91a02ba.png)

  Sessió 2:
  
  ![image](https://user-images.githubusercontent.com/80846119/161992761-90bcef8c-f04a-4a5e-b476-1745ca6acea6.png)
  
  Resultat:
  
  ![image](https://user-images.githubusercontent.com/80846119/161992789-d9634e92-b4a4-407e-a4a2-fc0e116cf371.png)


  
  
