
# MySQL CRUD Operace: Výukový Materiál

Tento materiál vás provede základními CRUD operacemi (Create, Read, Update, Delete) v MySQL. CRUD operace jsou základní operace, které umožňují manipulaci s daty v databázi.

## Obsah
1. [Připojení k databázi](#1-připojení-k-databázi)
2. [Vytvoření tabulky](#2-vytvoření-tabulky)
3. [Vkládání dat (Create)](#3-vkládání-dat-create)
4. [Čtení dat (Read)](#4-čtení-dat-read)
5. [Aktualizace dat (Update)](#5-aktualizace-dat-update)
6. [Mazání dat (Delete)](#6-mazání-dat-delete)

## 1. Připojení k databázi

Než začneme s operacemi CRUD, musíme se připojit k MySQL databázi. Postup je následující:

1. **Otevření terminálu nebo příkazového řádku:**
   - Na systému Windows můžete otevřít příkazový řádek (Command Prompt) nebo PowerShell.
   - Na systému MacOS nebo Linux můžete otevřít terminál.

2. **Připojení k MySQL serveru:**
   - Zadejte následující příkaz a nahraďte `uživatelské_jméno` svým MySQL uživatelským jménem:
     ```bash
     mysql -u uživatelské_jméno -p
     ```
   - Po zobrazení výzvy zadejte své heslo. Po úspěšném přihlášení se objeví MySQL prompt (`mysql>`).

3. **Výběr databáze:**
   - Po přihlášení můžete vybrat databázi, se kterou chcete pracovat, pomocí příkazu `USE`:
     ```sql
     USE nazev_databaze;
     ```

## 2. Vytvoření tabulky

Než můžeme vložit data do databáze, musíme vytvořit tabulku, která bude obsahovat naše data. Tabulka v databázi je struktura, která ukládá data ve formě řádků a sloupců.

1. **Vytvoření databáze:**
   - Pokud ještě nemáte vytvořenou databázi, můžete ji vytvořit pomocí příkazu:
     ```sql
     CREATE DATABASE firma;
     ```

2. **Výběr databáze:**
   - Použijte databázi `firma`:
     ```sql
     USE firma;
     ```

3. **Vytvoření tabulky:**
   - Vytvořme tabulku `zamestnanci` s následující strukturou:
     - `id`: Primární klíč, automaticky se navyšující
     - `jmeno`: Jméno zaměstnance
     - `prijmeni`: Příjmení zaměstnance
     - `email`: Email zaměstnance
     ```sql
     CREATE TABLE zamestnanci (
         id INT AUTO_INCREMENT PRIMARY KEY,
         jmeno VARCHAR(50),
         prijmeni VARCHAR(50),
         email VARCHAR(100)
     );
     ```

## 3. Vkládání dat (Create)

Pro vložení nových záznamů do tabulky používáme příkaz `INSERT INTO`. Tento příkaz nám umožňuje přidat nové záznamy (řádky) do tabulky.

1. **Vložení jednoho záznamu:**
   - Příklad vložení nového zaměstnance:
     ```sql
     INSERT INTO zamestnanci (jmeno, prijmeni, email) VALUES ('Jan', 'Novak', 'jan.novak@example.com');
     ```

2. **Vložení více záznamů najednou:**
   - Můžeme také vložit více záznamů najednou:
     ```sql
     INSERT INTO zamestnanci (jmeno, prijmeni, email) VALUES 
     ('Petr', 'Svoboda', 'petr.svoboda@example.com'),
     ('Eva', 'Němcová', 'eva.nemcova@example.com');
     ```

## 4. Čtení dat (Read)

Pro čtení dat z tabulky používáme příkaz `SELECT`. Tento příkaz nám umožňuje načíst data z tabulky a zobrazit je.

1. **Načtení všech záznamů:**
   - Načtení všech záznamů z tabulky `zamestnanci`:
     ```sql
     SELECT * FROM zamestnanci;
     ```

2. **Načtení specifických sloupců:**
   - Můžeme specifikovat, které sloupce chceme načíst:
     ```sql
     SELECT jmeno, prijmeni FROM zamestnanci;
     ```

3. **Filtrování dat:**
   - Pomocí klauzule `WHERE` můžeme filtrovat data podle určitých kritérií:
     ```sql
     SELECT * FROM zamestnanci WHERE prijmeni = 'Novak';
     ```

## 5. Aktualizace dat (Update)

Pro aktualizaci existujících záznamů v tabulce používáme příkaz `UPDATE`. Tento příkaz nám umožňuje změnit informace v existujících záznamech.

1. **Aktualizace jednoho záznamu:**
   - Příklad, jak aktualizovat email zaměstnance s `id` 1:
     ```sql
     UPDATE zamestnanci SET email = 'novy.email@example.com' WHERE id = 1;
     ```

2. **Aktualizace více sloupců:**
   - Můžeme aktualizovat více sloupců najednou:
     ```sql
     UPDATE zamestnanci SET jmeno = 'Jan', prijmeni = 'Novak', email = 'jan.novak@novadomena.com' WHERE id = 1;
     ```

## 6. Mazání dat (Delete)

Pro mazání záznamů z tabulky používáme příkaz `DELETE`. Tento příkaz nám umožňuje odstranit určité záznamy z tabulky.

1. **Mazání konkrétního záznamu:**
   - Příklad, jak smazat zaměstnance s `id` 1:
     ```sql
     DELETE FROM zamestnanci WHERE id = 1;
     ```

2. **Mazání všech záznamů:**
   - Pro smazání všech záznamů z tabulky bez jejího odstranění:
     ```sql
     DELETE FROM zamestnanci;
     ```

## Závěr

Tento materiál vás provedl základními CRUD operacemi v MySQL. Znalost těchto operací je klíčová pro efektivní práci s databázemi. Další kroky zahrnují práci s pokročilejšími funkcemi MySQL, jako jsou joiny, indexy a transakce.
