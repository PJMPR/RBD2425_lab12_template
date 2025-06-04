# Zadanie laboratoryjne – Projekt JDBC na bazie Chinook

## 🎯 Cel zadania

Celem zadania jest utrwalenie wiedzy z wykładu poprzez praktyczne zastosowanie wzorców projektowych **Repository**, **Builder** i **Unit of Work** do obsługi relacyjnej bazy danych **Chinook** przy użyciu czystego **JDBC**.

---

## 🧩 Opis bazy danych

Baza danych **Chinook** to przykładowa baza dla sklepu muzycznego zawierająca dane o klientach, albumach, utworach, artystach, zamówieniach i pracownikach. Jej struktura obejmuje m.in. tabele:

* `Artist`, `Album`, `Track`, `Genre`, `MediaType`
* `Customer`, `Invoice`, `InvoiceLine`
* `Employee`

Skrypt SQL do utworzenia bazy znajduje się w pliku: `Chinook_MySql_AutoIncrementPKs.sql`

---

## 🧪 Zakres zadania

1. **Importuj bazę danych Chinook** do lokalnej instancji MariaDB.
2. Utwórz projekt Java z użyciem **Mavena** i dołącz sterownik MariaDB w `pom.xml`.
3. Dla wybranych encji z bazy Chinook:

   * Zaimplementuj modele (`model/`)
   * Zdefiniuj interfejsy repozytoriów (`dao/`)
   * Stwórz klasy implementujące repozytoria z wykorzystaniem czystego JDBC
4. Dodaj:

   * Klasę pomocniczą `DBConnection.java`
   * Obsługę transakcji z użyciem wzorca **Unit of Work**
   * Narzędzie do dynamicznego budowania zapytań SQL (`SqlQueryBuilder`)
5. W klasie `Main`:

   * Zaprezentuj operacje na wybranej encji (np. `Customer`, `Invoice`): dodanie, aktualizacja, usunięcie, pobranie
   * Użyj buildera do wygenerowania zapytania `SELECT` z `JOIN` i `GROUP BY`
   * Zastosuj **Unit of Work** do wykonania serii zmian jako jednej transakcji

---

## 💡 Wskazówki

* Zadbaj o czytelny podział klas i pakietów
* Nie używaj Springa ani Hibernate – tylko **czysty JDBC**
* Wzoruj się na dokumentach:

  * `jdbc_repository_mariadb.md`
  * `sql_query_builder.md`
  * `unit_of_work_transaction.md`
* Dodaj do repozytorium plik `README.md` opisujący Twój projekt i sposób uruchomienia

---

## ✅ Kryteria oceny

* [ ] Działający projekt Maven + JDBC
* [ ] Implementacja wzorca Repository (min. 2 encje)
* [ ] Użycie SqlQueryBuilder w co najmniej 1 zapytaniu
* [ ] Zastosowanie Unit of Work w co najmniej 1 transakcji
* [ ] Poprawność działania i czytelność kodu

---

