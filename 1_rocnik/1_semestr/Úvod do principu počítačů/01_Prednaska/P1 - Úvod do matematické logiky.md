### Matematická logika:
- Logika:
	- pochází od řeckého slova ___logos___ (slovo, rozum, smysl) → logika je vědecká disciplína o správném uvažování (usuzování)
	- ___Matematická (formální) logika___ neřeší zda předpoklady, z kterých vycházíme, jsou pravdivé, ani zda výsledek uvažování je ve shodě se skutečností, ale pouze __zda závěr vyplývá z daných předpokladů__
- Uplatnění matematické logiky:
	- nutná k ___přesnému matematickému vyjadřování___, k formulaci matematických vět a ke konstrukci jejich důkazů
	- při ___analýze a syntéze (konstrukci) elektronických logických obvodů___, které jsou základními prvky současných počítačů
	- ___při konstrukci rozhodovacích podmínek___ při návrhu softwaru
		- strojový kód procesoru vyhodnocuje podmínky pomocí logických instrukcí

___

### Výrokový počet:
- ___Výrokový počet___ – studium závislosti pravdivostní hodnoty složeného výroku na způsobu spojení a na pravdivostních hodnotách jednotlivých výroků.
- ___Výrok___ – každá oznamovací věta (sdělení), o které lze rozhodnout, zda je pravdivá či nepravdivá výrokem je:
	- Prší. 
	- Svítí sluníčko.
- výrokem není:
	- Kéž by pršelo! 
	- Pro celé číslo x platí, že x > 3.
- Pravdivostní hodnoty: 
	- pravda (true) – značíme 1 nebo t 
	- nepravda (false) – značíme 0 nebo f

---

### Výroky:
- ___Elementární výrok___ (logická nebo výroková ___proměnná___)
	 - základní výrok, jehož struktura se dále nedělí
	 - značíme malými písmeny: a,b,c,…,x,y,z
	 - např.: 
		 - a: Prší. 
		 - b: Vezmu si deštník. 
		 - c: Svítí sluníčko
- ___Složený výrok___ (logická nebo výroková ___formule___)
	- spojení elementárních výroků pomocí závorek a logických spojek
	- značíme velkými písmeny: A,B,C,…,X,Y,Z
	- např.: 
		- X: Prší a nesvítí sluníčko. 
		- Y: Jestliže svítí sluníčko, nevezmu si deštník.

___

### Vybrané logické spojky

| Spojka             | Význam                         | Značka | Příklad                                                                    |
| ------------------ | ------------------------------ | ------ | -------------------------------------------------------------------------- |
| negace             | „není pravda, že“              | ¬      | NenÍ pravda, že prší. (Neprší)                                             |
| konjunkce          | „a (zároveň)“                  | ∧      | Prší a svítí sluníčko.                                                     |
| disjunkce          | „nebo“                         | ∨      | Prší nebo svítí sluníčko.                                                  |
| implikace          | „jestliže ..., pak“            | →, ⇒   | Jestliže prší, vezmu si deštník.                                           |
| ekvivalence        | „právě tehdy, když“            | ↔, ⇔   | Prší právě tehdy, vezmu-li si deštník.                                     |
| nonekvivalence     | „nestejnost; vylučující nebo“  | ⊕      | Buď prší nebo svítí sluníčko.                                              |
| Shefferův operátor | „není pravda, že ... a ...“    | ↑      | NenÍ pravda, že prší a svítí sluníčko. (Neprší nebo nesvítí sluníčko.)     |
| Pierceova šipka    | „není pravda, že ... nebo ...“ | ↓      | NenÍ pravda, že prší nebo svítí sluníčko. (Neprší a ani nesvítí sluníčko.) |

---

### Pravdivostní funkce:
- Pravdivostní funkcí f ( p1 , p2 , . . . pn ) proměnných p1 , p2 , . . . pn rozumíme zobrazení {0,1}^n → {0,1} 
  ___„Pro každou kombinaci ohodnocení n vstupních dvouhodnotových {0,1} proměnných generuje výstupní hodnotu 0 nebo 1“___
- Každá formule generuje určitou pravdivostní funkci
- Pravdivostní funkce se obvykle zapisuje ve formě ___pravdivostní tabulky___

---

### Pravdivostní funkce vybraných logických operací:

- unární spojky → f(a)
	- negace (¬)
- binární spojky → f(a,b)
	- konjunkce (∧), disjunkce (∨), implikace (→, ⇒), ekvivalence (↔, ⇔), nonekvivalence (⊕), Shefferův op. (↑), Piercův op. (↓)

| a | ¬a |
|---|----|
| 0 | 1  |
| 1 | 0  

