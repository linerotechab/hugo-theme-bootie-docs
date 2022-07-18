+++

title = "Introduktion till pseudokod"

categories = ["Common"]

language= "Svenska"

+++
En grupp vänner besöker dig denna kväll, och du vill erbjuda dem hemlagad pestopizza i medelhavsstil. Problemet är att du inte vet hur du tillagar den. Du söker efter receptet på nätet och upptäcker att den kan tillagas i tre steg. Receptet ser ut så här:

> **Steg 1**
> Förvärm en ugn till 175 °C.
>
> **Steg 2**
> Bred ut peston på pizzabotten; toppa med fetaost, tomater och oliver.
>
> **Steg 3**
> Grädda i den förvärmda ugnen tills osten har smält, 6 till 8 minuter.

Grattis, din pizza var en succé; din vän älskade den. **Men vad har en pestopizza i medelhavsstil med programmering att göra?**

I mycket förenklade termer är matlagning inget annat än att följa en serie instruktioner tills en maträtt har tillagats. På samma sätt är ett datorprogram inget annat än en serie instruktioner (d.v.s. kommandon) som, när de väl körts i en specifik ordning, ger ett resultat.

Kockar följer ett **recept** för att skapa en maträtt. På samma sätt följer utvecklare en **algoritm** för att skapa ett program.

# Vad är en algoritm?
En *algoritm* är en **sekvens av instruktioner** om hur en uppgift ska lösas.

Din roll som utvecklare är enkel: **för varje problem du stöter på skapar du en algoritm som löser det**. Låt oss till exempel säga att du måste utveckla ett datorprogram som beräknar ytan hos en triangel.

Hur skulle algoritmen se ut?

> ### Algoritm för ytan hos en triangel
> **Steg 1**
> Ta reda på triangelns bas
>
> **Steg 2**
> Ta reda på triangelns höjd
>
> **Steg 3**
> Beräkna ytan genom att multiplicera *bas* * *höjd* * 0,5
>
> **Steg 4**
> Visa resultatet för användaren

När datorprogrammet kör de här stegen kommer programmet att returnera ytan hos en triangel.

# Lös det först på papper
Den mänskliga hjärnan är väldigt komplex och väldigt smart. Om jag ber dig göra mig en smörgås behöver jag inte specificera varje steg för att göra en smörgås. Datorn inte dock så smart. Om jag vill skapa en applikation som gör en smörgås **måste jag specificera varje enskilt steg på ett mycket detaljerat sätt**; annars kanske jag inte får någon smörgås alls, eller ännu värre, ett nerbränt kök.

En del av detta program är att hjälpa dig att utveckla det vi kallar *programmerarsinnet*, vilket innebär att tänka på problem på ett mycket detaljerat sätt. Att utveckla *programmerarsinnet* börjar med att förstå och öva på konceptet att *först lösa det på papper*. Det betyder att **du måste ha lösningen på papper innan du börjar skriva din första kodrad. (Ja, bokstavligen på papper)**.

Om du till exempel vill skapa en applikation som gör en smörgås kommer din instinkt vara att börja skriva kod, **men gör inte det**. **Lös istället problemet på papper först**: strukturera dina idéer, strukturera algoritmen och definiera rätt sekvens av steg. Att lösa problemet på papper hjälper dig att hitta problem med din algoritm redan innan du skriver den första kodraden, och hjälper dig att fokusera på en sak i taget: först på att lösa problemet och sedan översätta din algoritm till kod.

Algoritmen du skriver på papper kallas formellt *pseudokod*.

# Vad är pseudokod?
*Pseudokod* är en informell, högnivåbeskrivning av en algoritm. De viktigaste egenskaperna är följande:
- Den är avsedd att läsas av människor och inte av datorer.
- Det finns ingen kod när du skriver pseudokod
- Beskriv **vad** som behöver göras och **inte hur** det behöver göras.

{{% notice warning %}}
Eftersom pseudokod är en viktig del av programmet måste du visa din pseudokod varje gång du presenterar en lösning för klassen eller begär hjälp från instruktören.
{{% /notice %}}

# Pseudokodens syntax
Det finns ingen formell syntax eller sätt att skriva pseudokod. För detta program kommer vi dock att följa denna syntax:

- **INPUT**: Anger att en användare matar in ett värde
- **OUTPUT**: Indikerar att en utmatning visas på skärmen
- **WHILE**: En iteration som har ett villkor i början
- **FOR**: En räknande iteration
- **IF – THEN – ELSE:** ett beslut där ett val görs

Instruktioner som förekommer i ett kommando med ett *urval* eller en *iteration* indragna.

{{% notice note %}}
I denna modul är det godtagbart att inte förstå vad `WHILE` och `FOR` gör. Vi kommer dock att lära oss mer om dessa i de kommande modulerna.
{{% /notice %}}

### Exempel 1
Skriv pseudokod för att beräkna ytan hos en cirkel och skriv ut resultatet.

{{<kotlin>}}
INPUT radius of the circle
Use the equation "PI * radius * radius" to calculate the area
OUTPUT area of the circle
{{</kotlin>}}

### Exempel 2:
Skriv pseudokod som frågar om användarens ålder. Om talet är mindre än `18`, skriv ut meningen `minderårig`; skriv annars ut `vuxen.`

{{<kotlin>}}
INPUT age
IF age < 18 THEN
OUTPUT "minor"
ELSE
OUTPUT "adult"
{{</kotlin>}}

### Exempel 3
Skriv pseudokod för att skriva ut alla udda tal från `50` till `100.`{{<kotlin>}}
FOR number is 50 to 100
IF number is odd
OUTPUT number
{{</kotlin>}}

# Flödesschema
Ett annat sätt att visualisera pseudokod är att använda flödesscheman. Formerna som ska användas för vart och ett av pseudokodens kommandon är följande:

{{< mermaid align="left">}}
graph TD
B[\INPUT\]
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
B([OUTPUT])
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
B[/FOR\]
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
B[/WHILE\]
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
B{IF};
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
B[Step];
{{< /mermaid >}}

Nedan illustrerar vi hur versionen med flödesschema skapas från exemplen på pseudokod ovan.

### Flödesschema 1
{{< mermaid align="left">}}
graph TD
A((Start)) --> B[\Get the radius of the circle\];
B --> C[Use the equation PI * radius * radius to calculate the area];
C --> D([Print the area]);
D --> E((End));
{{< /mermaid >}}

### Flödesschema 2
{{< mermaid align="left">}}
graph TD
A((Start)) --> B[\Get age of the user\];
B --> C{is age < 18};
C --> |Yes| D([print 'minor'])
C --> |No| E([print 'adult'])
D --> F((End))
E --> F
{{< /mermaid >}}

### Flödesschema 3
{{< mermaid align="left">}}
graph TD
A((Start)) --> B[/number is 50 to 100\];
B --> E((End))
B --> C{is number odd?};
C --> |Yes| D([print number])
D --> B
{{< /mermaid >}}
