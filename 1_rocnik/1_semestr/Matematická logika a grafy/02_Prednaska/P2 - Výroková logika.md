### Převod formule do (úplného) disjunktivního tvaru:
#### Logický důsledek:

- Definice:

	- Říkáme, že formule ψ je důsledkem formule φ, pokud je ψ pravdivá při každém ohodnocení, při kterém je pravdivá formule φ. Tento vztah se značí φ⊨ψ.

- Příklad

- Určete, zda je ψ důsledkem φ:

	- φ=A∨B, ψ=A⇒B
	    
	- φ=A∧A′, ψ=A′⇔B
	    
- Pozorování
	- Jakákoli formule je důsledkem kontradikce, tautologie je důsledkem jakékoli formule.
### Logický důsledek více formulí:
- Definice
	- Říkáme, že formule ψ je důsledkem množiny formulí Γ, pokud je ψ pravdivá při každém ohodnocení, při kterém je pravdivá každá formule z množiny Γ. Tento vztah se značí Γ⊨ψ.

### Dám si moučník?:
- Příklad

	- Polévku nebo hlavní jídlo si určitě dám, ovšem jestliže si dám hlavní jídlo, nedám si rozhodně polévku i moučník.
	- Určete, zda jsou následující věty logickým důsledkem výše uvedeného:
		- Dám si polévku. NENÍ
		    
		- Dám si hlavní jídlo. NENÍ
		    
		- Jestliže si dám hlavní jídlo i moučník, nedám si polévku. JE

### Ekvivalence formulí podruhé:

- Definice:
	- Dvě formule (řekněme φ a ψ) se nazývají ekvivalentní, pokud nabývají stejné pravdivostní hodnoty při všech ohodnoceních (mají stejnou pravdivostní tabulku). Značíme φ≡ψ.
- Fakt:
	- Formule φ a ψ jsou ekvivalentní právě tehdy, když je formule φ⇔ψ tautologií.


### Příklady ekvivalentních formulí:

- **Zákon dvojité negace:** ¬(¬A)≡A
    
- **De Morganova pravidla:**
    
    - ¬(A∨B)≡A′∧B′
        
    - ¬(A∧B)≡A′∨B′
        
- ¬(A⇒B)≡A∧B′
    
- (A⇔B)≡(A∧B)∨(A′∧B′)
    
- **Idempotence:** A∨A≡A,A∧A≡A
    
- **Komutativita:** A∨B≡B∨A,A∧B≡B∧A
    
- **Asociativita:** (A∨B)∨C≡A∨(B∨C)≡A∨B∨C
    
- **Distributivita:** A∧(B∨C)≡(A∧B)∨(A∧C)
    
- A∧A′≡0,A∨A′≡1
    
- A∨1≡1,A∨0≡A
    
- A∧1≡A,A∧0≡0


### Disjunkce konjunkcí, konjunkce disjunkcí:

- Definice
	- Výrokové proměnné a jejich negace se souhrnně nazývají **literály**.

- Definice
	- Formule je v **disjunktivním tvaru** (disjunktivní normální formě – DNF), pokud je disjunkcí konjunkcí literálů.

- Definice
	- Formule je v **úplném disjunktivním tvaru**, pokud je v disjunktivním tvaru a každá konjunkce obsahuje všechny výrokové proměnné nebo jejich negace.

- Definice
	- Formule je v **konjunktivním tvaru** (konjunktivní normální formě – CNF), pokud je konjunkcí disjunkcí literálů.

#### Převeďte do disjunktivního tvaru (DNF)

Disjunktivní normální forma (DNF) je disjunkce (součet) konjunkcí (součinů) literálů.

1. **(A′∧(B′∨A))**
    
    - Použijeme distributivní zákon: (A′∧B′)∨(A′∧A)
        
    - Člen (A′∧A) je vždy nepravdivý (kontradikce), takže je ekvivalentní 0.
        
    - (A′∧B′)∨0
        
    - **Výsledek:** A′∧B′
        
2. **(A′⇒(B∧C′))′**
    
    - Nejprve odstraníme implikaci (X⇒Y)≡(X′∨Y): ((A′)′∨(B∧C′))′
        
    - Zjednodušíme dvojitou negaci: (A∨(B∧C′))′
        
    - Použijeme De Morganovo pravidlo na celou závorku: A′∧(B∧C′)′
        
    - Znovu použijeme De Morganovo pravidlo: A′∧(B′∨(C′)′)
        
    - Zjednodušíme dvojitou negaci: A′∧(B′∨C)
        
    - Použijeme distributivní zákon pro převedení na DNF: (A′∧B′)∨(A′∧C)
        
    - **Výsledek:** (A′∧B′)∨(A′∧C)
        
3. **A′⇔(B∨C′)**
    
    - Odstraníme ekvivalenci (X⇔Y)≡(X∧Y)∨(X′∧Y′):
        
    - (A′∧(B∨C′))∨((A′)′∧(B∨C′)′)
        
    - Zjednodušíme a použijeme De Morganovo pravidlo: (A′∧(B∨C′))∨(A∧(B′∧C))
        
    - Aplikujeme distributivní zákon na první část: (A′∧B)∨(A′∧C′)
        
    - Spojíme vše dohromady: (A′∧B)∨(A′∧C′)∨(A∧B′∧C)
        
    - **Výsledek:** (A′∧B)∨(A′∧C′)∨(A∧B′∧C)
        

#### Převeďte do konjunktivního tvaru (CNF)

Konjunktivní normální forma (CNF) je konjunkce (součin) disjunkcí (součtů) literálů.

