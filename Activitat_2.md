**Activitat 2**

* Desactiva l’opció que ve per defecte de innodb_file_per_table
  
  Es pot fer de dos maneres, un és configurant l'arxiu `/etc/my.cnf` com és el meu cas, i l'altre manera és fent un `SET GLOBAL innodb_file_per_table=OFF / 0`. Ja que si
  no el desactivem, el servei de mysql ho activa per defecte.
  
  ![image](https://user-images.githubusercontent.com/80846119/161930664-326487bd-7c99-4418-a1d5-b125b379ac5b.png)

* Importa la BD Sakila com a taules InnoDB.
  
  A l'hora d'importar la Base de Dades Sakila, ho fet de manera molt fàcil, he anat al moodle, he copiat el fitxer i amb l'ajut del workbench l'he importada.
  
* Quin/quins són els fitxers de dades? A on es troben i quin és la seva mida?
  
  Quan l’opció de innodb_file_per_table està desactivada, a les hores els arxius de “.ibd” canvien de ruta. En la següent imatge es pot observar la mida de sakila.
  
  ![image](https://user-images.githubusercontent.com/80846119/161931269-8fa0b7e9-2cfd-4731-bb06-6f219532131a.png)
  
* Canvia la configuració del MySQL per:
- Canviar la localització dels fitxers del tablespace de sistema per defecte a /discs-mysql/
- Tinguem dos fitxers corresponents al tablespace de sistema.
-	Tots dos han de tenir la mateixa mida inicial (10MB) 
-	El tablespace ha de créixer de 5MB en 5MB.
-	Situa aquests fitxers (de manera relativa a la localització per defecte) en una nova localització simulant el següent:
-	/discs-mysql/disk1/primer fitxer de dades → simularà un disc dur
-	/discs-mysql/disk2/segon fitxer de dades → simularà un segon disc dur.

Per fer tot el demanat, em de fer el següents passos:

1.  Em d'aturar el servei de mysql.
    
    ![image](https://user-images.githubusercontent.com/80846119/161931596-01a48a77-02da-4fd7-a9e6-6aa6df3107f9.png)
    
2. Segidament, em de crear la ruta arrel dels discos i donarli els repectius permissos a mysql.
   
   ![image](https://user-images.githubusercontent.com/80846119/161931821-4c9ede39-e7a0-4fcc-9f9c-7780a7210371.png)

3. Ara em de copiar tot el qe hi ha a la ruta de `/var/lib/mysql/*` a la nova ruta `/discs-mysql/`.
   
   ![image](https://user-images.githubusercontent.com/80846119/161932066-35cbf66d-b815-44bc-8905-c05884f8cdf3.png)

5. Instalarem els paquets de `policycoreutils-python`.
   
   ![image](https://user-images.githubusercontent.com/80846119/161965556-03ebd812-ac66-499a-8dcd-117606157057.png)
   
   ![image](https://user-images.githubusercontent.com/80846119/161965589-12838944-3f0d-47f9-8ced-dcfbce064554.png)
   
6. Ara amb les credencials d'administrador farem les dues següents comandes.

   ![image](https://user-images.githubusercontent.com/80846119/161965888-b0b61901-7719-4975-85d1-cdb187a4a7c0.png)
   
   ![image](https://user-images.githubusercontent.com/80846119/161965910-f58228b0-7cea-4b8d-acf6-a1c7de3c886f.png)

7. El pas més imporatant, és l'edició de l'arxiu `/etc/my.cnf` on afegirem els següetns atributs.
    
   ![image](https://user-images.githubusercontent.com/80846119/161965942-b82b2583-9220-4ab9-8bbd-6049619d3a1c.png)

8. Una vegada feta l'edició, haurem de reiniciar el servei de mysql.
  
   ![image](https://user-images.githubusercontent.com/80846119/161966024-5e82dfd3-0706-4a7a-abae-7a6553979a66.png)

9. Farem una comprovació, perque és vegi que no hi ha cap trampa.
  
   ![image](https://user-images.githubusercontent.com/80846119/161966132-b976c12a-5c00-471f-a1cd-f2c1a685aa70.png)
    
   ![image](https://user-images.githubusercontent.com/80846119/161966158-fb0cd1b4-8850-471b-9395-9060c0d6ce16.png)

10. Ara anem a veure si ens ha creat els disks demanats.
    
    ![image](https://user-images.githubusercontent.com/80846119/161969427-2cb6ebb0-4629-4dea-8089-9e8455a13597.png)

    ![image](https://user-images.githubusercontent.com/80846119/161969504-42de081b-b6c6-4049-afe3-f96063043385.png)

    ![image](https://user-images.githubusercontent.com/80846119/161969528-4eaad2d6-b057-4b72-9a18-8e4b3d0c348b.png)

    ![image](https://user-images.githubusercontent.com/80846119/161969637-b657c2fa-4acc-4e1b-9616-24d2d62c88c8.png)

    ![image](https://user-images.githubusercontent.com/80846119/161969663-a8655527-2b66-4f21-8651-1e8e9dad2230.png)

    ![image](https://user-images.githubusercontent.com/80846119/161969682-e23bbcdb-70f1-4ecb-a39a-5f638c43074a.png)

    


    




