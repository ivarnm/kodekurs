## a) Aritmetiske uttrykk
Skriv følgende matematikk-setninger korrekt i Python:

La $a$ være $2$

La $b$ være $3$

La $c$ være $5a + b$

La $d$ være $a * b + c$

La $e$ være $\frac{-b + 4}{a - 4}$

La $f$ være $5^{a * b + 2}$

La $g$ være $[(a + b) * c - d]$

```python
# Skriv koden din her


print(a) # skal bli 2
print(b) # skal bli 3
print(c) # skal bli 13
print(d) # skal bli 19
print(e) # skal bli -0.5
print(f) # skal bli 390625
print(g) # skal bli 46
```

Hint: bruk parenteser rundt uttrykk for at de skal bli evaluert i ønsket rekkefølge. Eksponent i Python skrives `**` (eks $2^{3}$ skrives `2**3`).


## b) Matematiske funksjoner
Eksempel på den matematiske funksjonen $f(x) = 2x + 3$ i Python:

```python
def f(x): # Definerer funksjonen
    return 2 * x + 3 # Returnerer parameteren x ganget med 2 og plusset med 3

print(f(5)) # skal regne ut 2*5 + 3 og så printe ut svaret
```
**Skriv følgende matematiske funksjoner i Python:**

$f(x) = 2x + 1$

$g(x) = \frac{-4x + 2}{5x + 3}$

$h(x) = x^2 + 2x + 1$

$i(x) = \sqrt(x)$

```python
# Definer funksjonene dine her

print(f(10)) # skal gi 21 
print(g(5)) # skal gi -0.6428571428571429
print(h(3)) # skal gi 16
print(i(4)) # skal gi 2.0
```

## Tutorial: Heltallsdivisjon og modulo
I tillegg til vanlig divisjon (`/`) har Python også heltallsdivisjon som skrives `//` og modulo som skrives med operatoren `%`.

Heltallsdivisjon og modulo minner om måten du lærte divisjon på barneskolen før du hadde lært desimaltall, altså med hele tall og rest.

Tabellen under illustrerer hvordan disse operatorene virker:

**Utrykk i Python**|**Resultat**|**Forklaring**
---|---|---
17 / 5	|3.4	|Vanlig divisjon
17 // 5|	3	|Heltallsdivisjon, gir hvor mange hele ganger nevneren 5 går opp i telleren 17
17 % 5	|2|	Modulo, gir resten av 17 // 5, dvs. de 2 som blir til over
7.75 / 2.5	|3.1|	Vanlig divisjon
7.75 // 2.5	|3.0|	Heltallsdivisjon, gir hvor mange hele ganger nevneren 2.5 går opp i 7.75.<br> Her blir svaret et flyttall (3.0) heller enn heltallet 3, fordi teller og nevner er flyttall.
7.75 % 2.5	|0.25|	Modulo, Resten av 7.75//2.5 er 0.25 fordi 2.5 * 3.0 er 7.5

Heltallsdivisjon og modulo har en rekke nyttige bruksområder i programmering.

Ett eksempel er regning med enheter som aggregeres på andre måter enn det typiske 10, 100, 1000, slik som 60 sekund per minutt, 60 minutt per time, 24 timer per døgn, 7 døgn per uke.

Koden under viser hvordan // og % kan brukes til slike beregninger.

```python
def antall_hele_uker(dager):
    return dager // 7

def antall_uker_dager(dager):
    uker = dager // 7
    dager = dager % 7
    return uker, dager

print(antall_hele_uker(10))
print(antall_uker_dager(15))
```


## c) Bruk av heltallsdivisjon og modulo
Lag tre funksjoner `antall_minutt(sekunder)`, `antall_dogn(timer)` og `antall_timer_minutt(sek)`, som gjør om sekunder til hele minutter, timer til hele døgn og sekunder til timer og minutter.

```python
# Definer funksjonene dine her

print(antall_minutt(120)) # skal gi 2
print(antall_dogn(75)) # skal gi 3
print(antall_timer_minutt(19832)) # skal gi (5, 32)
```

## d) Partall
Denne kan være vanskelig. Prøv selv først, men mye hjelp å få hvis man googler.

Skriv en funksjon `is_even(number)` som returnerer om et heltall er et partall eller ikke ved hjelp av modulo.

```python
# Definer funksjonen din her

print(is_even(3)) # skal gi False
print(is_even(4)) # skal gi True
```
