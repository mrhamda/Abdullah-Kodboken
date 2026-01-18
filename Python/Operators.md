# Pythonuppgift: [Operators och logik] [Abdullah Hamdan]

## Syfte

> I den här uppgiften lär sig eleven att använda `Assignment Operators && Comparison Operators`.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.
- Du vet vad **Variabler** är.

## Steg-för-steg

### Steg 1: Ändra värden med Addition och Subtraktion

Vi börjar med att se hur vi kan uppdatera en variabel genom att lägga till eller dra ifrån värden.

```python
mitt_poäng = 10
print(f"Vi börjar med poäng = {mitt_poäng}")

mitt_poäng += 5
print(f"Efter poäng += 5 (Addition) är värdet nu: {mitt_poäng}")

mitt_poäng -= 3
print(f"Efter poäng -= 3 (Subtraktion) är värdet nu: {mitt_poäng}")
```

- `+=` betyder "plus lika med". Det är ett snabbare sätt att skriva `mitt_poäng = mitt_poäng + 5`. Datorn tar det gamla värdet lägger till 5 och sparar det nya resultatet i samma låda.

- `-=` fungerar på samma sätt men för subtraktion. Det minskar värdet som redan finns i variabeln.

### Steg 2: Multiplikation och Division och Modulo

Nu ska vi se hur vi kan gångra och dela värdet i en variabel.

```python
mitt_poäng *= 2
print(f"Efter poäng *= 2 (Multiplikation) är värdet nu: {mitt_poäng}")

mitt_poäng /= 4
print(f"Efter poäng /= 4 (Division) är värdet nu: {mitt_poäng}")

mitt_tal = 10
mitt_tal %= 3
print(f"Efter 10 %= 3 (Modulo) är värdet nu: {mitt_tal}")
```

- `*=` används för multiplikation. Om poängen var 12 och vi kör `*= 2`, blir det 24.

- `/=` används för division. Notera: När du delar ett tal i Python blir resultatet alltid ett decimaltal, till exempel `3.0` istället för bara `3`.

- `%=` kallas för **Modulo**. Den räknar ut vad som blir över vid en division.

- Exempel: Om du har 10 godisar och delar dem på 3 personer, får de 3 godisar var. Då blir det 1 godis över. Det är den ettan som sparas i variabeln.

### Steg 3: Jämföra om saker är lika eller olika

Jämförelseoperatorer ändrar inte på variablerna, de skapar bara ett svar: `True` (Sant) eller `False` (Falskt).

```python
alice_poäng = 10
oskars_poäng = 20

resultat_lika = (alice_poäng == oskars_poäng)
print(f"Är {alice_poäng} == {oskars_poäng}? Svar: {resultat_lika}")

resultat_olika = (alice_poäng != oskars_poäng)
print(f"Är {alice_poäng} != {oskars_poäng}? Svar: {resultat_olika}")
```

- `==` (dubbelt likhetstecken) är en **fråga**: "Är dessa två exakt lika stora?". Använd aldrig ett enkelt `=` när du vill jämföra, för det används bara för att ge en variabel ett värde.

- `!=` betyder "inte lika med". Den svarar `True` om värdena är olika.

### Steg 4: Jämföra storlek (Mer än, mindre än eller lika)

Här lär vi oss att kolla om ett värde är större, mindre eller om det når upp till en viss gräns.

```python
resultat_större = (alice_poäng > oskars_poäng)
print(f"Är {alice_poäng} > {oskars_poäng}? Svar: {resultat_större}")

resultat_större_lika = (alice_poäng >= 10)
print(f"Är {alice_poäng} >= 10? Svar: {resultat_större_lika}")

resultat_mindre_lika = (alice_poäng <= 5)
print(f"Är {alice_poäng} <= 5? Svar: {resultat_mindre_lika}")
```

- `>` och `<` kollar bara om något är strikt större eller mindre än.

- `>=` (Större än eller lika med) och `<=` (Mindre än eller lika med) är jätteviktiga. De kollar om talet är större/mindre ELLER om det är exakt samma. Om `alice_poäng är 10`, så är alice_poäng >= 10 sant (`True`), men `alice_poäng > 10` är falskt (`False`).

### Steg 5: Kombinera krav med `and`

Ibland måste flera saker vara sanna samtidigt för att resultatet ska bli sant. För detta använder vi `and`.

```python
poäng = 15
har_nyckel = True

kan_öppna_dörr = (poäng >= 10 and har_nyckel == True)
print(f"Har du 10 poäng OCH nyckel? Svar: {kan_öppna_dörr}")
```

- `and` kräver att båda sidorna är `True`. Om du har poängen men saknar nyckeln, blir svaret `False`.

### Steg 6: Ge alternativ med `or`

Ibland räcker det med att ett av flera krav är uppfyllt. Då använder vi or.

```python
är_helg = True
är_lov = False

är_ledig = (är_helg == True or är_lov == True)
print(f"Är det helg ELLER lov? Svar: {är_ledig}")
```

- `or` ger svaret `True` om minst en av sidorna är sann. Det spelar ingen roll om det bara är helg, bara lov eller både och du får svaret `True` ändå.
