## Hangman

I denne oppgaven bruker vi en enkel while-løkke for å lage et hangman-spill i Python. Dette er en større og mer utfordrende oppgave som du kan prøve deg på hvis du har lyst. Gjerne prøv å bruk AI tillegg for å få erfaring med hvordan det kan hjelpe deg.

Lag et program som tar inn et ord (tekststreng) og antall liv (heltall) fra en bruker, og lar en annen (eller samme) bruker gjette på bokstaver i ordet. 

**a)** Start med å hente inn data fra bruker. Lagre dette i to variabler "hemmelig_ord" og "antall_liv".

**b)** Utvid koden over med en funksjon, *hangman(hemmelig_ord, antall_liv)*, som inneholder en while-løkke. Din oppgave er å fylle inn manglende logikk i henhold til kravene under: 

* Hent inn en bokstav fra bruker
* Sjekk om denne er i det hemmelige ordet 
  * Trekk fra et liv dersom brukeren tipper feil
 * Hvis brukeren ikke har flere liv skal løkken avsluttes.

PS: Husk å skrive ut resultatet til brukeren.

Eksempel på kjøring av kode:

```
Skriv inn det hemmelige ordet: hemmelig
Hvor mange forsøk får brukeren? 2
Gjett på én bokstav i ordet: f
Bokstaven f er ikke i ordet.
Du har  1 liv igjen, prøv på nytt.
Gjett på én bokstav i ordet: h
Stemmer, bokstaven er i ordet
Gjett på én bokstav i ordet: e
Stemmer, bokstaven er i ordet
Gjett på én bokstav i ordet: r
Bokstaven r er ikke i ordet.
Du har ingen liv igjen.
```

**c)**: Fyll inn logikk for å fullføre spillet. Ting som kan implementeres er:

* Avslutt løkken hvis brukeren har gjettet alle bokstavene i løsningsordet. Hint: bruk "break" for å avslutte en løkke

* For hvert gjett, print ut maskert løsningsord med stjerner for hver bokstav som fortsatt ikke er gjettet. `(Eks.: lø*ning*ord)`
