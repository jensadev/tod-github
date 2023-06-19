---
title: Spara ändringar med git
eleventyNavigation:
    key: spara ändringar med git
    parent: git
    order: 1
    excerpt: För att spara ändringar i ett repo så använder Git commits.
---

{% instructions %}

## Introduktion

*[repo]: Repository

I introduktionen till [Git](/introduktion/vad-ar/git-versionshantering/) så kunde du läsa om att Git arbetar med tre tillstånd för filerna i ett repo. Det är viktigt att förstå detta när du arbetar med Git. De tre tillstånden är:

1. **Modified**, filen är ändrad men inte sparad i Git-historiken.
2. **Staged**, filen är ändrad och kommer att sparas i Git-historiken med nästa commit.
3. **Committed**, filen är sparad i Git-historiken.

Utöver detta så har varje enskild fil ett tillstånd:

-   **Untracked** - Filen finns inte i Git-repot och är inte sparat i historiken.
-   **Tracked** - Filen finns i Git-repot och är sparat i historiken.

Så alla filer som är untracked känner inte Git till. Men när en fil är tracked så kan den vara i något av de tre tillstånden.

## Instruktioner

Om du har följt instruktionerna från föregående moment så har du nu ett Git repo. Detta innebär att du har en katalog som innehåller alla filer för ett projekt.

Börja med att kontrollera att du är i rätt katalog. Detta gör du genom att skriva `pwd` i terminalen. Detta kommer att skriva ut den katalog du befinner dig i. Om du inte är i rätt katalog så kan du använda `cd` för att navigera till rätt katalog.

Du kan nu kontrollera statusen för repot genom att skriva `git status` i terminalen.

```bash
On branch main
No commits yet
nothing to commit (create/copy files and use "git add" to track)
```

### Skapa en fil

För att skapa en fil kommer du att använda kommandot `echo`. Kommandot `echo` skriver ut text till terminalen. Du kan använda `echo` för att skapa en fil genom att skriva `echo "Innehåll" > filnamn`. Detta kommer att skapa en fil med namnet `filnamn` och innehållet `Innehåll`.

```bash
echo "Hello World" > hello.txt
```

Kontrollera repots status med `git status`.

```bash
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        hello.txt
nothing added to commit but untracked files present (use "git add" to track)
```

Git har nu upptäckt att du har skapat en ny fil som den inte känner till. Detta är en fil som inte finns i historiken och som inte är sparat i Git-repot. Denna fil är alltså **untracked**.

### Lägg till filen i Git

För att lägga till filen i Git, det vill säga att göra den till en **tracked** fil, så skriver du `git add <filnamn>`. Detta kommer att lägga till filen i Git-repot och den kommer att sparas i historiken.

```bash
git add hello.txt
```

Kontrollera sedan repots status.

```bash
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   hello.txt
```

Filen är nu tillagd i Git-repot och kommer att sparas i historiken. Filen är nu **tracked** och i **staged** tillståndet.

### Ta bort filen

Om du önskar ta bort filen för Git så kan du använda `git rm --cached <filnamn>`. Det gör att filen blir **untracked** igen. Detta är inte samma sak som att ta bort filen från din dator.

{%- hint "danger" -%}
Om du använder `git rm` utan `--cached` så tar du bort filen från din dator.
{%- endhint %}

### Ändringar

Om du gör fler ändringar i filen och kollar statusen så kommer du att se att filen är i **modified** tillståndet. Det betyder att du måste lägga till filen igen för att den ska hamna i **staged** tillståndet.

```bash
git add hello.txt
```

För att se ändringarna i filen så skriver du `git diff`. Detta kommer att skriva ut alla ändringar som gjorts i filen sedan den senaste committen.

```bash
git diff
```

### Commit

Filen i repot är nu i **staged** tillståndet. Det betyder att den kommer att sparas i historiken med nästa commit. Kommandot för att skapa en commit är `git commit`. Detta kommer att skapa en commit med alla filer som är i **staged** tillståndet.

`git commit` kommer att starta din texteditor och du kommer att kunna skriva en commit-meddelande. Commit-meddelandet är viktigt för att kunna förstå vad som har ändrats i filen.

Du behöver nu skriva ditt meddelande och spara filen / stänga texteditorn. Detta kommer att skapa en commit med filen.

En commit kan se ut så här:

```bash
[main (root-commit) 84e2186] Test
 1 file changed, 1 insertion(+)
 create mode 100644 hello.txt
```

Du kan också skriva din commit direkt i terminalen.

```bash
git commit -m "Meddelande"
```

Detta är enklare och snabbare än att använda texteditorn.

{%- hint "warning" -%}
Det är väldigt vanligt att det blir stor förvirring när `git commit` körs och textredigeraren öppnar en fil, särskilt om detta program är Vim. Så för enkelhetens skull, använd `git commit -m "Meddelande"`.
{%- endhint %}

{% endinstructions %}

{% questions %}

{% base %}

#### Uppgift 1

Förklara skillnaden mellan **untracked** och **tracked**?

{% endbase %}

{% endquestions %}
