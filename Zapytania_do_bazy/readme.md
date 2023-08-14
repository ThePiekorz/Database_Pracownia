#Przykładowe widoki utworzone na podanych wcześniej danych:

Wyświetla Imię i Nazwisko projektanta dla każdego projektu.

![alt text]()

```
SELECT PROJEKT.ID_projektu, PRACOWNIK.imie, PRACOWNIK.Nazwisko
FROM PROJEKT
INNER JOIN PRACOWNIK ON PROJEKT.pracownik_id_pracownik=PRACOWNIK.ID_pracownik;
```

Wyświetla ilość obsługiwanych wykonawców
