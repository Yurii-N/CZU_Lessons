### Co je to algoritmus?
- Postup, návod, jak vyřešit nějakou úlohu / problém

### Vlastnosti algoritmů:
- ___Konečnost___ - konečný počet kroků • 
- ___Určitost___ - je přesně specifikováno, co se bude dít (žádné náhodné jevy) 
- ___Korektnost___ - pro platný vstup vrátí správný (a pokaždé stejný) výstup 
- ___Obecnost___ - umí řešit všechny problémy daného “typu”
### Z čeho se algoritmus skládá:
- ___Sekvence___ - příkazy po sobě 
- ___Selekce___ - větvení, podmínky 
- ___Iterace___ - cyklení, opakován
### Způsoby zápisu algoritmů:
- Slovně 
- Vývojové diagramy 
- Strukturogramy 
- Specializované (programovací) jazyky
### Proměnné:
- Je to zástupné jméno pro nějakou zapamatovanou hodnotu, typicky odkaz někam do paměti

### Práce s proměnnými pomocí operátorů:
- **=**  přiřazení 
- == rovnost 
- <> != nerovnost 
- <, >, <=, >= porovnání 
- AND & ∧ logická konjunkce - „a zároveň “ 
- OR || ∨ logická disjunkce - „nebo“ 
- XOR ^ úplná disjunkce, vylučovací nebo - „buď …, anebo …“
- mod modulo: zbytek po dělení -> 7 mod 3 je 1
### Pravdivostní tabulka – Logické AND:
|                 **a**                  |                 **b**                  |              **a AND b**               |
| :------------------------------------: | :------------------------------------: | :------------------------------------: |
| <span style="color:green;">True</span> | <span style="color:green;">True</span> | <span style="color:green;">True</span> |
| <span style="color:green;">True</span> | <span style="color:red;">False</span>  | <span style="color:red;">False</span>  |
| <span style="color:red;">False</span>  | <span style="color:green;">True</span> | <span style="color:red;">False</span>  |
| <span style="color:red;">False</span>  | <span style="color:red;">False</span>  | <span style="color:red;">False</span>  |
### Pravdivostní tabulka – Logické OR:
|                 **a**                  |                 **b**                  |               **a OR b**               |
| :------------------------------------: | :------------------------------------: | :------------------------------------: |
| <span style="color:green;">True</span> | <span style="color:green;">True</span> | <span style="color:green;">True</span> |
| <span style="color:green;">True</span> | <span style="color:red;">False</span>  | <span style="color:green;">True</span> |
| <span style="color:red;">False</span>  | <span style="color:green;">True</span> | <span style="color:green;">True</span> |
| <span style="color:red;">False</span>  | <span style="color:red;">False</span>  | <span style="color:red;">False</span>  |
### Pravdivostní tabulka – Logické XOR:
|                 **a**                  |                 **b**                  |              **a XOR b**               |
| :------------------------------------: | :------------------------------------: | :------------------------------------: |
| <span style="color:green;">True</span> | <span style="color:green;">True</span> | <span style="color:red;">False</span>  |
| <span style="color:green;">True</span> | <span style="color:red;">False</span>  | <span style="color:green;">True</span> |
| <span style="color:red;">False</span>  | <span style="color:green;">True</span> | <span style="color:green;">True</span> |
| <span style="color:red;">False</span>  | <span style="color:red;">False</span>  | <span style="color:red;">False</span>  |
### Typy proměnných:
- Číselné 
- Textové (slova, znaky) 
- Pravdivostní (true, false) 
- … a další
### Výrazy:
- spojení proměnných pomocí operátorů tvoří výraz - de facto jeden příkaz nebo hodnotu, např:
	- ___x = y___ je příkaz, aby se do x nakopírovala hodnota z y 
	- ___x + 3___ je výraz, jehož hodnota je o tři větší, než x
	- ___x = x + 3___ je příkaz, aby se x zvýšilo o tři 
	- ___x > 7___ je výraz, který má hodnotu true nebo false, podle toho jestli je x větší než sedm

___
### Příklad 1:
- Vytvořte algoritmus pro vyřešení zvolené každodenní činnosti. Algoritmus zapište slovně v bodech. Identifikujte, jestli a kde váš algoritmus obsahuje selekci (větvení / podmínky) a iteraci (opakování / cyklení). Pokud neobsahuje, zvažte zda je možné tyto prvky do vašeho algoritmu vhodně zakomponovat, nebo jestli se tyto prvky “neukáží” při zdrobnění algoritmu
	- ## Algoritmus: Příprava čaje
		### Slovní popis algoritmu (v bodech)
		
		1. Připrav si hrnek.
	    
		2. Zkontroluj, jestli je k dispozici čajový sáček.
	    
		    - Pokud **není**, vezmi nový sáček z krabičky.
        
		3. Naplň konvici vodou.
	    
		4. Zapni konvici a **čekej**, dokud se voda neuvaří.
	    
		5. Nalij horkou vodu do hrnku.
	    
		6. Vlož čajový sáček do hrnku.
	    
		7. **Čekej**, dokud se čaj nevylouhuje (např. 3–5 minut).
	    
		8. Vyjmi čajový sáček.
	    
		9. Přidej cukr nebo med, pokud chceš.
	    
		10. Zamíchej.
	    
		11. **Ochutnej čaj** – pokud je příliš horký, **počkáš chvíli**, jinak můžeš pít.
	    
		12. Konec.
