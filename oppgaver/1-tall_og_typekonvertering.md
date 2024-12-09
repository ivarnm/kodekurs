## a)
I koden under er det noe feil. Finn feilene og rett opp i de

Rett utskrift skal være: `25`

```python
def legg_sammen_to_tall(a, b):
    return str(a) + str(b)

legg_sammen_to_tall(10, 15)
```


## b)
Lag en funksjon `legg_til_landskode(telefonnummer, landskode)` som tar inn `telefonnummer` (`int`) og `landskode` (`int`) som parametere og returnerer telefonnummeret prefixet med "+", landskode og et mellomrom.

```python
# Skriv koden din her

telefonnummer1 = 12345678
landskode1 = 47

telefonnummer2 = 87654321
landskode2 = 46

print(legg_til_landskode(telefonnummer1, landskode1))
print(legg_til_landskode(telefonnummer2, landskode2))
```

Hvis du har gjort alt rett, skal kodeblokken over gi ut:

```
+47 12345678
+46 87654321
```

## c)
Kodeblokken nedenfor inneholder noen variabler. Konverter alle til `int`. **Merk**: Det lurer seg kanskje noen feil i koden!


```python
a = '1'
b = True
c = False
d = '1.5'
e = '2,45'

# Skriv koden din her

print(f'a er nå {a}')
print(f'b er nå {b}')
print(f'c er nå {c}')
print(f'd er nå {d}')
print(f'e er nå {e}')
```

Hvis du har gjort alt rett, skal kodeblokken over skrive ut:

```
a er nå 1
b er nå 1
c er nå 0
d er nå 1
e er nå 2
```


## d)
Skriv en kode som spør hvor gammel brukeren er. Koden skal så fortelle brukeren hvor gammel han er om 5 år.

Eksempel på kjøring:
```
Hvor gammel er du? 8
Om 5 år er du 13 år
```
