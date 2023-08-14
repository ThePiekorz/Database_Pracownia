# Database_Pracownia

Projekt miał na celu stworzenie Bazy Danych dla pracowni projektowej realizującej opracowanie projektów sieci elektroenergetycznych, w celu optymalizacji zarządzania projektami.

## Założenia funkcjonalne:

Baza oparta jest na głównej tabeli PROJEKT która posiada własne podstawowe informacje
dotyczące projektu, takie jak wstępna wycena czy data zamówienia. Dany projekt posiada jednego zleceniodawcę, ale jeden zleceniodawca może być przypisany
do wielu projektów. Projekt posiada wykonawcę, w tym każdy wykonawca posiada swojego dostawcę.

Do projektu jest przypisany również numer faktury, w którym możemy znaleźć informacje
takie jak cena netto/brutto oraz finalne koszta danego projektu.

Do każdego projektu przypisany jest również pracownik, który go wykonuje. Jeden
pracownik, może wykonywać wiele projektów.

## Poniżej model relacyjny
![alt text](https://github.com/ThePiekorz/Database_Pracownia/blob/main/ModelRelacyjny.png)
