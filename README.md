# Intro til Python

## Først: hva er Python?
- Python er et programmeringsspråk.
- Ligner litt på "vanlige" språk, skal gjøre det lettere for oss å lage programmer.
- Mye mer firkantet, dvs. vi må følge skrivereglene (grammatikken) nøye.

---

## Hvordan programmerer vi, rent praktisk, i Python?
- Vi skriver programmet som ren tekstfil, kalt *kildekode*
- Vi får Python-tolkeren (et program) til å lese kildekoden og utføre den:
   - linje for linje fra toppen.
   - gjør det om til *maskinkode* som datamaskinen utfører (litt forenklet forklart). 

---

## Hvordan ser et program ut?
En vanlig struktur på et program er
- input
- prosessering/beregning
- output

#### Eksempel: Regn ut summen av to tall
```python
# Input, her er de hardkodet
a = 1
b = 2

# Utregning
c = a + b

# Output
print(c)
```

---

## Variabler
En variabel er som en **navnelapp** for å lagre informasjon i minnet. Tenk på det som en boks med et navn, der du kan legge inn noe og hente det senere. 

I programmeringsspråk brukes `=` for å **gi en variabel en verdi**. Dette er altså ikke en sammenligning slik som i matematikken, men en handling som lagrer data i en variabel.

#### Eksempel
```python
name = "Sara"
age = 25

print("Hei, jeg heter", name, "og jeg er", age, "år gammel.")

age = 10
print(age)
age = age + 1
print (age)
age += 2
print(age)

```
Her lager vi to variabler:
- `name` inneholder teksten `"Sara"`
- `age` inneholder tallet `25`

Som vist i eksempelet kan man også gi en variabel en ny verdi, og den nye verdien kan også være utledet fra verdien variabelen allerede har.

### Regler for variabler
1. Navnet må starte med en bokstav eller understrek
1. Ingen mellomrom. Bruk f.eks. understrek (`_`) for å erstatte mellomrom
    - Eks: `minimum_age`
1. Bruk meningsfulle navn. Det gjør det lettere å lese koden din senere
   - Bra: `antall_epler`, `pris_per_kg`
   - Dårlig: `a`, `x123`

---

## Input og output
`print()` skriver i konsollen/terminalen det som står i parentesen. Kan ta flere argumenter samtidig hvis man ønsker. Hvis du tar inn flere argumenter så legger Python automatisk til et mellomrom mellom argumentene når de skrives ut.

```python
text = 'and one'
number = 3

print ("Hei DIPS")
print('One', text, text, 'is', number)
```

`input()` brukes for at brukeren kan taste inn input til programmet når det kjører. Den venter på at brukeren taster inn noe og slår ENTER.

```python
name = input("Hva heter du? ")
print("Hyggelig å møte deg,", name, "!")
print(f"Hyggelig å møte deg, {name}!")
```

---

## Datatyper
I Python, og andre programmeringsspråk, kan data ha forskjellige _typer_. Forskjellige datatyper egner seg for forskjellige bruksområder. For eksempel hvis vi skal lagre alderen til en person, vil det lønne seg å lagre dette i en `int` (heltall). Navnet til samme person, derimot, bør være en `string`. 

Det finnes mange forskjellige datatyper, men de viktigste er:

* **Integer** - et heltall. F.eks. `10`. I Python brukes `int` for en integer.
* **Float** - et flyttall (tall med desimal). F.eks. `10.5`.
* **String** - tekst. F.eks. `"DIPS"`. I Python brukes `str` for en string.
* **Boolean** - sannhetsverdi. Enten `True` eller `False`. I Python brukes `bool` for boolean.
* **List** - en liste med verdier. En liste inneholder variabler/verdier av hvilken som helst datatype. F.eks. `[1, 2, "Er kodekurs gøy?", True]`.


### Integer
Integers er enten et negativt heltall, 0 eller et positivt heltall. Eksempel:

```python
a = -10
b = 0
c = 5
```

Integers følger et sett med regler, akkurat som i matematikken. Vi kan for eksempel addere integers, hvor resultatet også vil være en integer. Det samme gjelder for multiplikasjon. Utfører vi _divisjon_ med to integers derimot, vil resultatet være en `float`. Eksempel:

```python
print(a + b) # Samme som å si -10 + 0
print(b - c) # Samme som 0 - 5
print(a * c) # Samme som -10 * 5
print(b * c) # Samme som 0 * 5
print(a / c) # Samme som -10 : 5
```


