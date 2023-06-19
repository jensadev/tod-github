---
title: Konflikter
eleventyNavigation:
    key: konflikter
    parent: github
    order: 3
    excerpt: När historiken mellan lokalt och remote inte stämmer uppstår en konflikt. 
---

{% instructions %}

## Introduktion

Konflikter är oundvikliga när du arbetar med Git och GitHub, förr eller senare kommer det att ske. Med en konflikt menas att du har ändringar i en eller flera filer på remote och lokalt som inte är synkroniserade. När du får en konflikt så måste du lösa den genom att berätta för Git vilken ändring du vill behålla.

{%- hint -%}
En inte helt ovanlig lösning på konflikter är att användaren kopierar de lokala filerna till en annan plats, tar bort hela repo katalogen och klonar ner repot igen för att sedan kopiera in ändringarna. Det är dock inte en bra lösning då du förlorar historiken för ditt repository.
{%- endhint %}

## Instruktioner

Du ska nu skapa en konflikt för att sedan lösa den med hjälp av Git och GitHub.

### Skapa en konflikt

För att skapa en konflikt ska du göra en ändring i en fil på remote och sedan göra en ändring i samma fil i ditt lokala repo.

1. Skapa en ny fil i ditt lokala repo på din dator. Lägg till den i staging area och gör en commit. Kör sedan `git push` för att skicka ändringarna till remote.

```bash
echo "konflikter är till för att lösas" > konflikt.txt
git add konflikt.txt
git commit -m "feat: new file konflikt.txt"
git push
```

2. Surfa till ditt repo på GitHub och redigera filen `konflikt.txt` genom att lägga till en rad med text. Klicka sedan på `Commit changes`. **Du har nu en remote commit som du inte har i ditt lokala repo**.

3. Byt till ditt lokala repo och redigera filen `konflikt.txt` genom att lägga till en rad med text. Kör `git add konflikt.txt` för att lägga till filen i staging area följt av `git commit -m "refactor: konflikt.txt"` för att göra en commit. **Du har nu en lokal commit som du inte har på remote**.

4. Kör `git pull` för att försöka hämta ner ändringarna från remote. Du kommer då få en konflikt.

```bash
Auto-merging konflikt.txt
CONFLICT (content): Merge conflict in konflikt.txt
Automatic merge failed; fix conflicts and then commit the result.
```

Använd `git status` för att få information om var filen som har konflikten finns.

{%- hint -%}
Om dina lokala ändringar inte är **staged** och **committed** så får du följande felmeddelande.
{%- endhint %}

```bash
error: Your local changes to the following files would be overwritten by merge:
        konflikt.txt
Please commit your changes or stash them before you merge.
Aborting
```

### Lösa konflikten

För att lösa konflikten är det viktigt att förstå hur Git fungerar och vad det är som sker. Git har två olika commits som den försöker slå ihop, en lokala och en remote. Tillsammans är dessa commits som skapar konflikten eftersom Git inte kan bestämma vilka ändringar som ska behållas. För att lösa konflikten måste du berätta för Git vilka ändringar du vill behålla.

Kör `git status` så kommer du att se att du har en fil som är `both modified`. Detta betyder att du har ändringar i filen både på remote och lokalt.

Öppna filen `konflikt.txt` i din texteditor och du kommer att se att filen ser ut ungefär så här.

```bash
konflikter är till för att lösas

<<<<<<< HEAD
Detta är en lokal ändring.
=======
Detta är en remote ändring.
>>>>>>> 2e08f07dff38fd2e40f4549b575195c0a1596db4
```

Git har lagt till `<<<<<<< HEAD`, `=======` och `>>>>>>>` för att du ska kunna identifiera var ändringarna börjar och slutar.

Redigera filen och ta bort allt utom den ändring du vill behålla (inklusive Gits markeringar). Du kan välja att behålla den lokala , remote eller en kombination av båda. För att behålla den lokala ändringen.

```bash
konflikter är till för att lösas

Detta är en lokal ändring.
```

Redigera och spara filen. Om du har flera konflikter så behöver du göra detta för varje fil. När du är klar så lägger du till filen i staging area och skapar en commit.

```bash
git add konflikt.txt
git commit -m "refactor: resolved conflict konflikt.txt"
git push
```

Grattis, du har nu löst konflikten och kan fortsätta arbeta med ditt projekt.

{% endinstructions %}
