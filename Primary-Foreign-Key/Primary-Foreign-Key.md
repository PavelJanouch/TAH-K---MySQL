### Primární klíč (Primary Key)

Primární klíč je unikátní identifikátor každého záznamu v tabulce. Používá se k jednoznačné identifikaci řádků v tabulce a zajistí, že každý řádek má unikátní hodnotu. Typicky se jedná o sloupec s jedinečnými hodnotami.

**Příklad:**
V tabulce zaměstnanců by mohl být sloupec "ID" primárním klíčem, kde každý zaměstnanec má jedinečné číslo ID.

### Cizí klíč (Foreign Key)

Cizí klíč je sloupec v tabulce, který odkazuje na primární klíč v jiné tabulce. Používá se k vytvoření vztahu mezi dvěma tabulkami v databázi. Sloupec s cizím klíčem obsahuje hodnoty, které odpovídají hodnotám v primárním klíči jiné tabulky.

**Příklad:**
V tabulce "Objednávky" by mohl být sloupec "CustomerID" cizím klíčem, který odkazuje na primární klíč "ID" v tabulce "Zákazníci". To umožňuje spojit objednávku s konkrétním zákazníkem.

#### Příklad v Markdownu:

```sql
#### Zaměstnanci
| ID | Jméno    | Příjmení | Oddělení |
|----|----------|----------|----------|
| 1  | John     | Doe      | IT       |
| 2  | Jane     | Smith    | Finance  |
| 3  | Bob      | Johnson  | HR       |

#### Objednávky
| OrderID | CustomerID | Produkt  | Množství |
|---------|------------|----------|----------|
| 101     | 1          | Laptop   | 2        |
| 102     | 3          | Mobil    | 1        |
| 103     | 2          | Tiskárna | 1        |
```

V tomto příkladu sloupec "ID" v tabulce "Zaměstnanci" slouží jako primární klíč. Sloupec "CustomerID" v tabulce "Objednávky" je cizím klíčem, který odkazuje na primární klíč v tabulce "Zaměstnanci"