### Float
Floats oppfører seg på nesten samme måte som Integers. De består av de rasjonale tallene $\mathbb{Q}$. De skiller seg fra Integers ved at de kan ligge mellom heltall. Eksempel:

```python
d = 1.2
e = -4.2
f = 0.0
```
På samme måte som med heltall kan vi utføre aritmetiske operasjoner på floats: 

```python
print(d + e) # Samme som 1.2 + (-4.2)
print(d - e) # Samme som 1.2 - (-4.2)
print(f * e) # Samme som 0.0 * (4.2)
```


### String
String er en datatype som inneholder tekst. For å lage en streng skriver vi tekst omringet av "fnutter". Vi kan bruke både enkeltfnutter `'Jeg er en streng'`, dobbeltfnutter `"Jeg er en annen streng"` eller trippelfnutter `"""Jeg er enda en streng"""`. Alle tre måtene å skrive strenger på er like riktig, men de har forskjellige bruksområder. Enkelt- og dobbeltfnutter er veldig like. En av forskjellene er at om du bruker enkeltfnutter, kan du ha dobbeltfnutter i teksten uten noe problem, og omvendt ved bruk av dobbeltfnutter. For eksempel `'Ordet "stein" kan være både et navn og et objekt man finner i naturen'` eller `"Ordet 'stein' kan være både et navn og et objekt man finner i naturen"`. Trippelfnutter lager såkalte "multiline"-strenger. Altså kan vi få strenger på flere linjer. Eksempel:

```python
s1 = 'Jeg er en streng med enkeltfnutter'
s2 = "Jeg er en streng med dobbeltfnutter"
s3 = """Jeg er en
multiline streng"""

print(s1)
print(s2)
print(s3)
```

Vi kan ikke gjøre aritmetiske operasjoner på strenger, på samme måte som `int`s og `float`s. Det betyr derimot ikke at vi ikke kan bruke matematiske operatorer på strenger:

```python
s4 = '10' + '15' + '20'
print(s4)
```

`+` operatoren "setter sammen" strenger. Som i eksempelet over setter vi sammen, eller konkatenerer, tre strenger; `'10'`, `'15'` og `'20'`, til én stor streng `'101520'`

```python
s5 = '10' * 3
print(s5)
```

`*` operatoren ganger strengen antall ganger. I eksempelet over ganger vi strengen `'10'` med `3`, og får den resulterende strengen `'101010'` ('10' 3 ganger), ikke `30` som om vi hadde ganget `int`-en `10` med `int`-en `3`. Operatorene `-` og `/` kan vi ikke bruke på strenger.


### Boolean
En `bool` er en sannhetsverdi, enten `True` eller `False`, og er en _veldig_ sentral datatype i programmering. Booleans kan brukes for eksempel til å sjekke om en alder er under eller over 18. 

```python
had_lunch = True
print(f'Jeg har hatt lunsj: {had_lunch}')
```

Booleans blir viktig når vi senere kommer til if-setninger.

### List
Lister er en annen fundamental datatype i Python. Lister er en samling av verdier, enten av andre datatyper, eller av lister selv. For å lage en liste brukes klammeparenteser []. Inne i klammene legger vi verdiene våre, separert med komma.

```python
participants = ["Thomas", "Lalita"]
print(f'Her har du en liste over alle deltakerne: {participants}')
```

På samme måte som strenger kan vi ikke gjøre vanlige matematiske operasjoner på lister. Vi kan derimot gange en liste med et tall, og plusse sammen lister. Oppførselen blir det samme som når vi ganger en streng med et tall, eller plusser sammen to strenger. _Elementene_ i listen blir ikke ganget med tallet, de vil bli duplisert X ganger. _Elementene_ i listene vil heller ikke bli plusset sammen ved bruk av `+`, men den ene listen blir lagt til i den andre listen:

```python
liste_med_tall = [1,2,3,4]
liste_med_tall2 = [5,6,7,8]

liste2 = liste_med_tall + liste_med_tall2
print(liste2)

liste3 = liste_med_tall * 10
print(liste3)
```

---

## Konvertering mellom datatyper
Ofte kommer vi i situasjoner hvor vi har data av en viss type, men vi trenger samme data bare med en annen type. Da må vi konvertere dataene. Noen vanlige konverteringsfunksjoner:

