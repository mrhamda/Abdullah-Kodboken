# Pythonuppgift: [While loop] [Abdullah Hamdan]

## Syfte

> I den här uppgiften lär sig eleven hur man styr flödet i en loop. Vi går igenom hur man hoppar över specifika steg med `continue` och hur man avbryter en hel process i förtid med `break`.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.
- Du vet vad **Variabler** är.

## Steg-för-steg

### Steg 1: Skapa loopen och räknaren

Först behöver vi en variabel som håller koll på hur många varv vi har kört, och en loop som startar.

```python
count = 0

while count < 5:
    count += 1
```

- Vi börjar på 0. `while count < 5` betyder att loopen fortsätter så länge `count` är mindre än 5. Inuti loopen plussar vi på 1 direkt (`count += 1`), vilket gör att första varvet börjar med siffran 1.

### Steg 2: Hoppa över ett steg med `continue`

Ibland vill vi att loopen ska fortsätta, men just för ett specifikt värde vill vi inte köra resten av koden.

```python
    if count == 2:
            print("Hoppar över 2 (continue)")
            continue
```

- Här kollar vi om `count` är exakt 2. Om det är sant körs `continue`. Det betyder: "Stopp! Gå direkt tillbaka till början av loopen och börja på nästa varv". Datorn kommer alltså inte att nå `print`-raden längst ner för just siffran 2.

### Steg 3: Avbryt loopen helt med `break`

Om något speciellt händer vill vi kanske stänga ner hela loopen direkt, även om villkoret `count < 5` fortfarande är sant.

```python
    if count == 4:
            print("Hittade 4, avslutar loopen (break)")
            break
```

- När `count` blir 4 körs `break`. Det fungerar som en nödbroms. Loopen avslutas omedelbart och programmet hoppar ner till den allra sista raden utanför loopen. Siffran 5 kommer alltså aldrig att hinnas med.

### Steg 4: Skriv ut resultatet

Längst ner i loopen skriver vi ut siffran, men bara om vi inte har råkat ut för en `continue` eller `break`.

```python
    print(f"Numret är: {count}")

print("Loopen är klar!")
```

- `print(f"...")` används för att skriva ut variabeln inuti texten. Den sista raden ("Loopen är klar!") har ingen indragning (mellanslag till vänster), vilket betyder att den körs först när hela loopen har stannat.

### Hela koden:

```python
count = 0

print("Startar while-loop:")
while count < 5:
    count += 1

    if count == 2:
        print("Hoppar över 2 (continue)")
        continue

    if count == 4:
        print("Hittade 4, avslutar loopen (break)")
        break

    print(f"Numret är: {count}")

print("Loopen är klar!")
```
