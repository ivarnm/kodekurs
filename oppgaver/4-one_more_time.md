## Tutorial om oppsamlingsløkker
Ofte brukes løkker til å samle opp et resultat (f.eks. en tallverdi) som vi er interessert i å finne. Et enkelt eksempel på en oppsamlingsløkke, er følgende som summerer alle tallene fra og med 1 til og med 100 (som egentlig er en unødvendig løkke å kjøre siden resultatet er kjent på forhånd, men greit å bruke som illustrasjon):

```python
summen = 0
for i in range(1, 101):
    summen += i          # summen = summen + i
print("Summen av tallene 1-100:", summen)
```

## a)
Lag en funksjon som ved hjelp av en løkke ber brukeren om å taste inn x heltall, som vist i eksemplet på kjøring under. x tas inn som brukerinput. Til slutt skal funksjonen returnere summen av tallene.

Eksempel på kjøring:
```
Hvor mange tall vil du summere? 7
Skriv inn et heltall: 6
Skriv inn et heltall: 4
Skriv inn et heltall: 7
Skriv inn et heltall: 3
Skriv inn et heltall: 2
Skriv inn et heltall: 456
Skriv inn et heltall: 99
Summen av tallene ble 577
```

## b)
Lag en funksjon som multipliserer sammen alle tallene fra 1,2,3,... og avslutter når produktet er større enn 1000.

Hint: Du vet ikke på forhånd hvor lenge du kan multiplisere tallene før du får et produkt større enn 1000, så her kan det være lurt å bruke en while-løkke med produkt mindre enn 1000 som betingelse. Svaret skal bli 5040.


## Tutorial om nøstede løkker
Nøstede løkker vil si løkker som er inni andre løkker. Et eksempel på en nøstet løkke er en dobbel løkke, som vil si at det er en løkke inni en annen løkke. Doble løkker brukes mye i programmering, typisk når man skal løse problemer som på en eller annen måte er todimensjonale, f.eks. knyttet til matriser eller todimensjonale tabeller med tall. Todimensjonal her kan bety rent visuelt (f.eks. at man skal tegne noe på en skjerm og må oppdatere fargen i hvert punkt i et rutenett av piksler), men behøver ikke å ha noen visuell betydning. Det kan være snakk om dimensjoner av informasjon på en mer abstrakt måte. F.eks. kan de to dimensjonene være tall og verdier i kortstokken, vi kan da generere en hel kortstokk ved en dobbel løkke som følge

```python

def format_card_deck():
    
    farger = ['♠', '♣', '♥', '♦']
    verdier = ['A', '2', '3', '4', '5', '6', '7', '8', '9', '10', 'J', 'Q', 'K']
    outer_string = ""
    
    for farge in farger:  # Traverse the farger-array
        inner_string = ""
        for verdi in verdier: # Traverse the verdier-array
            inner_string += farge + verdi + " " # Add the current farge and verdi, in addition to spacing
        outer_string += inner_string + "\n" # add all the values of one farge to the result, and start at a new line
           
    return outer_string

print(format_card_deck())
```

Vil printe ut:
```
♠A ♠2 ♠3 ♠4 ♠5 ♠6 ♠7 ♠8 ♠9 ♠10 ♠J ♠Q ♠K 
♣A ♣2 ♣3 ♣4 ♣5 ♣6 ♣7 ♣8 ♣9 ♣10 ♣J ♣Q ♣K 
♥A ♥2 ♥3 ♥4 ♥5 ♥6 ♥7 ♥8 ♥9 ♥10 ♥J ♥Q ♥K 
♦A ♦2 ♦3 ♦4 ♦5 ♦6 ♦7 ♦8 ♦9 ♦10 ♦J ♦Q ♦K 
```

## c)
Lag en funksjon som returnerer en tekststreng med alle klokkeslett i løpet av et døgn på en fin måte. Du trenger kun å tenke på timer og minutter. Klokkeslettene skal gå fra 0:0 til 23:59 som vist nedenfor.

Eksempel på kjøring av kode:

```python
print(klokkeslett())

0:0
0:1
0:2
.
.       # Alle klokkeslett imellom her skal skrives ut
.
23:58
23:59
```