**`int()`** - konverterer til heltall.
- `int('423')` gir 423 (dvs. tekststrengen blir konvertert til et tall). Virker kun hvis tekststrengen faktisk inneholder et heltall.
- `int(5.69)` gir 5 (dvs. for flyttall blir desimaldelen fjernet).

**`float()`** - konverterer til flyttall.
- `float('5.69')` gir 5.69 (tekststre.ng konvertert til tall).
- `float('5')` gir 5.0, dvs. float() virker på tekststrenger enten de inneholder flyttall eller heltall (men ikke på strenger som er noe annet enn tall).
- `float(5)` gir 5.0

**`str()`** - konverterer til tekststreng.
- `str(42)` gir '42'.
- `str(5.69)` gir '5.69'.

```python
alder = '13'
alder_mor = '37'
sum_alder = alder + alder_mor

print(f'Gratulerer, til sammen er dere {sum_alder} år!')

sum_alder = int(alder) + int(alder_mor)
print('Gratulerer, til sammen er dere', sum_alder, 'år!')
```

---

## Funksjoner
- input og print er navn på *funksjoner* i Python, som utfører gitte oppgaver (som navnet tilsier).
- Vi kan *gjenbruke* funksjoner uten å måtte skrive koden på nytt.
- Funksjoner gjør det også lettere å se hva koden gjør.
- Vi *kaller* (utfører) funksjoner ved å skrive navnet, etterfulgt av parenteser.
- Vi "mater" funksjonene ved å angi inputverdier inne i parentesene. Dette kalles for *argumentene* til funksjonen.

Vi kan også lage egne funksjoner. Vi definerer funksjoner ved å begynne å skrive "def" i koden:

```python
def banner():
    print("***************************************")
    print("***************BANNER******************")
    print("***************************************")
    
print("Dette er ikke en del av funksjonen")
```

### Viktige ting å legge merke til:
- *nøkkelordet* **def** signaliserer at vi skal definere en *funksjon*.
- Funksjonsnavnet er **banner**.
- Funksjonsnavnet etterfølges alltid av et parentespar ( ).
- Inne i parentesen står det hva som skal være *input* til funksjonen. Her er det ingen input ennå.
- Python bruker kolon (:) og innrykk av kodelinjene etterpå for å skille ut en *kodeblokk*.
- Funksjonsdefinisjonen slutter der hvor det ikke lenger er innrykk i koden.

### Kall av funksjoner
- Når vi definerer en funksjon, så blir den ikke utført, bare lagret for bruk.
- Vi *kaller* en funksjon ved å bruke funksjonsnavnet med parentes:

```python
  banner()
```

La oss gjøre funksjonen litt mer nyttig. Vi vil kunne sende den teksten den
skal skrive. Da må den ha en *parameter*. Parameteren er et variabelnavn som gjelder bare inne i funksjonen, som lagrer argumentet som sendes til funksjonen når vi kaller den.

```python
def banner_med_input(tekst):
    tekst_lengde = len(tekst) # en funksjon som gir antall tegn i tekst.
    banner_lengde = tekst_lengde + 2*10
    print("*" * banner_lengde)
    print("*" * 10 + tekst + "*" * 10)
    print("*" * banner_lengde)
    
# La oss kalle funksjonen 
banner_med_input("DIPS")
```

Funksjoner kan også returnere data. Her er et eksempel på en funksjons om summerer to tall:

```python
def add(a, b):
  print(f"Adding {a} and {b}...")
  result = a + b
  print("Done adding")
  return result

x1 = 10
x2 = 30
x3 = add(x1, x2)
x4 = add(x1, x3)
print(x3)
print(x4)
```

---

## If-setninger
I mange programmer har vi kodelinjer som skal utføres bare under visse betingelser. F.eks. at en fartsbot bare skal gis dersom farten var for høy, at varme tilført et rom bare skal økes hvis temperaturen for øyeblikket er lavere enn man ønsker, etc.

Den vanligste programmeringsmekanismen for å oppnå slik betinget oppførsel er if-setninger.

Det finnes tre typer if-setninger:
- if
- if-else
- if-elif-(elif-...)-else

Eksempel: 
```python
nice_weather = True
if nice_weather:
    print('Det er fint vær, gå ut!')
else:
    print('Det er ikke fint vært, bli inne du')
    print('Det er uansett mest behagelig')
```

