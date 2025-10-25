# Množiny

## Ať jsou tady množiny

### Pseudodefinice

**Množinou** rozumíme souhrn určitých a navzájem rozlišitelných objektů existujících v naší mysli. Tyto objekty nazýváme prvky dané množiny. Fakt, že $x$ je prvkem množiny $A$ zapisujeme $x \in A$. V opačném případě píšeme $x \notin A$.

### Příklady

- $P = \{a, b, c, d, e, f\}$
- $B = \{\text{krtek, lama, emu, beruška, lemur, krajta}\}$
- $S = \{x \in P \mid x \text{ je samohláska}\} = \{a, e\}$
- $V = \{x \in B \mid x \text{ snáší vajíčka}\} = \{\text{emu, beruška, krajta}\}$


## Vlastnosti množin

- ### Poznámka

	- Prvky množiny nemají pořadí.

### Poznámka

- Množina je jednoznačně určena svými prvky, nemá žádné další vlastnosti. Dvě množiny se tedy rovnají právě tehdy, když mají stejné prvky: $A = B$, jestliže pro každé $x$ platí $x \in A \Leftrightarrow x \in B$.

### Poznámka

- Množiny mohou být nekonečné (obsahovat nekonečně mnoho prvků).

## Kvantifikátory

- ### Značení

	- $\forall x \in A$ – (pro) každé $x$ z množiny $A$,
	- $\exists x \in A$ – existuje $x$ z množiny $A$,
	- $\exists ! x \in A$ – existuje právě jedno $x$ z množiny $A$.

### Definice

- Množinu neobsahující žádný prvek nazýváme **prázdnou množinou** a značíme ji $\emptyset$. Lze ji definovat například takto $\emptyset = \{x \mid x \neq x\}$.



## Příklady na množinové operace, hledáme bublinky

- ### Příklad

	- Mějme množiny $A = \{k, o, s, t, e, l\}$ a $B = \{s, t, á, n, e, k\}$. Určete $A \cap B$, $A \cup B$, $A \setminus B$ a $B \setminus A$.

- ### Příklad

	- Mějme množiny $C = \{k, a, l\}$ a $D = \{v, l, a, k, v, e, d, o, u, c, í\}$. Určete $C'_D$ a $\mathcal{P}(C)$.

## Množinové operace

- Říkáme, že množina $A$ je **podmnožinou** množiny $B$, pokud každý prvek náležející do $A$ leží také v $B$, značíme
  $$A \subseteq B \Leftrightarrow (\forall x)(x \in A \Rightarrow x \in B).$$
- Nechť $A \subseteq B$. Pak **doplňkem** množiny $A$ v množině $B$ je množina
  $$A'_B = \{x \mid x \in B \land x \notin A\}.$$
- $A \cap B = \{x \mid x \in A \land x \in B\}$ – **průnik**
- Množiny, které mají prázdný průnik, nazýváme **disjunktní**.
- $A \cup B = \{x \mid x \in A \lor x \in B\}$ – **sjednocení**
- $A \setminus B = \{x \mid x \in A \land x \notin B\}$ – **rozdíl**
- $\mathcal{P}(A) = \{X \mid X \subseteq A\}$ – **potenční množina** A



## Vennovy diagramy pro tři množiny:
![[Pasted image 20251025153909.png]]

## Vennovy diagramy pro ˇctyˇri mnoˇziny:

![[Pasted image 20251025153924.png]]
# Použití Vennových diagramů

## Příklad

Modelu Octavia se loni vyrobilo stejně ve verzi kombi jako ve verzi sedan (jiná verze se nevyrábí). Klimatizaci mělo 80% Octavií, CD-přehrávač 72%. Kombíky s klimatizací a CD-přehrávačem tvoří pouze pětinu všech vyrobených Octavií, sedany s klimatizací 45% a kombíky bez CD-přehrávače 20% (v obou případech se jedná o procento ze všech vyrobených Octavií). Společnost Škoda nevyrábí sedany s CD-přehrávačem, které by neměly klimatizaci. Určete

- Kolik procent výroby tvoří sedany bez CD-přehrávače a klimatizace.
- Kolik procent sedanů má klimatizaci.
- Kolik Octavií loni společnost Škoda vyrobila?

# Množiny

## Použití Vennových diagramů

### Příklad

Ve třídě 3.B na biologickém gymnáziu v Zelené ulici č. 43 je 30 žáků. Hada i potkana chová sedm žáků, hada i velkého chlupatého pavouka pět žáků, potkana i (velkého chlupatého) pavouka osm žáků. Jedničkářů, čili žáků, kteří doma chovají alespoň dvě zvířata, je ve třídě 14. Čtyři žáci nechovají žádné zvíře, neboť jim to maminka nedovolila. Určete

- Kolik žáků chová hada, potkana i pavouka?
- Kolik žáků chová právě jedno zvíře?
- Kolik žáků chová pouze hada?

## Číselné obory

- $\mathbb{N} = \{0, 1, 2, 3, \ldots\}$ – přirozená čísla,
- $\mathbb{Z} = \{\ldots, -2, -1, 0, 1, 2, 3, \ldots\}$ – celá čísla,
- $\mathbb{Q} = \{q \mid q \text{ lze napsat jako } \frac{a}{b}, a, b \in \mathbb{Z}, b \neq 0\}$ – racionální čísla,
- $\mathbb{R}$ – reálná čísla, čísla odpovídající bodům na číselné ose (přímce),
- $\mathbb{I} = \mathbb{R} \setminus \mathbb{Q}$ – iracionální čísla,
- $\mathbb{C} = \{a + ib \mid a, b \in \mathbb{R}, i^2 = -1\}$ – komplexní čísla.
- $\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$

