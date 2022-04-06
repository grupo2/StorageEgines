# StorageEgines


*	Com podem comprovar (Innodb Log Checkpointing)
*	LSN (Log Sequence Number)
*	L'últim LSN actualitzat a disc
*	Quin és l'últim LSN que se li ha fet Checkpoint
	
	![image](https://user-images.githubusercontent.com/80846119/161988422-3ec179cf-912d-4e68-af32-05f75be3e9bb.png)	
	
	En la següent captura és pot observar els LOGS.
	
	![image](https://user-images.githubusercontent.com/80846119/161988561-ab908022-4aa0-4908-bc25-d37916fd1d01.png)

*	Proposa un exemple a on es vegi l'ús del redolog
	
El RedoLog és una estructura de dades que s'utilitza a l'hora de la recuperació de falles per a corregir per dades que han estat escrites per transaccions incompletes. Es pot posar el cas que hi ha hagut un apagat inesperat, aleshores el `Redolog` es posa en acció, és a dir, totes les modificacions que no han estat completades, es reprodueixen automaticament durant la inicialització del nostre servei.
	
*	Com podem mirar el número de pàgines modificades (dirty pages)? I el número total de pàgines?
	
	Es pot observar de la mateixa manera que abans, obrint l'arxiu LOG.
	
	![image](https://user-images.githubusercontent.com/80846119/162068602-991512ec-9952-42d8-bd97-8e8f27ceaa9b.png)

	
