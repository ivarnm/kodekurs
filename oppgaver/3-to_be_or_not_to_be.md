## a) Stemmerett
I denne deloppgaven skal det lages et program som sjekker om en person kan stemme, altså om personen er 18 år eller eldre. Man må da spørre brukeren om alder og lagre svaret i en variabel, for deretter å sjekke om brukerens alder er 18 eller mer.

**Eksempel på kjøring**

```
Hvor gammel er du? 19
Du kan stemme

Hvor gammel er du? 18
Du kan stemme

Hvor gammel er du? 2
Du kan ikke stemme ennå
```

## b) Kan stemme litt
Lag en utvidet versjon av programmet fra (a) med hjelp av `elif` som sier om personen kan stemme eller ikke, med følgende regler:

- `alder >= 18`: Kan stemme både ved lokalvalg og Stortingsvalg
- `alder >= 16`: Kan stemme ved lokalvalg, men ikke ved Stortingsvalg
- ellers (`alder < 16`): Kan ikke stemme.

**Eksempel på kjøring**

```
Hvor gammel er du? 19
Du kan stemme både ved lokalvalg og Stortingsvalg

Hvor gammel er du? 17
Du kan stemme ved lokalvalg, men ikke ved Stortingsvalg

Hvor gammel er du? 12
Du kan ikke stemme ennå
```


## c) Sammenligning av strenger
Du skal nå lage et program som sammenligner to matvarer, og sjekker om de er like. Det skal ikke spille noen rolle om matvarenavnene som sendes inn har store eller små bokstaver, dvs. at `"druer"` og `"DrUer"` skal regnes som like matvarer (se Hint). Det trengs ikke å ta hensyn til entall og flertall, dvs. at `"druer"` og `"drue"` regnes som to forskjellige matvarer.

**Eksempel på kjøring:**
```
Sammenligner druer og DrUer
Det er samme matvare

Sammenligner druer og drue
Dette er to forskjellige matvarer

Sammenligner TomAT og ToMat
Det er samme matvare

Sammenligner tomat og potet
Dette er to forskjellige matvarer
```

#### Hint
`str.lower()` returnerer en kopi av strengen bestående av små bokstaver.

Dvs., om du har en variabel `a = "DrUer"`, vil `a.lower()` gi strengen `"druer"`. Men husk, `a.lower()` endrer ikke på variabelen `a`, så man må enten lage en ny variabel `b = a.lower()` og bruke variabelen `b` i sjekken, eller så kan man bruke `a.lower()` direkte i sjekken i stedet for `a`.


## d) Datamaskinen som tigget epler (vanskelig)
I denne oppgaven får du utdelt en kodesnutt som inneholder feil. Det er både konkrete feil i koden (Python-syntaks) og logiske feil (brukeren kan gi input som får programmet til å gi betydningsløse svar). 

Din oppgave er å rette opp i syntaks-feilene, og håndtere de logiske feilene på en fornuftig måte. 

### d1:
Funksjonen tar inn hvor mange epler brukeren har, og hvor mange han er villig til å gi bort, som argumenter. Basert på disse argumentene er det tre mulige utfall, som vist under:

```
>>> teste_gavmildhet(0, 0)

Dette er et program for å teste din sjenerøsitet.
Du har 0 epler.
Æsj, det sier du bare for å slippe å gi noe!
```
  
```
>>> teste_gavmildhet(5, 2)

Dette er et program for å teste din sjenerøsitet.
Du har 5 epler.
Du er villig til å gi meg 2 epler.
Du beholder det meste for deg selv...
Du har nå 3 epler igjen.
```
  
```
>>> teste_gavmildhet(7, 5)

Dette er et program for å teste din sjenerøsitet.
Du har 7 epler.
Du er villig til å gi meg 5 epler.
Takk, det var snilt!
Du har nå 2 epler igjen. 
```

Koden som skal kjøre programmet er som vist under. **Finn syntaksfeilene og rett opp i dem slik at koden kjører som vist i eksempelteksten.**

```python
def teste_gavmildhet(antall_epler, antall_gis_bort):
    streng = "Dette er et program for å teste din sjenerøsitet.\n"
    streng += f"Du har {antall_epler} epler.\n"
    
    if antall_epler = 0:
        streng += "Æsj, det sier du bare for å slippe å gi noe!\n"
        return streng
    else
    streng += f"Du er villig til å gi meg {antall_gis_bort} epler.\n"
    if antall_gis_bort < antall_epler / 2:
       streng += "Du beholder det meste for deg selv...\n"
           else:
           streng += "Takk, det var snilt!")
       strent += f"Du har nå {har_epler - gir_epler} epler igjen.\n"
    return streng"
```

### d2:
Utskriften av siste print-setning vil bli grammatisk feil hvis brukeren har igjen 1 eple, siden det skrives «epler». Utvid funksjonen slik at det skriver:

  
```
>>> test_gavmildhet(5, 4)

Dette er et program for å teste din sjenerøsitet.
Du har 5 epler.
Du er villig til å gi meg 4 epler.
Takk, det var snilt!
Du har nå 1 eple igjen. 
```

hvis det ble akkurat ett, ellers epler i flertall som det står nå.

## d3:
Hvis brukeren skriver inn et større tall for hvor mange epler man kan gi bort enn hva man faktisk hadde, kommer siste linje ut med et negativt tall.

Utvid funksjonen ytterligere slik at hvis brukeren f.eks. har 7 epler, men vil gi bort 9, avslutter funksjonen med

  
```
Du har nå 0 epler igjen. Gi meg de 2 du skylder meg neste gang vi møtes.
```
