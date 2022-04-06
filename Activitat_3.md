# StorageEgines
* Partint de l'esquema anterior configura el Percona Server perquè cada taula generi el seu propi tablespace en una carpeta anomenada tspaces (aquesta pot estar situada a on vulgueu).

*	Indica quins són els canvis de configuració que has realitzat.

  Per fer aquest exercici em de fer el següent:
  
  1. Primer activarem l’opció de innodb_file_per_table.
  
     ![image](https://user-images.githubusercontent.com/80846119/161980945-d4563901-a7de-49e9-be9e-7b4bd726dd87.png)
  
  2. I reiniciem el servei i comprovem el seu funcionament.
    
    ![image](https://user-images.githubusercontent.com/80846119/161981013-0139eb97-9e75-4975-851b-9c685ca652e0.png)
    
    ![image](https://user-images.githubusercontent.com/80846119/161981096-c5a53d37-54ba-4596-90c3-b1e419daed4f.png)

  3. Crearem la carpeta anomenada ‘tspaces’ i la situarem a l’arrel de la nostre maquina. Per fer tot això farem gairebé el mateix procediment que abans.

    ![image](https://user-images.githubusercontent.com/80846119/161981201-058eda71-3b53-495b-865a-b504fdf27eb7.png)
  
  4. Ara copiarem els arxius de “/var/lib/mysql/*” a “/tspaces”.
    
    ![image](https://user-images.githubusercontent.com/80846119/161981340-d4469792-3a0b-4590-967c-a3a6a80ef178.png)
  
  5. Farem les dues 2 comandes.
  
    ![image](https://user-images.githubusercontent.com/80846119/161981373-73514f65-2e67-4e16-b477-3d7dfa9ce9db.png)

  6. Modificarem l’arxiu “/etc/my.cnf” i editarem les següents línies de codi.

    ![image](https://user-images.githubusercontent.com/80846119/161981504-fbcde9fc-acb8-4dae-813e-8a485134a5dc.png)

  7. I tornem a iniciar el servei de mysql, i verifiquem el `@@DATADIR`.

    ![image](https://user-images.githubusercontent.com/80846119/161981552-bd2e23ba-879b-4365-b70e-7ecda9485ad0.png)

    ![image](https://user-images.githubusercontent.com/80846119/161981579-c6ff33ec-f699-432c-8bbc-c293a44f6f71.png)
