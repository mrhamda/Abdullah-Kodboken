# Pythonuppgift: [Match case] [Abdullah Hamdan]

## Syfte

> I den här uppgiften lär du dig hur man kombinerar en loop med villkorsstyrd logik. Du får lära dig hur man använder `range()` för att räkna, samt hur den moderna `match-case` satsen fungerar för att fatta beslut i koden baserat på matematiska villkor.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.
- Du vet vad **Print** är.
- Du vet vad **Operators** är.

### Steg 1: Skapa en loop med `range`

Först måste vi berätta för datorn att vi vill gå igenom många tal efter varandra.

```python
for nummer in range(1, 101):
```

- `for nummer in ...` skapar en loop som tar ett tal i taget och sparar det i variabeln `nummer`. `range(1, 101)` fungerar som en start och stoppskylt. Den börjar på 1 och slutar precis innan **101** (alltså vid 100). Loopen kommer alltså att köras 100 gånger.

### Steg 2: Starta en `match`-sats

Nu ska vi titta närmare på varje tal som loopen ger oss.

```python
    match nummer:
```

- `match nummer` betyder: "Titta på vad som finns inuti variabeln nummer just nu". Det är här vi startar vår beslutsfattning. All kod som hör till denna match måste ha ett extra indrag åt höger.

### Steg 3: Kontrollera om talet är jämnt med en "Guard"

Vi vill veta om talet går att dela med 2 utan att det blir något över.

```python
        case n if n % 2 == 0:
            print(f"{n} är jämnt")
```

- `case n`: Vi ger talet ett tillfälligt namn, `n`, inuti denna rad.

- if `n % 2 == 0`: Detta kallas för en "guard". Procenttecknet % (modulo) räknar ut resten av en division. Om du delar ett jämnt tal med 2 blir resten alltid 0.

- Om detta stämmer, körs `print`-raden. Bokstaven `f` framför texten gör att vi kan skriva variabeln `{n}` direkt i meningen.

### Steg 4: Kontrollera om talet är jämnt med en "Guard"

Vi vill veta om talet går att dela med 2 utan att det blir något över.

```python
        case _:
            print(f"{nummer} är udda")
```

- Understrecket `_` fungerar som en fångstmaska för allt som inte matchade det första villkoret. I programmering kallas detta ofta för ett "wildcard" eller "default". Om talet inte var jämnt, hamnar det här, och vi skriver ut att det är udda.

### Hela koden:

```python
for nummer in range(1, 101):
    match nummer:
        case n if n % 2 == 0:
            print(f"{n} är jämnt")
        case _:
            print(f"{nummer} är udda")
```