### Příklad 2:
- Vytvořte algoritmus, který seřadí tři čísla podle velikosti od nejmenšího po největší. Ověřte, zda funguje správně (tři čísla lze zadat celkem šesti různými způsoby, ověřte všech šest možností). Analyzujte složitost algoritmu (počet porovnání). V případě, že váš algoritmus vyžaduje více jak tři porovnání, pokuste se ho lépe navrhnout / optimalizovat.

```mermaid
flowchart TD
    %% Start všech permutací
    A1((1,2,3)) --> B1[Porovnání a>b? 1>2? Ne] 
    B1 --> C1[a>c? 1>3? Ne] 
    C1 --> D1[b>c? 2>3? Ne] 
    D1 --> E1((Výsledek: 1,2,3))

    A2((1,3,2)) --> B2[Porovnání a>b? 1>3? Ne] 
    B2 --> C2[a>c? 1>2? Ne] 
    C2 --> D2[b>c? 3>2? Ano → Swap b c] 
    D2 --> E2((Výsledek: 1,2,3))

    A3((2,1,3)) --> B3[Porovnání a>b? 2>1? Ano → Swap a b] 
    B3 --> C3[a>c? 1>3? Ne] 
    C3 --> D3[b>c? 2>3? Ne] 
    D3 --> E3((Výsledek: 1,2,3))

    A4((2,3,1)) --> B4[Porovnání a>b? 2>3? Ne] 
    B4 --> C4[a>c? 2>1? Ano → Swap a c] 
    C4 --> D4[b>c? 3>2? Ano → Swap b c] 
    D4 --> E4((Výsledek: 1,2,3))

    A5((3,1,2)) --> B5[Porovnání a>b? 3>1? Ano → Swap a b] 
    B5 --> C5[a>c? 1>2? Ne] 
    C5 --> D5[b>c? 3>2? Ano → Swap b c] 
    D5 --> E5((Výsledek: 1,2,3))

    A6((3,2,1)) --> B6[Porovnání a>b? 3>2? Ano → Swap a b] 
    B6 --> C6[a>c? 2>1? Ano → Swap a c] 
    C6 --> D6[b>c? 3>2? Ano → Swap b c] 
    D6 --> E6((Výsledek: 1,2,3))

```


### Příklad 3:
- Navrhněte algoritmus, který zadanou částku v korunách rozdělí tak, aby byl použit co nejnižší počet bankovek a mincí. Zamyslete se, jestli je možné tento algoritmus navrhnout tak, aby neobsahoval žádné cykly.
```mermaid
flowchart TD
    A[Start: částka v Kč] --> B{Je částka >= 1000?}
    B -- Ano --> C[Odečti 1000, počet 1000 += 1]
    C --> B
    B -- Ne --> D{Je částka >= 500?}
    D -- Ano --> E[Odečti 500, počet 500 += 1]
    E --> D
    D -- Ne --> F{Je částka >= 200?}
    F -- Ano --> G[Odečti 200, počet 200 += 1]
    G --> F
    F -- Ne --> H{Je částka >= 100?}
    H -- Ano --> I[Odečti 100, počet 100 += 1]
    I --> H
    H -- Ne --> J{Je částka >= 50?}
    J -- Ano --> K[Odečti 50, počet 50 += 1]
    K --> J
    J -- Ne --> L{Je částka >= 20?}
    L -- Ano --> M[Odečti 20, počet 20 += 1]
    M --> L
    L -- Ne --> N{Je částka >= 10?}
    N -- Ano --> O[Odečti 10, počet 10 += 1]
    O --> N
    N -- Ne --> P{Je částka >= 5?}
    P -- Ano --> Q[Odečti 5, počet 5 += 1]
    Q --> P
    P -- Ne --> R{Je částka >= 2?}
    R -- Ano --> S[Odečti 2, počet 2 += 1]
    S --> R
    R -- Ne --> T{Je částka >= 1?}
    T -- Ano --> U[Odečti 1, počet 1 += 1]
    U --> T
    T -- Ne --> V[Výsledek: rozděleno na minimum kusů]

```


### Příklad 4:
- Navrhněte algoritmus, který ze zadané řady čísel najde a vypíše to nejmenší číslo. Algoritmus zapište nejprve slovně, pak zakreslete pomocí vývojového diagramu

```mermaid
flowchart TD
    A[Start: zadaná řada čísel] --> B[Inicializuj min = první číslo]
    B --> C{Je další číslo v řadě?}
    C -- Ano --> D[Porovnej číslo s min]
    D --> E{Je číslo < min?}
    E -- Ano --> F[min = číslo]
    E -- Ne --> G[Pokračuj]
    F --> G
    G --> C
    C -- Ne --> H[Vypiš min]
    H --> I[End]

```
### Příklad 5:
- Vytvořte a pomocí vývojového diagramu zakreslete algoritmus, který pro zadané číslo zjistí, jestli se jedná o prvočíslo nebo nikoliv. Ve vývojového diagramu využijte zápisu operací pomocí vhodně navržených proměnných.

```mermaid
flowchart TD
    A[Start: zadej číslo n] --> B{Je n menší než 2?}
    B -- Ano --> C[Není prvočíslo] --> I[End]
    B -- Ne --> D[i = 2]
    D --> E{i*i <= n?}
    E -- Ano --> F{n modulo i = 0?}
    F -- Ano --> G[Není prvočíslo] --> I
    F -- Ne --> H[i = i + 1] --> E
    E -- Ne --> J[Je prvočíslo] --> I

```