Vi ser her at variabelen `nice_weather` bestemmer hva koden gjør. 
- if-setningen avsluttes med kolon-tegnet :
- De linjene som er rykket inn under if-setningen blir kjørt hvis betingelsen i if-setningen er True.
- Hvis verdien til variabelen er `True` så kjøres kodeblokka som sier at det er fint vær.
- Hvis ikke så kjøres kodeblokka som sier at det er dårlig vær.

Her har vi et eksempel på et program som spør om kvadratroten av 64 og sjekker om du har svart riktig:

```python
print("Hva er kvadratroten til 64?")

hint = input("Trenger du et hint? ")
if hint == "ja":
    print("Kvadratroten til 64 er det tallet som ganget med seg selv, gir 64.")
    print("F.eks. så er kvadratroten til 4 lik 2, fordi 2 ganger 2 er lik 4.")

svar = input("Hva er svaret? ")
if int(svar) == 8:
    print("Korrekt svar!")
else:
    print("Beklager, feil svar. Riktig svar er 8.")
```
I den første if-setningen så sjekker vi om brukeren har svart "ja".
-  == er en sammenligningsoperator. 
- `if hint == "ja"` kan du lese som: er verdien av `hint` "ja"? 
- Hvis verdien til variabelen hint er "ja", så er
   - resultatet av operasjonen lik verdien **True**
   - kodelinjene som printer hintet utføres
- Hvis brukeren svarte noe annet enn "ja", så blir er tekststrengene forskjellige, og
   - resultatet av operasjonen er **False**
   - hintene blir IKKE printet.

I den neste delen av koden har vi en ny if-setning, men også en **else**-del. 
- Her tester vi om brukeren har svart riktig ved å først konvertere svaret til et tall og så sammenligne det med 8.
- Hvis testen er True. så får du beskjed om at du har svart riktig.
- Hvis ikke så kjøres det som står inne i else-blokken.

### Relasjonsoperatorer, boolske uttrykk
- I koden over har vi brukt == til å undersøke om to strenger er like.
- Det resulterer i en av de to boolske verdiene True eller False
- Uttrykk som evalueres til True eller False, kalles for *boolske uttrykk*

**NB! Legg merke til forskjellen mellom**
- =, som vi bruker til å tilordne verdier til variable,
- ==, som sammenligner to objekter, og returnerer True hvis de er like.

Vi har også flere operatorer, som vi kjenner fra matematikk. De gir enten verdien True eller False

| Matematikk | Python | Forklaring       |
|------------|--------|------------------|
| `<`        | `<`    | Mindre enn       |
| `>`        | `>`    | Større enn       |
| `≤`        | `<=`   | Mindre eller lik |
| `≥`        | `>=`   | Større eller lik |
| `=`        | `==`   | Er lik           |
| `≠`        | `!=`   | Er ulik          |


| Betingelse | Verdi  |
|------------|--------|
| `4 < 3`    | False  |
| `4 == 4`   | True   |
| `3 != 3`   | False  |
| `3 >= 3`   | True   |

### Nøstede if-setninger
- Enhver kodeblokk kan inneholde all type kode, også nye if-setninger.
- En if-setning som er inneholdt i en slik blokk, kalles en nøstet if-setning.

#### Eksempel på en nøstet if-setning
Du søker boliglån i en bank. Banken har noen kriterier for å gi lån:
- Du får låne maks tre ganger brutto-lønn.
- Du får låne maks 60% av boligens verdi.

```python
lånebeløp = float(input("Hvor mye ønsker du å låne? "))
boligverdi = float(input("Hva er boligens verdi? "))
inntekt = float(input("Hva er din brutto-lønn? "))

if lånebeløp <= 3 * inntekt:
    if lånebeløp <= 0.6 * boligverdi:
        print(f"Gratulerer! Ditt lån på kr {lånebeløp} er innvilget.")
    else:
        print("Dessverre, ditt lån er ikke innvilget.")
        print("Du har ikke tilstrekkelig sikkerhet i boligen.")
else:
    print("Dessverre, ditt lån er ikke innvilget.")
    print("Boliglånet overskrider tre ganger din inntekt.")

```

### if-elif-else
Vi kan utføre flere tester på samme nivå ved å bruke **elif** (som står for else if).