| a   | b   | a ∧ b | a ∨ b | a → b | a ↔ b | a ⊕ b | a ↑ b | a ↓ b |
| --- | --- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| 0   | 0   | 0     | 0     | 1     | 1     | 0     | 1     | 1     |
| 0   | 1   | 0     | 1     | 1     | 0     | 1     | 1     | 0     |
| 1   | 0   | 0     | 1     | 0     | 0     | 1     | 1     | 0     |
| 1   | 1   | 1     | 1     | 1     | 1     | 0     | 0     | 0     |

---

### Tautologie a kontradikce:
- Tautologie T, 1 generuje f(a,b): 
	- „tautologie (formule T) je pravdivá pro všechna ohodnocení proměnných a a b, tj. vždy nabývá hodnotu 1“
- Kontradikce F, 0 generuje f(a,b): 
	- „kontradikce (formule F) je nepravdivá pro všechna ohodnocení proměnných a a b, tj. vždy nabývá hodnotu 0“

| a | b | T | F |
|---|---|---|---|
| 0 | 0 | 1 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 0 |

---

### Vyhodnocení logické formule:
- ___Vyhodnocením logické formule___ __f__ je myšleno sestavení __pravdivostní tabulky__ popisující pravdivostní funkci generovanou logickou formulí __f__ 
	- Pořadí vyhodnocení je dáno: 
		- směrem od ___vnitřních závorek (formulí) k vnějším__ závorkám (formulím)
		- prioritou logických spojek – ___unární spojky mají vyšší prioritu než binární
- Splnitelnost formule:
	- ___Formule je splnitelná___, jestliže existuje alespoň jedna kombinace ohodnocení vstupních proměnných, pro kterou nabývá pravdivostní funkce hodnoty 1

|  p  |  q  |  r  | ¬q  | p ∨ ¬q | r ∧ q | (p ∨ ¬q) ⇒ (r ∧ q) |
| :-: | :-: | :-: | :-: | :----: | :---: | :----------------: |
|  0  |  0  |  0  |  1  |   1    |   0   |         0          |
|  0  |  0  |  1  |  1  |   1    |   0   |         0          |
|  0  |  1  |  0  |  0  |   0    |   0   |         1          |
|  0  |  1  |  1  |  0  |   0    |   1   |         1          |
|  1  |  0  |  0  |  1  |   1    |   0   |         0          |
|  1  |  0  |  1  |  1  |   1    |   0   |         0          |
|  1  |  1  |  0  |  0  |   1    |   0   |         0          |
|  1  |  1  |  1  |  0  |   1    |   1   |         1          |

---

### Ekvivalence formulí:
- Dvě formule A a B jsou tautologicky ekvivalentní, jestliže generují stejnou pravdivostní funkci: 
	- Značíme A ≡ B
- Dvě formule A a B jsou tautologicky ekvivalentní, právě když formule A ⇔ B je tautologie
- Příklad 
	- Ukažme, že formule A: x ⇒ y je tautologicky ekvivalentní formuli B: ¬x ∨ y
- Příklad tautologické ekvivalence:

| x | y | ¬x | A = (x ⇒ y) | B = (¬x ∨ y) | (A ⇔ B) |
|:-:|:-:|:-:|:-:|:-:|:-:|
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 1 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 0 | 1 |
| 1 | 1 | 0 | 1 | 1 | 1 |

---

### Důležité ekvivalence:

| Ekvivalence                                                                               | Název zákona                     | Poznámka / vysvětlení                    |
| :---------------------------------------------------------------------------------------- | :------------------------------- | :--------------------------------------- |
| ¬¬a ≡ a                                                                                   | zákon dvojí negace               | dvojnásobná negace vrací původní hodnotu |
| a ∨ ¬a = 1  <br> a ∧ ¬a = 0                                                               | zákony o vyloučeném třetím       | „buď a, nebo ne-a“                       |
| a ∨ 0 ≡ a  <br> a ∧ 1 ≡ a                                                                 | zákon neutrality nuly a jedničky | 0 a 1 jsou neutrální prvky               |
| a ∧ 0 = 0  <br> a ∨ 1 = 1                                                                 | zákon agresivity nuly a jedničky | 0 „vynuluje“, 1 „zapne“                  |
| a ∨ a ≡ a  <br> a ∧ a ≡ a                                                                 | zákony o idempotenci prvků       | opakování stejného prvku nic nemění      |
| a ∨ b ≡ b ∨ a  <br> a ∧ b ≡ b ∧ a  <br> a ⊕ b ≡ b ⊕ a                                     | komutativní zákony               | pořadí nehraje roli                      |
| (a ∨ b) ∨ c ≡ a ∨ (b ∨ c)  <br> (a ∧ b) ∧ c ≡ a ∧ (b ∧ c)  <br> (a ⊕ b) ⊕ c ≡ a ⊕ (b ⊕ c) | asociační zákony                 | závorky lze přeskupit                    |
| a ∨ (b ∧ c) ≡ (a ∨ b) ∧ (a ∨ c)  <br> a ∧ (b ∨ c) ≡ (a ∧ b) ∨ (a ∧ c)                     | distributivní zákony             | OR se rozkládá přes AND a naopak         |
| ¬(a ∨ b) ≡ (¬a ∧ ¬b)  <br> ¬(a ∧ b) ≡ (¬a ∨ ¬b)                                           | De Morganovy zákony              | negace mění spojku                       |
| a ∨ (a ∧ b) ≡ a  <br> a ∧ (a ∨ b) ≡ a                                                     | zákony o absorpci                | „silnější“ část pohltí slabší            |
| a ∨ (¬a ∧ b) ≡ a ∨ b  <br> a ∧ (¬a ∨ b) ≡ a ∧ b                                           | zákony o absorpci negace         | zjednodušení kombinace s negací          |

