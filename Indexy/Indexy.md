# Indexy v SQL

Indexy v SQL jsou struktury, které zrychlují vyhledávání a dotazy v databázi. Indexy vytvářejí se na jednom nebo více sloupcích tabulky a databázový systém je používá k rychlému nalezení záznamů. Zde je několik důležitých bodů o indexech v SQL:

## 1. Typy indexů

### Jednoduchý index

Jednoduchý index se vytváří na jednom sloupci tabulky.

```sql
CREATE INDEX nazev_indexu ON tabulka(sloupec);
```

### Složený index

Složený index se vytváří na více sloupcích tabulky.

```sql
CREATE INDEX nazev_indexu ON tabulka(sloupec1, sloupec2);
```

## 2. Výhody indexů

- **Rychlejší vyhledávání**: Indexy umožňují databázovému systému rychle najít záznamy pomocí vyhledávacích dotazů.
- **Optimalizace dotazů**: Indexy mohou zlepšit výkon dotazů, což znamená rychlejší vykonání SQL dotazů.
- **Unikátní hodnoty**: Indexy mohou zajistit, že hodnoty ve sloupci jsou unikátní, což je užitečné pro primární klíče a unikátní omezení.

## 3. Nevýhody indexů

- **Větší velikost**: Indexy mohou zvětšit velikost databáze, protože ukládají dodatečné informace o položkách v tabulce.
- **Zpomalení zápisu**: Při vkládání, aktualizaci nebo mazání dat může být zápis pomalejší kvůli aktualizaci indexů.
- **Náročnější údržba**: Indexy vyžadují pravidelnou údržbu a aktualizace, aby zůstaly efektivní.

## 4. Kdy použít indexy

- **Vyhledávání podle sloupce**: Použij indexy na sloupce, podle kterých často vyhledáváš nebo řadíš výsledky dotazů.
- **Tabulky s velkým objemem dat**: Indexy jsou obzvláště užitečné v tabulkách s velkým počtem záznamů, kde by vyhledávání mohlo být pomalé bez indexů.

Indexy jsou důležitou součástí návrhu a optimalizace databáze v SQL. Správné používání indexů může výrazně zlepšit výkon dotazů a celkovou efektivitu databáze.
