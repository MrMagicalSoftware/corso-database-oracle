
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
   
3. Visualizza solo i nomi dei clienti.
4. Visualizza i clienti che vivono in Italia
5. Visualizza i clienti che vivono a Roma.
6. Visualizza i clienti ordinati per nome. (nota mi serve ORDER BY..... CERCARE SU GOOGLE)
7. Visualizza i clienti che NON vivono in Francia. (SIMBOLO DIVERSO !=)
8. Visualizza i clienti che vivono in Italia o in Germania.
9. Visualizza i clienti il cui nome inizia con 'A'. (CERCARE SU GOOGLE LIKE)
10. Visualizza i clienti la cui città termina con 'o'.
11. Visualizza i clienti la cui città contiene esattamente 5 lettere. (CERCARE FUNZIONE LENGTH)
12. Visualizza i clienti che hanno lo stesso nome di città e paese (solo se coincidono).



```
SELECT * FROM Customers;
```