### Logický důsledek:
Z výroků P = {v1 , v2 , … , vn } logicky vyplývá výrok d (je logickým důsledkem) P ⇒ d
- právě tehdy, když pro všechna pravdivá ohodnocení všech výroků {v1 , v2 , … , vn } je výrok d také pravdivý
- právě tehdy, když formule:
	- v1 ∧ v2 ∧ … ∧ vn ⇒ d je tautologie
- právě tehdy, když formule:
	- v1 ∧ v2 ∧ … ∧ vn ¬d je kontradikce
- V opačném případě výrok d z výroků v1 , v2 , … , vn logicky nevyplývá


---
## Informace a data v počítači:
### Binární soustava v počítači
Jednotka - bit
- Jednotka informace (i dat): ___bit___ (binary digit) – značení: b 
	- rozhodnutí mezi dvěma alternativami, možné hodnoty jsou
		- ANO (true) 
		- NE (false)
- Bitu odpovídají hodnoty 1 = ANO, 0 = NE v dvojkové (binární) soustavě
	- Téměř všechny současné počítače pracují v binární soustavě
	- Stavy 1 / 0 lze poměrně snadno technicky realizovat – úrovně napětí, směr magnetických oblastí, odraz a pohlcení světla
- Bit je dále nedělitelný
- S vyjádřením nějaké hodnoty v jednotkách bit se nejčastěji setkáme ___při fyzickém přenosu dat___
	- pomocí úrovní napětí na kovovém drátu, intenzity světla, rádiových vln, …), např. přenosových rychlostí v počítačových sítích

# Jednotka – Byte (Bajt)

## Definice
**Byte (bajt)** – značení: **B**

- = **8 bitů** (2⁸ = 256 možných různých stavů)  
- Binárně vyjádřená čísla: **0 – 255**  
- Základní jednotka, s kterou obvykle počítače pracují  
- Používá se jako nejmenší jednotka pro uložení dat v počítači  
  (v paměti, na pevném disku, ...)

![[Pasted image 20251007130943.png]]

### Jednotka – půlbyte (půlbajt):
- Půlbyte – 4 bity (16 možností) 
	- číslice v šestnáctkové (hexadecimální) soustavě) 
	- Byte je pak vyjádřen dvojicí šestnáctkových číslic
		- 0,1,2,3,4,5,6,7,8,9, A=10,B=11,C=12, D=13,E=14,F=15 
		- velmi časté např. při výpisu obsahu paměti počítače




![[Pasted image 20251007130959.png]]


![[Pasted image 20251007131319.png]]Hexadecimální výpis paměti

## Co to je
Hexadecimální výpis (hex dump) je zobrazení dat v souboru nebo paměti v šestnáctkové soustavě.

Každý řádek má:
1. **Offset (adresa)** – pozice v souboru (např. `00000A00`)
2. **Bajty (hex)** – 8–16 bajtů, např. `4D 00 65 00 74 00`
3. **Textová interpretace** – pokus převést bajty na znaky

## Příklad
```text
00000A00: 4D 00 65 00 74 00 6F 00 64 00 69 00 63 00 6B 00   Metodick
```


### Vyšší informatické jednotky:
- Násobky jednotek (předpony z latiny)

| **Předpona** | **Značení** | **Fyzikální jednotky** | **Informatické jednotky** |
|:-------------:|:------------:|:------------------------:|:---------------------------:|
| **kilo-** | k | 10³ = 1 000 | 2¹⁰ = 1 024 |
| **mega-** | M | 10⁶ = 1 000 000 | 2²⁰ = 1 048 576 |
| **giga-** | G | 10⁹ = 1 000 000 000 | 2³⁰ = 1 073 741 824 |
| **tera-** | T | 10¹² = 1 000 000 000 000 | 2⁴⁰ = 1 099 511 627 776 |
| **peta-** | P | 10¹⁵ = 1 000 000 000 000 000 | 2⁵⁰ = 1 125 899 906 842 624 |

---

