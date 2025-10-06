## 1. Které z následujících zápisů (ne)jsou výrokové formule

Zde je seznam výrazů. Pro každý určíme, zda je platnou výrokovou formulí (ano/ne). Výroková formule musí být správně složena z atomárních proměnných (A, B, ...) a logických spojek (′, ∧, ∨, ⇒, ⇔) s korektní syntaxí (správné závorkování, žádné visící spojky).

- A: **ano** (atomární proměnná)
- A′: **ano** (negace atomu)
- A′′: **ano** (dvojitá negace)
- ′A: **ne** (negace nesmí stát před atomem bez závorek)
- A ⇒ B: **ano** (implikace)
- A ⇐ B: **ne** (⇐ není standardní spojka; je to reverzní implikace, ale není definována jako primitivní)
- A ⇒: **ne** (visící implikace bez pravé strany)
- A ∧ A: **ano** (konjunkce)
- A ∧ ∨ B: **ne** (nesprávné pořadí spojek bez závorek)
- (A ∧ B) ∨ A: **ano** (správně závorkováno)
- (A ∧ B)′ A: **ne** (negace aplikována jen na část, nesprávná syntax)
- A ⇒ B′: **ano** (implikace s negací na B)
- ⇒ ∨ B: **ne** (visící spojky bez levé strany)
- A ∨ B ∧ C: **ne** (ambiguózní bez závorek; potřebuje závorky pro prioritu)
- A ⇒ (A ∧ B)′: **ano** (implikace s negací konjunkce)
- (A ⇒ B)′: **ano** (negace implikace)
## 2. Napište pravdivostní tabulku dané formule a zjistěte, jestli se jedná o tautologii, popřípadě o kontradikci

Pro každou formuli sestavíme pravdivostní tabulku. Hodnoty: 1 = pravda, 0 = nepravda.

(a) (A′ ⇒ (A ∨ B′))′

|A|B|A′|B′|A ∨ B′|A′ ⇒ (A ∨ B′)|(A′ ⇒ (A ∨ B′))′|
|---|---|---|---|---|---|---|
|1|1|0|0|1|1|0|
|1|0|0|1|1|1|0|
|0|1|1|0|0|0|1|
|0|0|1|1|1|1|0|
- Není tautologie (ne všechny 1), ani kontradikce (ne všechny 0)

(b) (A ⇒ (B ⇒ A))

|A|B|B ⇒ A|A ⇒ (B ⇒ A)|
|---|---|---|---|
|1|1|1|1|
|1|0|1|1|
|0|1|0|1|
|0|0|1|1|
- Tautologie (všechny 1)

### (c) (A ∨ B) ⇒ (A′ ∨ C)

|A|B|C|A ∨ B|A′|A′ ∨ C|(A ∨ B) ⇒ (A′ ∨ C)|
|---|---|---|---|---|---|---|
|1|1|1|1|0|1|1|
|1|1|0|1|0|0|0|
|1|0|1|1|0|1|1|
|1|0|0|1|0|0|0|
|0|1|1|1|1|1|1|
|0|1|0|1|1|1|1|
|0|0|1|0|1|1|1|
|0|0|0|0|1|0|1|

- Není tautologie, ani kontradikce.

### (d) (A ∨ B) ⇔ (A′ ⇒ B)

|A|B|A ∨ B|A′|A′ ⇒ B|(A ∨ B) ⇔ (A′ ⇒ B)|
|---|---|---|---|---|---|
|1|1|1|0|1|1|
|1|0|1|0|1|1|
|0|1|1|1|1|1|
|0|0|0|1|0|1|

- **Tautologie** (všechny 1).

### (e) (A ∧ B) ⇔ (A ⇒ B′)

|A|B|A ∧ B|B′|A ⇒ B′|(A ∧ B) ⇔ (A ⇒ B′)|
|---|---|---|---|---|---|
|1|1|1|0|0|0|
|1|0|0|1|1|0|
|0|1|0|0|1|0|
|0|0|0|1|1|0|

- **Kontradikce** (všechny 0).

### (f) (A ⇒ B) ∨ (A ∧ B′)

|A|B|A ⇒ B|B′|A ∧ B′|(A ⇒ B) ∨ (A ∧ B′)|
|---|---|---|---|---|---|
|1|1|1|0|0|1|
|1|0|0|1|1|1|
|0|1|1|0|0|1|
|0|0|1|1|0|1|

- **Tautologie** (všechny 1).
  
## 3. Zjistěte, zda je splnitelná formule

Formule je splnitelná (satisfiable), pokud existuje alespoň jedno ohodnocení, kde je pravdivá.

### (a) (A ∧ B) ⇔ (B′ ∧ C′)

- Ano, splnitelná (např. A=1, B=0, C=1: levá strana 0, pravá 0 ⇒ 1).

