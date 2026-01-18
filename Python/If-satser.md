# Pythonuppgift: [If-satser] [Abdullah Hamdan]

## Syfte

> I den här uppgiften lär sig eleven hur ett program fattar beslut genom logiska val. Målet är att förstå hur man styr programflödet med `if`, `elif` och `else`, samt hur flera krav kan kombineras med de logiska operatorerna `and`, `or` och `not`. Eleven får även praktisk övning i att ta emot information från en användare via `input()` och konvertera textsträngar till heltal för att kunna utföra matematiska jämförelser.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.
- Du vet vad **Variabler** är.
- Du vet vad **Operators** är.

## Steg-för-steg

### Steg 1: Samla in information

För att programmet ska kunna fatta ett beslut behöver vi veta två saker: personens ålder och om de har sällskap av en vuxen.

```python
svar = input("Hur gammal är du? ")
alder = int(svar)

med_vuxen = input("Har du en vuxen med dig? (ja/nej) ")
```

- `input()` stannar programmet och väntar på att användaren skriver något.

- `int(svar)` är jätteviktigt! Datorn ser "15" som text, men för att kunna jämföra med siffror (större än/mindre än) måste vi göra om det till ett heltal (integer).

- `med_vuxen` sparar texten "ja" eller "nej" som vi ska använda senare.

### Steg 2: Kontrollera högsta åldersgränsen

Vi börjar med att kolla om personen är gammal nog att gå in helt själv.

```python
if alder >= 15:
    print("Välkommen in! Du är gammal nog.")
```

Om personen är 15 år eller äldre (`>= 15`) körs denna kod. Då hoppar datorn över resten av kontrollerna eftersom personen redan är godkänd.

### Steg 3: Kombinera krav med `and` (`elif`)

Om personen är under 15, kollar vi om de uppfyller kraven för 11 årsgränsen. Här krävs två saker samtidigt.

```python
elif alder >= 11 and med_vuxen == "ja":
    print("Välkommen in tillsammans med din vuxen!")
```

- Operatorn `and` betyder att båda sidorna måste vara sanna.

- Är du minst 11 år? **OCH** har du en vuxen med dig? Bara om båda svaren är "Ja" får man gå in här.

### Steg 4: Ge alternativ med `or` (`elif`)

Nu kollar vi om besökaren ska nekas inträde. Det kan hända av två olika anledningar.

```python
elif alder < 11 or med_vuxen == "nej":
    print("Tyvärr, du uppfyller inte kraven för den här filmen.")
```

- Operatorn `or` betyder att det räcker att minst ett av påståendena är sant för att koden ska köras.

- Är du under 11 år? **ELLER** har du ingen vuxen med dig? Om något av detta stämmer nekas man inträde.

### Steg 5: Vänd på logiken med `not` (`if`)

Till sist kollar vi om någon har skrivit in en omöjlig ålder.

```python
if not alder > 0:
    print("Vänta nu, du kan inte vara 0 år eller yngre!")
```

- `not` används för att kontrollera om något inte stämmer. Här läser vi det som: "Om det inte är sant att åldern är större än 0". Det är ett smart sätt att fånga upp felaktiga siffror som t.ex. -5.
