# Dodawanie projektu Maven w IntelliJ IDEA

Ten krótki przewodnik pokaże Ci, jak dodać nowy projekt Maven do repozytorium przy użyciu IntelliJ IDEA.

---

## 🛠️ Krok po kroku

### 1. Utwórz nowy projekt Maven

1. Otwórz **IntelliJ IDEA**
2. Wybierz **File > New > Project...**
3. Wybierz **Maven** jako typ projektu (Build System)
4. Kliknij **Next**

### 2. Uzupełnij dane projektu

* Name: chinook-lab
* Location: wybierz folder repozytorium git

Kliknij **Create**.

### 3. Struktura projektu

Po utworzeniu zobaczysz strukturę:

```
chinook-lab/
├── pom.xml
└── src/
    ├── main/java
    └── test/java
```

---

## 📦 Dodanie zależności

Otwórz `pom.xml` i dodaj np. sterownik do MariaDB:

```xml
<dependencies>
    <dependency>
        <groupId>org.mariadb.jdbc</groupId>
        <artifactId>mariadb-java-client</artifactId>
        <version>3.3.1</version>
    </dependency>
</dependencies>
```

Po zapisaniu IntelliJ automatycznie pobierze zależności.

---

**Gotowe!** Teraz możesz rozpocząć programowanie z użyciem Mavena. 🧪
