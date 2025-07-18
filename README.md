# corso-database-oracle


Academy Oracle database


## Let's jump in !! 




### Link e Materiale di riferimento  

https://www.docker.com/



**comando docker per vederere i container attivi**

```
docker ps

```

**comando docker per stoppare un container**

```
docker stop NOME_DEL_CONTAINER_DA_FERMARE

```


**INSTALLARE ORACLE DATABASE SU WIN/MAC/LINUX**
```
 docker run -d -p 1521:1521 -e ORACLE_PASSWORD=wow123456 gvenzl/oracle-free
```


https://www.oracle.com/it/database/sqldeveloper/technologies/download/

<img width="1502" height="870" alt="Screenshot 2025-07-15 alle 15 03 49" src="https://github.com/user-attachments/assets/3d9be44f-68df-441a-ae3a-d26f83cdc245" />



NOTA : I NOMI UTENTE IN MAIUSCOLO : 

<img width="1909" height="818" alt="Screenshot 2025-07-15 alle 17 28 25" src="https://github.com/user-attachments/assets/0fafbf16-b9ca-4f80-ab07-8ed75f84715d" />


<img width="1090" height="657" alt="Screenshot 2025-07-15 alle 17 28 31" src="https://github.com/user-attachments/assets/bd377b36-50ac-451a-aff2-f051bff15715" />


<img width="1911" height="774" alt="Screenshot 2025-07-15 alle 17 28 40" src="https://github.com/user-attachments/assets/30ebf739-da11-4954-bb46-fccde0c9f336" />

<img width="1907" height="784" alt="Screenshot 2025-07-15 alle 17 28 47" src="https://github.com/user-attachments/assets/5a1fcd0b-9d8a-4e66-a80c-3809daf82a42" />

---

sql plus :


per accedere con sql plus : 


```
sqlplus MR/wow123456@127.0.0.1:1521/freepdb1
```






