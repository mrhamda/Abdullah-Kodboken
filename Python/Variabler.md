# Pythonuppgift: [Variabler] [Abdullah Hamdan]

## Syfte

> Syftet med den här uppgiften är att förstå hur datorn lagrar olika typer av information i sitt minne med hjälp av variabler. Du kommer att lära dig att skilja på text, heltal, decimaltal och logiska värden (sant/falskt). Dessutom lär du dig att använda f-strings för att dynamiskt presentera data och kommunicera med användaren genom programmet.

---

## Förkunskaper

- Du har **VS Code** (eller annan textredigerare) redo.
- **Python 3** är installerat på din dator.
- Du vet hur man skapar en ny fil med ändelsen `.py`.

### Steg 1: Skapa ett heltal (Integer)

Ett heltal är ett tal utan decimaler.

```python
ålder = 10
print(f"Jag är {ålder} år gammal")
```

- Här skapar vi variabeln `ålder` och ger den värdet `25`. Tänk på variabeln som en namngiven låda i datorns minne. Vi skriver namnet på lådan först, sedan ett likhetstecken `=` och sist vad vi vill lägga i lådan.

- Genom att skriva bokstaven `f` precis före citattecknen i `print() funktionen` skapar vi en så kallad `"Formatted String"`.

- Inuti texten kan vi nu använda måsvingar `{}`. När datorn ser dem pausar den utskriften av texten tittar vad som finns i variabeln `ålder` (i det här fallet 25), och klistrar in det värdet direkt i meddelandet.

### Steg 2: Skapa ett flyttal (Float)

Flyttal används för tal med decimaler. Kom ihåg att programmering använder punkt . istället för komma.

```python
längd_cm = 169.5
print(f"Jag är {längd_cm} cm lång")
```

- Här skapar vi variabeln `längd_cm` och ger den värdet `169.5`.

- Det är viktigt att komma ihåg att programmering nästan alltid använder punkt `.` som decimaltecken. Om du skriver `169.5` kommer Python tro att det är två olika tal som separeras av ett kommatecken.

- Vi använder flyttal när vi behöver hög precision till exempel för pengar vetenskapliga mätningar eller som här: längd i meter.

### Steg 3: Skapa en textsträng (String)

En sträng används för att lagra text.

```python
namn = "Alice"
print(f"Välkommen hit, {namn}")
```

- Här skapar vi variabeln `namn` och ger den värdet `Alice`.

- För att datorn ska veta att "Alice" är text och inte ett kommando i programmet, måste vi sätta ordet inom citattecken.

- Precis som med siffror kan vi använda `f formatet` för att hämta namnet ur variabeln. Om vi ändrar värdet på `namn` till "Julius", kommer hela hälsningen att ändras automatiskt nästa gång vi kör programmet.

### Steg 4: Skapa en textsträng (String)

Ett enskilt tecken kallas ofta för en "char". I Python fungerar det som en kort textsträng.

```python
bokstav = 'A'
print(f"Min första bokstav är {bokstav}")
```

- Här skapar vi variabeln `bokstav` och ger den värdet `A`.

- I Python kan man använda både `'` och `"`. En vanlig tradition är att använda enkla citattecken när man bara har ett enda tecken, för att visa för andra programmerare att variabeln bara är tänkt att hålla en bokstav.

### Steg 5: Skapa ett logiskt värde (Boolean)

En boolean kan bara ha två värden: Sant eller Falskt.

```python
körkort = False
print(f"Jag har körkort: {körkort}")
```

- Här skapar vi variabeln `körkort` och ger den värdet `False`.

- Denna typ används för att kontrollera om något stämmer eller inte.

- I Python stavas dessa alltid med stor första bokstav: `True` och `False`. Om du skriver dem med små bokstäver kommer datorn inte att förstå vad du menar och ge dig ett felmeddelande. De ska inte heller ha citattecken runt sig, för då blir de vanliga textsträngar istället för logiska värden.