Logikken fra eksempelet over kan skrives om slik:
```python
if (lånebeløp > 3 * inntekt):
    print("Dessverre, ditt lån er ikke innvilget.")
    print("Boliglånet overskrider tre ganger din inntekt.")
elif (lånebeløp > 0.6 * boligverdi):
    print("Dessverre, ditt lån er ikke innvilget.")
    print("Du har ikke tilstrekkelig sikkerhet i boligen.")
else:
    print(f"Gratulerer! Ditt lån på kr {lånebeløp} er innvilget.")
```

- Først så sjekkes det om du har nok inntekt. Har du det så kjøres if-kodeblokken og ingen av de andre blokkene.
- Kun hvis du har nok inntekt (if-setningen er False) så sjekkes lånedekningen i elif-blokken. 
- Hvis både if- og elif-setningen er False så kjøres else-blokken.

### Logiske operatorer: and, or og not
Vi kan lage sammensatte tester ved å kombinere dem med de logiske operatorene `and`, `or` og `not`.

### `and` (og)
Returnerer True hvis **begge** verdiene er True.

| a       | b       | a and b  |
|---------|---------|----------|
| False   | False   | False    |
| False   | True    | False    |
| True    | False   | False    |
| True    | True    | True     |

#### `or` (eller)
Returnerer True hvis **minst én** av verdiene er True.

| a       | b       | a or b   |
|---------|---------|----------|
| False   | False   | False    |
| False   | True    | True     |
| True    | False   | True     |
| True    | True    | True     |

#### `not` (ikke)
Returnerer motsatt av verdien.

| a       | not a   |
|---------|---------|
| False   | True    |
| True    | False   |


```python
# Noen eksempler på bruk logiske operatorer

x = 5
print(not x == 0)        # True hvis x er forskjellig fra 0
print(x != 0)            # samme som over
print(x > 0 and x < 10)  # True for alle x mellom 0 og 10
print(x < 4 or x > 10)   # True for alle x mindre enn 4 og større enn 10
```

---

## Løkker - Å gjenta deler av koden
Løkker brukes for å gjøre en handling flere ganger uten å måtte skrive samme kode om og om igjen. Python har to typer løkker: **for-løkker** og **while-løkker**.

### for-løkker
En `for`-løkke gjentar noe for hver verdi i en liste, rekke eller annen samling.

Eksempel: Skriv ut tall fra en liste
```python
tall = [4, 1, 8, 2]

for nummer in tall:
    print("Tallet er:", nummer)
```

Når vi skriver `for number in tall` vil Python hente ut ett og ett element fra lista og kjøre kodeblokka en gang for hvert element.

Vi kan også iterere gjennom en streng:

```python
for character in "hello":
  print(character)
```

Hvis vi skal utføre en for-løkke et visst antall ganger, så bruker vi 
et eget range-objekt i Python:

Hvis vi skal telle til 4: 

```python
for i in range(5):
    print(i)
```
- range(5) gjør at løkka kjører 5 ganger, med tallsekvensen 0,1,2,3,4
    - dvs., når range gis kun ett argument, er dette tallet _til_-verdi, altså ikke _til-og-med_.
    - default startverdi for range( ) er 0.
    - default stegverdi er 1, dvs. for hvert tall i sekvensen øker verdien med 1.

Flere eksempler som illustrerer hvordan du kan bruke `range()`

```python
def create_list(sequence):
  result = []
  for element in sequence:
    result.append(element)
  return result

print(create_list(range(4))) # |0, 1, 2, 3]
print(create_list(range(2,6))) # [2, 3, 4, 5]
print(create_list(range(1, 10, 3))) # [1, 4, 7]
print(create_list(range(20, -1, -4))) # [20, 16, 12, 8, 4, 0]
```
- range(2,6) gir sekvensen 2, 3, 4, 5.
    - med to argument blir første startverdi, andre blir til-verdi.
    - stegverdi er fortsatt default, +1.
- hvis vi ønsker en annen stegverdi enn +1, må vi gi inn et tredje argument til range().
    - range(1, 10, 3) gir dermed sekvensen 1, 4, 7.
        - og fremdeles ikke 10, siden til-verdi ikke er med.
    - range(20, -1, -4) viser at vi også kan telle baklengs: 20, 16, 12, 8, 4, 0.
        - her blir stegverdi -4, dvs. trekker fra 4 for hver runde.
        - siste tall i sekvensen blir 0, siden til-verdi var satt til -1 som er mindre enn 0.