1. **A∨(A′∧B′)′**
    
    - Použijeme De Morganovo pravidlo: A∨((A′)′∨(B′)′)
        
    - Zjednodušíme dvojité negace: A∨(A∨B)
        
    - Díky asociativitě můžeme odstranit závorky: A∨A∨B
        
    - Díky idempotenci (A∨A≡A): A∨B
        
    - **Výsledek:** A∨B
        
2. **(A′⇒(B∧C′))′**
    
    - Z řešení DNF víme, že zjednodušený tvar je A′∧(B′∨C).
        
    - Tento tvar je již konjunkcí literálu A′ a disjunkce (B′∨C), takže je již v CNF.
        
    - **Výsledek:** A′∧(B′∨C)
        
3. **A′⇔B**
    
    - Odstraníme ekvivalenci (X⇔Y)≡(X⇒Y)∧(Y⇒X): (A′⇒B)∧(B⇒A′)
        
    - Odstraníme implikace: ((A′)′∨B)∧(B′∨A′)
        
    - Zjednodušíme dvojitou negaci: (A∨B)∧(B′∨A′)
        
    - **Výsledek:** (A∨B)∧(A′∨B′)


#### Převeďte do úplného disjunktivního tvaru (ÚDNF)

V Úplné DNF každá konjunkce obsahuje všechny proměnné (buď v normální, nebo negované podobě).

1. **A∨(A′∧B)**
    
    - Proměnné jsou A, B.
        
    - Člen `A` neobsahuje `B`, takže jej rozšíříme: A∧(B∨B′)≡(A∧B)∨(A∧B′).
        
    - Člen `A' ∧ B` již obsahuje obě proměnné.
        
    - Spojíme a seřadíme: (A∧B)∨(A∧B′)∨(A′∧B)
        
    - **Výsledek:** (A∧B)∨(A∧B′)∨(A′∧B)
        
2. **(A∧B)∨(B∧C′)**
    
    - Proměnné jsou A, B, C.
        
    - Člen `A ∧ B` rozšíříme o `C`: (A∧B)∧(C∨C′)≡(A∧B∧C)∨(A∧B∧C′).
        
    - Člen `B ∧ C'` rozšíříme o `A`: (B∧C′)∧(A∨A′)≡(A∧B∧C′)∨(A′∧B∧C′).
        
    - Spojíme vše a odstraníme duplicity (člen (A∧B∧C′) je tam dvakrát).
        
    - **Výsledek:** (A∧B∧C)∨(A∧B∧C′)∨(A′∧B∧C′)
        
3. **(A′⇒B′)∨(B∧C′)**
    
    - Nejprve zjednodušíme: (A∨B′)∨(B∧C′)≡A∨B′∨(B∧C′).
        
    - Rozšíříme každý člen tak, aby obsahoval všechny proměnné (A, B, C).
        
    - `A` → (A∧B∧C)∨(A∧B∧C′)∨(A∧B′∧C)∨(A∧B′∧C′)
        
    - `B'` → (A∧B′∧C)∨(A∧B′∧C′)∨(A′∧B′∧C)∨(A′∧B′∧C′)
        
    - `B ∧ C'` → (A∧B∧C′)∨(A′∧B∧C′)
        
    - Nyní spojíme všechny tyto mintermy a odstraníme duplicity.
        
    - **Výsledek:** (A∧B∧C)∨(A∧B∧C′)∨(A∧B′∧C)∨(A∧B′∧C′)∨(A′∧B′∧C)∨(A′∧B′∧C′)∨(A′∧B∧C′)
        

#### Napište formuli φ podle pravdivostní tabulky

| A   | B   | φ   |
| --- | --- | --- |
| 1   | 1   | 1   |
| 1   | 0   | 1   |
| 0   | 1   | 0   |
| 0   | 0   | 1   |
B ⇒ A


### Úloha: Napište formuli φ s následující pravdivostní tabulkou

Pro vytvoření formule použijeme metodu **úplné disjunktivní normální formy (ÚDNF)**. To znamená, že najdeme všechny řádky, kde je výsledek φ roven **1**, a pro každý z nich vytvoříme logický součin (minterm). Výsledná formule pak bude součtem těchto mintermů.

#### 1. Zadaná tabulka:

|A|B|C|φ|
|---|---|---|---|
|1|1|1|0|
|1|1|0|**1**|
|1|0|1|**1**|
|1|0|0|0|
|0|1|1|**1**|
|0|1|0|0|
|0|0|1|0|
|0|0|0|**1**|

Exportovat do Tabulek

#### 2. Identifikace řádků s výsledkem 1:

Výsledek je **1** ve čtyřech řádcích:

- Řádek 2: A=1,B=1,C=0
    
- Řádek 3: A=1,B=0,C=1
    
- Řádek 5: A=0,B=1,C=1
    
- Řádek 8: A=0,B=0,C=0
    

#### 3. Vytvoření mintermů:

Pro každý z těchto řádků vytvoříme konjunkci (AND), kde proměnnou s hodnotou 0 nahradíme její negací:

- Pro řádek 2 (1,1,0): (A∧B∧C′)
    
- Pro řádek 3 (1,0,1): (A∧B′∧C)
    
- Pro řádek 5 (0,1,1): (A′∧B∧C)
    
- Pro řádek 8 (0,0,0): (A′∧B′∧C′)
    

#### 4. Výsledná formule:

Spojíme všechny mintermy pomocí disjunkce (OR):

**φ≡(A∧B∧C′)∨(A∧B′∧C)∨(A′∧B∧C)∨(A′∧B′∧C′)**

Toto je hledaná formule v úplném disjunktivním tvaru.