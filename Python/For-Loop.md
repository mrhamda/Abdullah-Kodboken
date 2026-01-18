# Pythonuppgift: [For loop] [Abdullah Hamdan]

## Syfte

> I den här uppgiften lär sig eleven hur man använder **for-loopar** för att repetera kod. Eleven får lära sig att gå igenom innehåll i en lista och hur man använder `range()` för att räkna siffror och koppla dem till listans index.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.
- Du vet vad **Variabler** är.
- Du vet vad **Array** är.

## Steg-för-steg

### Steg 1: Skapa en lista med namn

Innan vi kan loopa behöver vi något att loopa igenom. Vi börjar med att skapa en lista.

```python
namn_lista = ["Alice", "Bob", "Charlie"]
```

- En lista skapas med hjälp av hakparenteser `[]`. Varje namn i listan är en "string" och måste därför ha citattecken runt sig. Namnen separeras med kommatecken.

### Steg 2: Gå igenom listan med en enkel loop

Nu ska vi hälsa på alla i listan utan att behöva skriva `print` tre gånger.

```python
for namn in namn_lista:
    print("Hej " + namn + "!")
```

- `for namn in namn_lista:` betyder: "Ta ett namn i taget från listan och lägg det i variabeln `namn`". Koden under (som är indragen med ett steg) körs sedan en gång för varje namn.

### Steg 3: Loopa med siffror (range)

Ibland vill vi räkna siffror istället för att bara gå igenom ord.

```python
for siffra in range(0, 3):
    print("Siffra:", siffra)
```

- Funktionen `range(0, 3)` skapar en serie siffror som börjar på 0 och slutar innan 3 (alltså 0, 1, 2). Variabeln `siffra` byter värde för varje varv loopen körs.

### Steg 4: Koppla ihop siffror med listan

Nu ska vi använda siffran från loopen för att hämta rätt namn från listan med hjälp av ett index.

```python
for siffra in range(0, 3):
    print("Siffra:", siffra)
    print("Detta representerar namnet", namn_lista[siffra])
```

- I programmering börjar man alltid räkna från 0. `namn_lista[0]` är alltså Alice. Genom att skriva `namn_lista[siffra]` inuti loopen kan vi hämta rätt namn automatiskt baserat på vilken siffra loopen är på.

### Steg 5: Avsluta programmet

Det är bra att visa när loopen är helt färdig.

```python
print("Programmet är klart!")
```

- Eftersom denna rad inte är indragen tillhör den inte loopen. Den körs därför bara en gång helt sist i programmet.
