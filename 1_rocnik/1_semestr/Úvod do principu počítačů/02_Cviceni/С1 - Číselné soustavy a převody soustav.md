# Číselné soustavy a převody soustav

## Úvod

Počítač musí být schopen:

- zobrazovat čísla,
    
- pamatovat si čísla,
    
- provádět operace s čísly.
    

Čísla mohou být zobrazena v různých **číselných soustavách**.  
Lidé používají **desítkovou (dekadickou)** soustavu, protože má 10 číslic (0–9) – vychází z toho, že člověk má deset prstů.

- Počítače využívají **dvojkovou (binární)** soustavu, protože je jednodušší rozlišovat dva stavy (0/1) než více.

---

##  1.1 Číselná soustava se základem Z

**Definice:**

- **Č** – hodnota čísla v desítkové soustavě
    
- **k** – koeficient (cifra)
    
- **Z** – základ soustavy (např. 2, 8, 10, 16, 60)
    
- **e** – exponent (−m … n)
    

**Cifry podle základu:**

|Soustava|Cifry|
|---|---|
|Z = 2|0, 1|
|Z = 8|0–7|
|Z = 16|0–9, A–F|

**Obecný zápis:**

Cˇ10=knZn+kn−1Zn−1+...+k0Z0+k−1Z−1+...+k−mZ−mČ_{10} = k_nZ^n + k_{n-1}Z^{n-1} + ... + k_0Z^0 + k_{-1}Z^{-1} + ... + k_{-m}Z^{-m}Cˇ10​=kn​Zn+kn−1​Zn−1+...+k0​Z0+k−1​Z−1+...+k−m​Z−m

---

### 1.1.1 Převod z nedekadické do dekadické soustavy

Postup: násobíme jednotlivé cifry příslušnou mocninou základu a sečteme.

**Příklad:**
(1010111,0011)₂ = (87,1875)₁₀  
(1234,56)₁₆ = (4660,333)₁₀  
(5713)₈ = (3019)₁₀

### 1.1.2 Převod z dekadické do nedekadické soustavy

**Postup:**

1. Zjistíme nejvyšší mocninu základu, kterou číslo obsahuje.
    
2. Určíme, kolikrát se tato mocnina vejde do čísla.
    
3. Odečteme a pokračujeme, dokud zbytek ≠ 0.
    

**Příklad:**
(250)₁₀ → (372)₈  
(38)₁₀ → (100110)₂


## 1.2 Dvojková, osmičková a šestnáctková soustava

**Dvojková soustava** je nejvýhodnější pro počítače, ale čísla jsou dlouhá.  
Z tohoto důvodu se používají i **osmičková (oktalová)** a **šestnáctková (hexadecimální)** soustava.

**Výhody:**

- Snadný převod mezi 2, 8 a 16
    
- Převody jsou jednoznačné a konečné
    

---

### 1.2.1 Převod mezi dvojkovou a šestnáctkovou soustavou

|Hex|Bin|Hex|Bin|
|---|---|---|---|
|0|0000|8|1000|
|1|0001|9|1001|
|2|0010|A|1010|
|3|0011|B|1011|
|4|0100|C|1100|
|5|0101|D|1101|
|6|0110|E|1110|
|7|0111|F|1111|

**Postup převodu:**

- Každou hex cifru nahraď 4 binárními bity.
    
- Čtveřice spoj dohromady.
    

**Příklad:**
(1A5)₁₆ → (110100101)₂  
(3E68)₁₆ → (11111001101000)₂

**Opačně (z binární do hex):**

- Rozděl číslo na skupiny po 4 bitech zprava.
    
- Doplň nuly vlevo, pokud chybí.
    
- Každou čtveřici převeď na hex cifru.

**Příklad:**

(111110010100)₂ → (F94)₁₆

### 1.2.2 Převod mezi dvojkovou a osmičkovou soustavou

|Okt|Bin|Okt|Bin|
|---|---|---|---|
|0|000|4|100|
|1|001|5|101|
|2|010|6|110|
|3|011|7|111|

**Příklad:**
(701)₈ → (111000001)₂  
(3764)₈ → (11111110100)₂

**Z binární do osmičkové:**

- Rozděl číslo na trojice zprava, doplň nuly vlevo.
    
- Každou trojici převeď na okt cifru.
    

**Příklad:**
(10 111 001 010)₂ → (2712)₈

### 1.2.3 Převod mezi osmičkovou a šestnáctkovou soustavou

Přímý převod neexistuje — používá se **převod přes dvojkovou soustavu**.

**Příklad:**
(1AC37F)₁₆ → (6541577)₈  
(357231)₈ → (1DE99)₁₆

## 1.3 Desítkové desetinné číslo ve dvojkové soustavě

Desetinné číslo rozdělíme na:

- **celou část** (před čárkou),
    
- **desetinnou část** (za čárkou).
    

---

### 1.3.1 Způsob převodu I

Používají se záporné mocniny základu 2.  
Převádíme celou část i desetinnou zvlášť.

**Příklad:**
(27,125)₁₀ → (11011,001)₂  
(312,686)₁₀ → (100111000,1010...)₂

### 1.3.2 Způsob převodu II

Nepoužívají se záporné mocniny, ale postupné násobení desetinné části.

**Postup:**

1. Desetinnou část násobíme 2.
    
2. Pokud výsledek > 1 → zapisujeme 1 a odečteme 1.
    
3. Pokud < 1 → zapisujeme 0.
    
4. Pokračujeme, dokud nezískáme požadovanou přesnost.
    

**Příklad:**
(0,853)₁₀ → (0,110110...)₂
