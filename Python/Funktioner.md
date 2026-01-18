# Pythonuppgift: [Funktioner och Inmatning] [Abdullah Hamdan]

## Syfte

> I den här uppgiften lär du dig grunderna i hur man skapar egna funktioner i Python för att utföra beräkningar. Du kommer också lära dig hur man tar emot information från användaren med `input()` och gör om text till tal med `float()`.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.
- Du vet vad **Variabler** är.
- Du vet vad **Operators** är.

## Steg-för-steg

### Steg 1: Ta emot inmatning från användaren

Först behöver vi fråga användaren efter siffror. I Python använder vi `input()`.

```python
tal1 = float(input("Skriv in det första talet: "))
tal2 = float(input("Skriv in det andra talet: "))
```

- Vi använder `float()` för att omvandla texten (string) användaren skriver till ett decimaltal. Utan detta kan vi inte räkna matte med siffrorna.

### Steg 2: Skapa en funktion för addition

En funktion är ett block kod som bara körs när man anropar den. Vi använder ordet def.

```python
def addera():
    return tal1 + tal2
```

- `def addera():` skapar funktionen. return skickar tillbaka resultatet av plus räkningen så att vi kan använda det senare.

### Steg 3: Skapa en funktion för subtraktion

Vi kan skapa hur många funktioner vi vill. Här gör vi en för minus.

```python
def subtrahera():
    return tal1 - tal2
```

- Denna funktion fungerar på samma sätt som additionen, men drar istället bort `tal2` från `tal1`.

### Steg 4: Anropa funktionerna

Att skapa en funktion gör ingenting förrän vi faktiskt "anropar" den, alltså säger till programmet att köra den koden.

```python
summa = addera()
skillnad = subtrahera()
```

- Vi sparar resultatet från våra funktioner i variablerna `summa` och `skillnad`.

### Steg 5: Skriva ut resultatet

Slutligen vill vi visa för användaren vad svaret blev. Vi använder en `f-string` för att blanda text och variabler.

```python
print("Resultat")
print(f"{tal1} + {tal2} = {summa}")
print(f"{tal1} - {tal2} = {skillnad}")
```

- Inuti måsvingarna `{ }` skriver Python ut det faktiska värdet som finns sparat i variabeln.

OBS: Kom ihåg att Python läser koden uppifrån och ner! Funktionerna måste definieras innan de kan användas.
