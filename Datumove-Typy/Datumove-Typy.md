# Datumové funkce v SQL

Datumové funkce v SQL umožňují manipulaci s daty a časy uloženými v databázi. Tyto funkce umožňují provádět operace jako je formátování, přidávání a odečítání časových intervalů, zjišťování rozdílů mezi daty a mnoho dalšího. Zde jsou některé z nejběžnějších datumových funkcí v SQL:

## 1. CURRENT_DATE

Funkce `CURRENT_DATE` vrací aktuální datum.

Příklad:

```sql
SELECT CURRENT_DATE;
```

## 2. CURRENT_TIME

Funkce `CURRENT_TIME` vrací aktuální čas.

Příklad:

```sql
SELECT CURRENT_TIME;
```

## 3. CURRENT_TIMESTAMP

Funkce `CURRENT_TIMESTAMP` vrací aktuální datum a čas.

Příklad:

```sql
SELECT CURRENT_TIMESTAMP;
```

## 4. DATE_FORMAT

Funkce `DATE_FORMAT` umožňuje formátovat datum podle zadaného formátu.

Příklad:

```sql
SELECT DATE_FORMAT(datum, '%d.%m.%Y') AS formatovany_datum FROM akce;
```

## 5. DATE_ADD a DATE_SUB

Funkce `DATE_ADD` a `DATE_SUB` umožňují přidávat nebo odebírat časové intervaly k datu.

Příklad:

```sql
SELECT DATE_ADD(datum, INTERVAL 1 DAY) AS novy_datum FROM akce;
```

## 6. DATEDIFF

Funkce `DATEDIFF` vrací rozdíl mezi dvěma daty v počtu dnů.

Příklad:

```sql
SELECT DATEDIFF(datum_konce, datum_zacatku) AS pocet_dni FROM rezervace;
```

Toto jsou pouze některé z nejběžnějších datumových funkcí v SQL. Každý databázový systém může mít mírně odlišné funkce nebo podporovat specifické operace s daty, ale tyto základní funkce jsou dostupné ve většině SQL databázových systémů.
