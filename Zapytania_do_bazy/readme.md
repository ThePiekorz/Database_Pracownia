Przykładowe widoki utworzone na podanych wcześniej danych:

Wyświetla Imię i Nazwisko projektanta dla każdego projektu.

![alt text](https://github.com/ThePiekorz/Database_Pracownia/blob/main/Zapytania_do_bazy/Zapytanie1.png)

```
SELECT PROJEKT.ID_projektu, PRACOWNIK.imie, PRACOWNIK.Nazwisko
FROM PROJEKT
INNER JOIN PRACOWNIK ON PROJEKT.pracownik_id_pracownik=PRACOWNIK.ID_pracownik;
```

Wyświetla ilość obsługiwanych wykonawców

![alt text](https://github.com/ThePiekorz/Database_Pracownia/blob/main/Zapytania_do_bazy/Zapytanie2.png)

```
SELECT Dostawca.nazwa_dostawcy, COUNT(WYKONAWCA.dostawca_id_dostawcy) AS
ilosć_dostawców FROM Wykonawca
LEFT JOIN Dostawca ON Wykonawca.dostawca_id_dostawcy = Dostawca.id_dostawcy
GROUP BY nazwa_dostawcy;
```

Wyświetla bilans przychodu dla projektu oraz jego wstępną wycene

![alt text](https://github.com/ThePiekorz/Database_Pracownia/blob/main/Zapytania_do_bazy/Zapytani3.png)

```
create view bilans as
select p.ID_projektu, p.wycena, (f.cena_brutto-f.cena_netto) bilans
from projekt p, faktury f
where p.faktury_id_faktura=f.id_faktura;
SELECT * FROM bilans;
```

Wyświetla pracowników, którzy jednocześnie są przełożonymi.

![alt text](https://github.com/ThePiekorz/Database_Pracownia/blob/main/Zapytania_do_bazy/Zapytanie4.png)

```
select imie, nazwisko from pracownik where pracownik_id_pracownik is null;
```

Wyświetla ilość pracowników zatrudnianych przez daną pracownie.

![alt text](https://github.com/ThePiekorz/Database_Pracownia/blob/main/Zapytania_do_bazy/Zapytanie5.png)

```
SELECT Pracownia.nazwa_prac, COUNT(Pracownik.pracownia_id_pracownii) AS
ilosć_pracowników FROM Pracownik
LEFT JOIN Pracownia ON Pracownik.pracownia_id_pracownii = Pracownia.ID_pracownii
GROUP BY nazwa_prac;
```
