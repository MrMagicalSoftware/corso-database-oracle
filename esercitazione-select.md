
# Query SQL per la gestione dei clienti

## Schema della tabella
| CustomerID | CustomerName | City     | Country |
|------------|--------------|----------|---------|
| INT        | VARCHAR      | VARCHAR  | VARCHAR |

## Query

1. Visualizzare tutti i clienti

```
SELECT * FROM Customers;
```
   
2. Visualizza solo i nomi dei clienti.

```
SELECT CustomerName
FROM Customers;
```




3. Visualizza i clienti che vivono in Italia

```
SELECT *
FROM Customers;
WHERE Country = "Italy";
```


4. Visualizza i clienti che vivono a Roma.

```
SELECT *
FROM Customers
WHERE City = "Rome";
```


5. Visualizza i clienti ordinati per nome. (nota mi serve ORDER BY..... CERCARE SU GOOGLE)
```
SELECT CustomerName
FROM Customers
ORDER BY CustomerName ASC;
```

6. Visualizza i clienti che NON vivono in Francia. (SIMBOLO DIVERSO <>)

```
SELECT CustomerName
FROM Customers
WHERE Country <> "France"
```




7. Visualizza i clienti che vivono in Italia o in Germania.


```
SELECT CustomerName
FROM Customers
WHERE Country = "Italy" or Country ="Germany" ; 
```



8. Visualizza i clienti il cui nome inizia con 'A'. (CERCARE SU GOOGLE LIKE)

```
SELECT CustomerName
FROM Customers
WHERE CustomerName like "A%" ; 
```


9. Visualizza i clienti la cui città termina con 'o'.

```
SELECT CustomerName
FROM Customers
WHERE CustomerName like "%o" ; 
```




10. Visualizza i clienti la cui città contiene esattamente 5 lettere. (CERCARE FUNZIONE LENGTH)


```
SELECT *
FROM Customers
WHERE LEN(City) = 5 ; 
```


11. Visualizza i clienti che hanno lo stesso nome di città e paese (solo se coincidono).


```
SELECT *
FROM Customers
WHERE City = Country 
```
