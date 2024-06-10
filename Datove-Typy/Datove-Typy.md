# Datové typy v SQL

Datové typy v SQL slouží k definování typu dat, která můžeme ukládat do databáze. Každá hodnota v databázi musí mít určený datový typ. Zde jsou některé z nejběžnějších datových typů v SQL:

## 1. Celá čísla (Integer)

Celá čísla jsou datový typ určený pro ukládání celých čísel, což jsou čísla bez desetinné části. V SQL je tento datový typ obvykle označován jako `INT`.

Příklad:

```sql
CREATE TABLE uzivatele (
    id INT,
    jmeno VARCHAR(50),
    vek INT
);
```

## 2. Čísla s desetinnou částí (Decimal)

Čísla s desetinnou částí jsou datový typ, který umožňuje ukládat čísla s desetinnou částí. V SQL může být tento datový typ označen jako `DECIMAL` nebo `NUMERIC`.

Příklad:

```sql
CREATE TABLE produkty (
    id INT,
    nazev VARCHAR(100),
    cena DECIMAL(10, 2) -- 10 celých čísel, 2 desetinná místa
);
```

## 3. Textové řetězce (Varchar)

Textové řetězce jsou datový typ určený pro ukládání textových hodnot. V SQL je tento datový typ obvykle označován jako `VARCHAR`. Umožňuje ukládat textové hodnoty s proměnnou délkou.

Příklad:

```sql
CREATE TABLE filmy (
    id INT,
    nazev VARCHAR(255),
    reziser VARCHAR(100),
    zanr VARCHAR(50)
);
```

## 4. Datum a čas (Date, Time, Datetime)

Datum a čas jsou datové typy, které umožňují ukládání informací o datech a časech.

- `DATE`: Ukládá pouze datum.
- `TIME`: Ukládá pouze čas.
- `DATETIME` nebo `TIMESTAMP`: Ukládá jak datum, tak čas.

Příklad:

```sql
CREATE TABLE akce (
    id INT,
    nazev VARCHAR(100),
    datum DATE,
    cas TIME
);
```

## 5. Booleovská hodnota (Boolean)

Booleovská hodnota je datový typ, který umožňuje ukládat pouze dvě hodnoty: `TRUE` nebo `FALSE`. V SQL je tento datový typ obvykle označován jako `BOOLEAN`.

Příklad:

```sql
CREATE TABLE uzivatele (
    id INT,
    jmeno VARCHAR(50),
    aktivni BOOLEAN
);
```

## 6. Binární data (Binary)

Binární data jsou datový typ určený pro ukládání binárních souborů, jako jsou obrázky nebo dokumenty. V SQL je tento datový typ obvykle označován jako `BLOB` (Binary Large Object).

Příklad:

```sql
CREATE TABLE soubory (
    id INT,
    nazev VARCHAR(100),
    obsah BLOB
);
```

Toto jsou pouze některé z nejběžnějších datových typů v SQL. Každý databázový systém může mít mírně odlišné pojmenování datových typů nebo může nabízet specifické typy, ale tyto základní typy jsou dostupné ve většině SQL databázových systémů.
