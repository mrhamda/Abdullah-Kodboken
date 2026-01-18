# Pythonuppgift: [Special Tecken] [Abdullah Hamdan]

## Syfte

> I den här uppgiften lär du dig att använda så kallade **escape-sekvenser**. Det är speciella kombinationer av tecken (som börjar med `\`) som gör att du kan formatera din text, skapa nya rader och lägga till tecken som annars skulle "trasiga" koden.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.
- Du vet vad **print** är.

### Steg 1: Skapa nya rader med `\n`

När vi skriver en vanlig textsträng fortsätter den på samma rad. Om vi vill att datorn ska göra en radbrytning använder vi symbolen `\n` (n står för newline).

```python
print("Här är rad ett.\nHär är rad två.")
```

- När Python ser backslash `\` följt av ett `n`, tolkar den det inte som vanlig text. Istället ser datorn det som ett kommando att trycka på "Enter"-tangenten och fortsätta skriva på nästa rad.

### Steg 2: Skapa snygga tabbar med `\t`

Ibland vill vi att text ska ligga i snygga kolumner. Istället för att trycka på mellanslag massor av gånger använder vi `\t` (t står för tab).

```python
print("Namn:\tKalle")
print("Ålder:\t12")
```

- `\t` fungerar precis som Tab-tangenten på ditt tangentbord. Den hoppar fram ett bestämt antal steg så att texten efteråt hamnar under varandra, vilket gör det lättare att läsa listor.

### Steg 3: Skriv ut citattecken i en text

Om du skriver `print("Han sa "Hej"")` kommer Python bli förvirrad eftersom den tror att texten tar slut vid det andra citattecknet. För att lösa detta använder vi `\"`.

```python
print("Namn:\tKalle")
print("Ålder:\t12")
```

- Backslashet berättar för Python: "Det här citattecknet är bara en vanlig symbol i texten, avsluta inte hela strängen här!".

### Steg 4: Hur man skriver ett backslash `\`

Eftersom backslash `\` används för att starta alla dessa specialkommandon, vad gör vi om vi faktiskt vill visa ett vanligt backslash i texten? Svaret är att vi skriver två stycken: `\\`.

```python
print("Sökvägen till mappen är C:\\Users\\Dokument")
```

- Det första backslashet "låser upp" det andra, så att datorn förstår att du faktiskt vill skriva ut ett backslash-tecken på skärmen.