## Komplexní čísla

- Sečtěte, odečtěte, vynásobte a vydělte komplexní čísla $18 - i$ a $3 + 2i$.
- Určete absolutní hodnotu čísel $-5$, $4 - 3i$, $1 + i$.
- Vyřešte kvadratickou rovnici $x^2 + 6x + 25 = 0$.
- Převeďte do goniometrického tvaru číslo $3\sqrt{3} + 3i$.
- Převeďte do algebraického tvaru číslo $\sqrt{2}(\cos \frac{3\pi}{4} + i \sin \frac{3\pi}{4})$.

# Řešení: Komplexní čísla

---

## 1. Operace s $z_1 = 18 - i$ a $z_2 = 3 + 2i$

- **Sčítání:**
  $z_1 + z_2 = (18 - i) + (3 + 2i) = (18 + 3) + (-1 + 2)i = 21 + i$

- **Odčítání:**
  $z_1 - z_2 = (18 - i) - (3 + 2i) = (18 - 3) + (-1 - 2)i = 15 - 3i$

- **Násobení:**
  $z_1 \cdot z_2 = (18 - i)(3 + 2i) = 54 + 36i - 3i - 2i^2 = 54 + 33i - 2(-1) = 54 + 33i + 2 = 56 + 33i$

- **Dělení:** (Rozšíříme zlomek komplexně sdruženým číslem ke jmenovateli, tj. $3 - 2i$)
  $$
  \frac{z_1}{z_2} = \frac{18 - i}{3 + 2i} = \frac{(18 - i)(3 - 2i)}{(3 + 2i)(3 - 2i)} = \frac{54 - 36i - 3i + 2i^2}{3^2 - (2i)^2} = \frac{54 - 39i - 2}{9 - 4i^2} = \frac{52 - 39i}{9 + 4} = \frac{52 - 39i}{13} = 4 - 3i
  $$

---

## 2. Absolutní hodnota

Absolutní hodnota (velikost) komplexního čísla $z = a + bi$ se vypočítá jako $|z| = \sqrt{a^2 + b^2}$.

- $|-5| = |-5 + 0i| = \sqrt{(-5)^2 + 0^2} = \sqrt{25} = 5$
- $|4 - 3i| = \sqrt{4^2 + (-3)^2} = \sqrt{16 + 9} = \sqrt{25} = 5$
- $|1 + i| = \sqrt{1^2 + 1^2} = \sqrt{2}$

---

## 3. Kvadratická rovnice $x^2 + 6x + 25 = 0$

Řešíme pomocí diskriminantu $D = b^2 - 4ac$.
$a = 1$, $b = 6$, $c = 25$

- **Diskriminant:**
  $D = 6^2 - 4 \cdot 1 \cdot 25 = 36 - 100 = -64$
- **Kořeny:** (Protože $D < 0$, kořeny budou komplexní. $\sqrt{D} = \sqrt{-64} = 8i$)
  $$
  x_{1,2} = \frac{-b \pm \sqrt{D}}{2a} = \frac{-6 \pm 8i}{2}
  $$
- **Výsledek:**
  $x_1 = \frac{-6 + 8i}{2} = -3 + 4i$
  $x_2 = \frac{-6 - 8i}{2} = -3 - 4i$
  
  Množina kořenů: $K = \{-3 + 4i, -3 - 4i\}$

---

## 4. Převod na goniometrický tvar: $z = 3\sqrt{3} + 3i$

Hledáme tvar $z = |z|(\cos \varphi + i \sin \varphi)$.

- **Velikost $|z|$:**
  $|z| = \sqrt{(3\sqrt{3})^2 + 3^2} = \sqrt{(9 \cdot 3) + 9} = \sqrt{27 + 9} = \sqrt{36} = 6$
- **Argument $\varphi$:**
  $\cos \varphi = \frac{a}{|z|} = \frac{3\sqrt{3}}{6} = \frac{\sqrt{3}}{2}$
  $\sin \varphi = \frac{b}{|z|} = \frac{3}{6} = \frac{1}{2}$
- Úhel, pro který platí obě podmínky (nachází se v 1. kvadrantu), je $\varphi = \frac{\pi}{6}$ (nebo $30^\circ$).

- **Výsledek:**
  $z = 6(\cos \frac{\pi}{6} + i \sin \frac{\pi}{6})$

---

## 5. Převod na algebraický tvar: $z = \sqrt{2}(\cos \frac{3\pi}{4} + i \sin \frac{3\pi}{4})$

Hledáme tvar $z = a + bi$ prostým vyčíslením goniometrických funkcí.

- Úhel $\frac{3\pi}{4}$ je ve 2. kvadrantu.
- $\cos(\frac{3\pi}{4}) = -\frac{\sqrt{2}}{2}$
- $\sin(\frac{3\pi}{4}) = \frac{\sqrt{2}}{2}$

- **Dosazení:**
  $z = \sqrt{2} \left( -\frac{\sqrt{2}}{2} + i \frac{\sqrt{2}}{2} \right)$
- **Roznásobení:**
  $z = -\frac{\sqrt{2} \cdot \sqrt{2}}{2} + i \frac{\sqrt{2} \cdot \sqrt{2}}{2}$
  $z = -\frac{2}{2} + i \frac{2}{2}$
- **Výsledek:**
  $z = -1 + i$

