Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically. 

```sql
(SELECT city, CHAR_LENGTH(city) AS length
 FROM station
 ORDER BY CHAR_LENGTH(city) DESC, city DESC
 LIMIT 1)

UNION

(SELECT city, CHAR_LENGTH(city) AS length
 FROM station
 ORDER BY CHAR_LENGTH(city) ASC, city ASC
 LIMIT 1);
```

Selecciona la row de city y la longitud de la row city.

```sql
(SELECT city, CHAR_LENGTH(city) AS length
```

Ordena por longitud y orden alfabético

```
 ORDER BY CHAR_LENGTH(city) ASC, city ASC
```

Limita a 1

```
 LIMIT 1
```
