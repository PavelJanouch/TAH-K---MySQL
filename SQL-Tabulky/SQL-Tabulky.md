# MySQL Základy Tabulek: Výukový Materiál

## Co je tabulka?

Tabulka je základní strukturou v relační databázi, která ukládá data ve formě řádků a sloupců. Každý řádek představuje jeden záznam a každý sloupec představuje jednu vlastnost tohoto záznamu.

### Struktura tabulky

Struktura tabulky se skládá z názvů sloupců a jejich datových typů. Každý sloupec má definovaný datový typ, který určuje, jaký typ dat může obsahovat.

#### Datové typy

- **INT**: Celé číslo, například 1, 10, -5.
- **VARCHAR(n)**: Řetězec s proměnnou délkou, kde n je maximální délka řetězce.
- **DECIMAL(p, s)**: Číslo s pevným počtem desetinných míst, kde p je celkový počet číslic a s je počet desetinných míst.
- **DATE**: Datum, ve formátu 'YYYY-MM-DD'.

#### Ukázka struktury tabulky

```sql
| Jméno   | Příjmení | Věk | Email            |
|---------|----------|-----|------------------|
| John    | Doe      | 30  | john@example.com |
| Jane    | Smith    | 28  | jane@example.com |
| Michael | Johnson  | 35  | michael@example.com |

### Typy tabulek

Existují různé typy tabulek, z nichž každý má své vlastnosti a použití:

#### 1. **Tabulky relační**
- **Standardní tabulka**: Základní tabulka pro ukládání dat, která obsahuje řádky a sloupce.
- **Dočasná tabulka**: Dočasné úložiště dat, které existuje pouze po dobu běhu dotazu nebo relace.
- **Pohled**: Virtuální tabulka, která vytváří pohled na data z jedné nebo více tabulek.

#### 2. **Tabulky specializované**
- **Auditovací tabulka**: Tabulka určená k sledování změn v databázi.
- **Protokolovací tabulka**: Tabulka pro ukládání protokolů o událostech nebo chybách.

#### 3. **Tabulky systémové**
- **Tabulka informačního schématu**: Obsahuje informace o databázových objektech, jako jsou tabulky, sloupce, indexy atd.
- **Tabulka metadat**: Obsahuje metainformace o tabulkách, jako jsou jejich názvy, typy dat a další atributy.

### Klíče v tabulce

- **Primární klíč (PK)**: Jednoznačný identifikátor každého záznamu v tabulce. Používá se pro jednoznačné identifikace řádků.
- **Cizí klíč (FK)**: Klíč, který odkazuje na primární klíč jiné tabulky a vytváří tak vztahy mezi tabulkami.

Tabulky jsou základními stavebními bloky relačních databází a správné pochopení jejich struktury je klíčové pro efektivní práci s databázemi.
