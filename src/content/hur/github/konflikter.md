---
title: Konflikter
eleventyNavigation:
    key: konflikter
    parent: github
    order: 3
    excerpt: Ett repository är en katalog som innehåller alla filer för ett projekt.
---

{%- intro %}

Konflikter är oundvikliga när du arbetar med Git och GitHub, förr eller senare kommer det att ske. Med en konflikt menas att du har ändringar i en fil både på remote och lokalt. När du får en konflikt så måste du lösa den genom att berätta för GitHub vilken ändring du vill behålla.

En inte helt ovanlig lösning på konflikter är att användaren kopierar de lokala filerna till en annan plats, tar bort hela repo katalogen och klonar ner repot igen för att sedan kopiera in ändringarna. Det är dock inte en bra lösning då du förlorar historiken för ditt repository.

{% endintro %}

{%- instruktioner %}

Du ska nu få skapa en konflikt för att sedan lösa den med hjälp av Git och GitHub.

### Skapa en konflikt

Du ska nu skapa en konflikt genom att göra en ändring i en fil på remote och sedan göra en ändring i samma fil på ditt lokala repository.

1. Skapa en ny fil i ditt lokala repository. Lägg till den i staging area och gör en commit. Kör sedan `git push` för att skicka ändringarna till remote.

```bash
echo "konflikter är till för att lösas" > konflikt.txt
git add konflikt.txt
git commit -m "Bäddar för konflikt"
git push
```

2. Gå till GitHub och redigera filen `konflikt.txt` genom att lägga till en rad med text. Klicka sedan på `Commit changes`. Du har nu en remote commit som du inte har i ditt lokala repository.

3. Gå tillbaka till ditt lokala repository och redigera filen `konflikt.txt` genom att lägga till en rad med text. Kör sedan `git add konflikt.txt` för att lägga till filen i staging area följt av `git commit -m "Konflikten är skapad"` för att göra en commit.

4. Kör sedan `git pull` för att försöka hämta ner ändringarna från remote. Du kommer då få en konflikt.

```bash
Auto-merging konflikt.txt
CONFLICT (content): Merge conflict in konflikt.txt
Automatic merge failed; fix conflicts and then commit the result.
```

Du kan nu köra `git status` för att se vad som har hänt.

Om du inte hade stagat och committat dina ändringar så hade du fått följande felmeddelande.

```bash
error: Your local changes to the following files would be overwritten by merge:
        konflikt.txt
Please commit your changes or stash them before you merge.
Aborting
```

### Lösa konflikten

För att lösa konflikten är det viktigt att förstå hur Git fungerar och vad det är som sker. Git har två olika commits som den försöker slå ihop, den lokala och den remote. Det är dessa två commits som skapar konflikten. För att lösa konflikten måste du berätta för Git vilken av de två commits som du vill behålla.

Om du kör `git status` så kommer du att se att du har en fil som är `both modified`. Detta betyder att du har ändringar i filen både på remote och lokalt.

Öppna nu filen `konflikt.txt` i din favorit texteditor och du kommer att se att filen ser ut ungefär så här.

```bash
konflikter är till för att lösas

<<<<<<< HEAD
Detta är en lokal ändring.
=======
Detta är en remote ändring.
>>>>>>> 2e08f07dff38fd2e40f4549b575195c0a1596db4
```

Du behöver nu redigera filen och ta bort allt utom den ändring du vill behålla. Du kan välja att behålla den lokala ändringen, remote ändringen eller en kombination av båda. I detta fall så vill vi behålla den lokala ändringen.

```bash
konflikter är till för att lösas

Detta är en lokal ändring.
```

Redigera filen och spara. Om du har flera konflikter så behöver du göra detta för varje fil. När du är klar så kan du lägga till filen i staging area och göra en commit.

```bash
git add konflikt.txt
git commit -m "Konflikten är löst"
git push
```

Grattis, du har nu löst konflikten och kan fortsätta arbeta med ditt projekt.

{% endinstruktioner %}