### while-løkker
While-løkke brukes når vi vil repetere en handling.
- Handlingen repeteres så lenge betingelsen som står bak while er __True__.
- koden som står på innrykk under while, er den som tilhører løkka.

Hvis betingelsen bak while er __False__ blir løkka ikke utført. Denne koden printer derfor kun start og stopp, ikke fortsett...

```python
print('start')
while False:
    print('fortsett')
print('stopp')
```

Med __True__ bak while, vil løkka gå i det uendelige, såkalt "evig løkke".
- koden under printer stadig nye linjer med fortsett, kommer aldri til stopp

Alle som har programmert en del, har ved en feil fått evig løkke.
- Heldigvis er det bare å trykke på STOP (den firkanta knappen ved siden av Run) eller trykke Ctrl-C i terminalen. 

```python
print('start')
while True:
    print('fortsett')
print('stopp')
```

Å sette True eller False direkte i betingelsen er lite meningsfylt, men bare gjort her for å vise hvordan mekanismen virker:
- løkka kjører mens vi har True, kjører ikke hvis False

Vanligvis vil betingelsen være basert på en eller flere variabler, og variablene må endre verdi underveis, slik at vi før eller senere får False (med mindre vi faktisk ønsker en evig løkke).
    
Nedenfor kommer noen små eksempler på bruk av while-løkke:

```python
def stabil_latter(antall):
    latter = 'Tillat meg å le: '
    tall = 1
    while tall <= antall:
        latter += 'ha'
        tall += 1
    return latter

print(stabil_latter(0))
print(stabil_latter(3))
```

Som vi ser over:
- når 0 settes inn for antall, kjører ikke løkka i det hele tatt
    - betingelsen blir 1 <= 0 som er False
    - returnert streng blir kun 'Tillat meg å le: ' uten noen latter bak
- når 3 settes inn for antall, kjører løkka tre ganger
    - 'hahaha' er blitt lagt til bakerst i strengen, en 'ha' for hver runde av løkka

#### While-løkke med brukerinput:
While-løkke kan blant annet brukes når vi skal ta imot en masse input fra brukeren, og skal fortsette inntil brukeren sier at vi skal stoppe. Kodecella under viser et banalt eksempel hvor datamaskinen fortsetter å mase om hvem som er vakrest inntil brukeren svarer __du__.

```python
svar = ''
while svar != 'du':
    svar = input('''Lille bruker på tastaturet der, 
    hvem er vakreste datamaskin i verden her? ''')
print('Takk, der svarte du riktig! Du er ikke så verst du heller!')
```

---

## Syntaksfeil
Selv de beste programmerere gjør av og til feil. Men en erfaren programmerer
- finner oftest raskere ut av feilene
- klarer å rette dem

Viktig del av veien til å bli en god programmerer:
- bli flinkere til å forstå og korrigere feil. 

Her starter vi med den enkleste typen feil
- Syntaksfeil (SyntaxError) 
- betyr at koden bryter med Pythons grammatikkregler

Eksempel der `return` er feilstavet:

```python
def square(x):
  retur x**2
```
- her klager Python på x, men det er "retur" som er feilen. Ofte kan en syntaksfeil føre til at Python klager på koden rundt der feilen faktisk er, men ikke alltid. Det kan enten være på samme linje eller linjen før eller etter. 

Typiske årsaker til feil kan være:
- ulovlige navn (eks. 1xy)
- feilskrevede nøkkelord (eks. retur i stedet for return)
- parenteser eller tekstfnutter som begynnes eller avsluttes feil
- manglende, eller overflødige, skilletegn
- manglende, eller overflødige, kommentartegn
- for få, eller for mange, innrykk

Finne ut av feilene:
- feilmeldingen indikerer hvilken kodelinje, og hva i linja
- noen ganger oppdages feilen lenger bak i koden enn den egentlig er
    - lenger bak på samme linje
    - på neste linje
    - eller helt sist i koden (f.eks. uavsluttet trippelfnutt)
    
Se derfor også på linjer foran hvis du ikke finner noe galt på indikert linje.

---

## Hvordan få hjelp
- W3Schools - https://www.w3schools.com/python/
- "Google" => StackOverflow har ofte mange gode svar
- AI (eks. ChatGPT)
  - Er veldig god på å løse enkle problemstillinger og finne feil i koden din. Det kan også ofte gi deg svar på hele kodeoppgavene du skal løse i dag, så for læringens skyld, ikke bruk AI i dag.
