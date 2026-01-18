# Pythonuppgift: [Array] [Abdullah Hamdan]

## Syfte

> I den här uppgiften lär du dig grunderna i hur man använder array i Python för att spara och organisera information. Du kommer att lära dig att lägga till saker, ta bort saker, ändra innehåll och läsa listan från olika håll.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.
- Du vet vad **Variabler** är.

## Steg-för-steg

### Steg 1: Skapa en lista och skriv ut den

Först behöver vi skapa en lista med några föremål. I Python använder vi kantiga parenteser `[]`.

```python
it_prylar = ["Laptop", "Mus", "Tangentbord"]
print(f"Listan från början: {it_prylar}")
```

- Vi skapar en variabel som heter `it_prylar`. Den innehåller tre texter (strings). Genom att använda `f` framför citattecknen i `print` kan vi enkelt sätta in variabeln direkt i texten.

### Steg 2: Lägg till och ta bort föremål

Listor är praktiska eftersom de kan ändras medan programmet körs.

```python
it_prylar.append("Skärm")
print(f"Listan efter att ha lagt till skärm: {it_prylar}")

it_prylar.remove("Mus")
print(f"Listan efter att ha tagit bort mus: {it_prylar}")
```

- `.append()` lägger alltid till något längst ner i listan. `.remove()` letar upp det exakta ordet och tar bort det.

### Steg 3: Ändra ett specifikt element

Varje sak i listan har en plats, ett så kallat index. Den första saken har alltid index **0**.

```python
it_prylar[0] = "MacBook"
print(f"Listan efter att ha ändrat första elementet till MacBook: {it_prylar}")
```

- Genom att skriva `it_prylar[0]` kommer vi åt den första platsen. Här byter vi ut "Laptop" mot "MacBook".

### Steg 4: Komma åt specifika delar (Access)

Du kan hämta ut enstaka saker från listan och spara dem i egna variabler.

```python
första = it_prylar[0]
andra = it_prylar[1]
print(f"Första elementet är: {första}")
print(f"Andra elementet är: {andra}")
```

- Vi hämtar värdet på plats 0 och 1. Detta kallas för att "accessa" element i en array/lista.

### Steg 5: Läsa från slutet och vända ordningen

Ibland vet man inte hur lång listan är, men man vill ändå åt det sista som finns där.

```python
sista = it_prylar[-1]
näst_sista = it_prylar[-2]
print(f"Sista elementet är: {sista}")
print(f"Näst sista elementet är: {näst_sista}")

it_prylar.reverse()
print(f"Listan efter reverse: {it_prylar}")
```

- Index `-1` betyder "det sista elementet". Index `-2` betyder "näst sista". Kommandot `.reverse()` vänder på hela listan så att den sista saken blir först.

### Steg 6: Kolla listans storlek

Det är ofta bra att veta hur många saker som finns i listan totalt.

```python
storlek = len(it_prylar)
print(f"Listans storlek är: {storlek}")
```

- `len()` är en förkortning av "length" (längd). Den räknar hur många objekt som finns inuti listan.

### OBS: List och array är nästan samma fast tekniskt i djup nivå är de olika!
