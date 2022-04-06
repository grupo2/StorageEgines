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

* Posa un exemple que produeix un DEADLOCK i mostra-ho al professor.
  
  Un Deadlock succeeix quan dues o més transaccions intenten fer bloquejos de claus en ordre oposat, per exemple: consulta 1: bloquejar clau(1), bloquejar clau(2);       consulta 2: bloquejar clau(2), bloquejar clau(1);
  
  Sessió 1:
  
  ![image](https://user-images.githubusercontent.com/80846119/161992733-5f2dd5b9-3bd9-46d3-ae22-5686e91a02ba.png)

  Sessió 2:
  
  ![image](https://user-images.githubusercontent.com/80846119/161992761-90bcef8c-f04a-4a5e-b476-1745ca6acea6.png)
  
  Resultat:
  
  ![image](https://user-images.githubusercontent.com/80846119/161992789-d9634e92-b4a4-407e-a4a2-fc0e116cf371.png)


  
  
