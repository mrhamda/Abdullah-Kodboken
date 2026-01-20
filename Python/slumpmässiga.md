# Pythonuppgift: [Slumpmässiga] [Abdullah Hamdan]

## Syfte

> I den här uppgiften lär sig eleven hur man arbetar med slumpmässiga tal `(random)` och hur man skapar och skriver till filer med hjälp av Python `(open)`. Eleven får också en introduktion till felhantering med `try` och `except`.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.
- Du vet vad **Variabler** är.

## Steg-för-steg

### Steg 1: Importera verktyg och skapa slumpmässiga tal

Först måste vi hämta Pythons inbyggda verktyg för slumpmässiga tal och bestämma vad filen ska heta och vad som ska stå i den.

```python
import random

fil_nummer = random.randint(1, 100)
filnamn = f"fil.{fil_nummer}.txt"
innehalls_nummer = random.randint(1000, 9999)
```

- `import random` gör att vi kan använda funktionen `randint(start, stopp)` för att få fram ett slumpmässigt tal. Vi skapar två tal: ett för filnamnet och ett för innehållet. `f"..."` (f-string) används för att sätta in siffran direkt i textsträngen för filnamnet.

### Steg 2: Skapa filen och skriv innehåll

Nu ska vi faktiskt be datorn att skapa filen på hårddisken och skriva ner vårt andra slumpmässiga tal i den.

```python
try:
    with open(filnamn, "w") as fil:
        fil.write(str(innehalls_nummer))
    print(f"Klart! Skapade '{filnamn}' med innehållet: {innehalls_nummer}")
except Exception as e:
    print(f"Ett fel uppstod: {e}")
```

- `try`: Här skriver du koden som du vill köra, men som kan orsaka ett fel (t.ex. att skapa en fil eller dela med noll). Det betyder: "Försök göra detta..."

- `except`: Här skriver du vad som ska hända om det blir ett fel i try-blocket. Det betyder: **"Om det blev fel, gör detta istället för att krascha."**

- `with open(filnamn, "w")`: Detta öppnar filen i "write" läge (skrivläge). `with` är smart för det ser till att filen stängs automatiskt när vi är klara.

- `fil.write()`: Här skriver vi faktiskt in talet. Vi måste använda `str()` för att göra om talet till text, eftersom filer bara kan ta emot textsträngar.