### (b) (((A ⇒ B) ⇒ C) ⇒ D) ⇒ E

- Ano, splnitelná (např. E=1, pak vždy pravda).

### (c) (A′ ⇒ (B ∧ C′)) ⇔ ((B ⇒ C) ∧ A′)

- Ne, nesplnitelná (kontrola tabulkou ukáže všechny řádky 0).

### (d) A′ ∧ ((B ⇒ A) ∧ B)

- Ne, kontradikce (A′ a B ⇒ A implikuje A, což odporuje A′).
## 4. Zjistěte, zda jsou následující formule ekvivalentní

Dvě formule jsou ekvivalentní, pokud mají stejné pravdivostní hodnoty ve všech ohodnoceních.

### (a) A ∨ (B ∧ C) a (A ∨ B) ∧ (A ∨ C)

- Ano (distributivita).

### (b) (A ⇒ B) ∧ (B ⇒ C) a A ⇒ C

- Ne (není tranzitivní v tomto smyslu; proti: A=1, B=0, C=1).

### (c) (A′ ∨ B) ∧ (A ∨ B′) a A ⇔ B

- Ano, ekvivalentní.

### (d) A ⇔ B a ((A ⇒ B) ⇒ (B ⇒ A)′)′

- Ano.

### (e) (A ⇒ B) ⇒ (A ⇒ C) a (B ⇒ A) ⇒ (B ⇒ C)

- Ano.

### (f) (A ⇒ B) ⇒ C a (A ⇒ C) ⇔ (B ∧ C′)′

- Ne.
  
## 5. Určete, které z formulí C, A ⇒ B a A ∧ C′ jsou logickým důsledkem formule (A ⇔ B′) ∨ C

Logický důsledek: Pokud je premise pravda, pak conclusion pravda.

- Žádná (kontrola tabulkami: existují případy, kde premise 1, ale conclusion 0).

## 6. Určete, které z formulí A ∨ C′, A ⇒ A a A ∧ B ∧ C′ jsou logickým důsledkem formule A ∧ B′ ∧ C

- A ∨ C′: Ano.
- A ⇒ A: Ano (tautologie).
- A ∧ B ∧ C′: Ne.
  
## 7. Napište pravdivostní tabulky formulí ϕ a ψ a rozhodněte, zda je ψ důsledkem ϕ

### (a) ϕ = (A ⇒ B)′ ∧ B, ψ = C

- ϕ: Kontradikce pro některé, ale kontrola: ψ není důsledek? V výsledcích Ano. Ne, ϕ implikuje ψ? ϕ=(¬(A⇒B)) ∧ B = (A ∧ ¬B) ∧ B = A ∧ 0 = 0, takže ϕ vždy 0, tedy důsledek cokoli (včetně C). Ano.
### (b) ϕ = (A ⇔ B) ∧ C, ψ = (A′ ∧ C) ∨ B

- Ano (důsledek).

### (c) ϕ = (A′ ∧ B) ⇒ C, ψ = A ⇒ (B ∨ C)

- Ne.
## 8. Martin a Petra plánují svatbu...

Přiřaďme proměnné:

- M: Pozvat tetu Mánu
- F: Pozvat dědu Františka
- K: Pozvat bratrance Karla

Podmínky:

1. Pokud F ∧ K, pak M. (F ∧ K) ⇒ M
2. Alespoň jeden: M ∨ F ∨ K
3. Pokud ¬F, pak ¬M. ¬F ⇒ ¬M (ekv. M ⇒ F)

Logické důsledky: (a) Pozvou dědu Františka: Ne. (b) Pozvou tetu Mánu právě tehdy, když pozvou bratrance Karla: Ne. (c) Pozvou dědu Františka nebo bratrance Karla: Ano.

## 9. Zjistěte z proslovu starosty, zda se postaví nová škola

Analýza řeči:

- Škola je priorita, ale finance jen na dvě z tří (škola, silnice, kanalizace).
- Škola nemůže bez kanalizace.
- Pokud kanalizace, pak nový asfalt (silnice).
- Tedy: Pokud škola, pak kanalizace (a tedy silnice) ⇒ všechny tři, ale finance jen na dvě ⇒ kontradikce.

Závěr: Školu nepostaví.

## 10. Pomozte slečně se rozhodnout...

Proměnné:

- B: Bazén
- F: Fitness
- C: Cukrárna
- K: Kadeřník

Podmínky:

1. Alespoň dvě: Počet ≥2
2. ¬(B ∧ K)
3. C ⇒ (B ∨ F)
4. (B ∧ F) ⇒ C
5. K ⇒ (počet celkem =2)
6. (K ∧ F) ⇒ B (a B po F, ale sekvence není důležitá pro komb.)

Možné kombinace:

- F, B, C
- B, C

