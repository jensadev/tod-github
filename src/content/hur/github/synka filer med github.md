---
title: Synka filer med GitHub
eleventyNavigation:
    key: synka filer med github
    parent: github
    order: 2
    excerpt: För att synkronisera ditt lokala Git repo mot remote så behöver du kunna ladda ned ändringar från remote.
---

{% instructions %}

## Introduktion

För att synkronisera ditt lokala Git repo mot remote så behöver du kunna ladda ned ändringar från remote.

För att se vilka ändringar som är gjorda på remote så kan du först använda kommandot `git fetch`. Fetch kommer inte att skriva över dina lokala ändringar. Om du sedan önskar att faktiskt ladda ned ändringarna och skriva över eventuellt lokala ändringar så använder du kommandot `git pull`. Detta kommer att ladda ned alla ändringar från remote och lägga till dem i ditt lokala repo.

### Tänk på

- `pull` kan skriva över dina lokala ändringar

## Instruktioner

Du ska nu synkronisera ditt repository med din remote. Först ladda ned ändringarna och sedan ladda upp.

{%- hint "warning" -%}
Förhoppningsvis så har du inga ändringar i filerna som din **pull** eller **push** försöker skriva över och allt fungerar bra. Annars har du fått en konflikt som du måste lösa, mer om det i nästa del.
{%- endhint %}

### Hämta ändringar, pull

För att hämta de ändringar (du skapade en ny fil `README.md`) du har gjort på remote till ditt lokala repo så använder du kommandot `git fetch`.

Börja med att navigera till din lokala katalog för ditt repo. Kör sedan `git fetch` för att ladda ned ändringar från remote.

```bash
git fetch
```

Du får då information om att git hämtar remote. Kör sedan `git status` så ser du att du har en ny branch `origin/main` som är en kopia av `main` branchen på remote.

Du kan nu välja att applicera ändringarna från remote till ditt lokala repo.

{%- hint "danger" -%}
`pull` kan skriva över dina lokala ändringar om du inte har gjort en commit. Det räcker inte att filerna är sparade i din editor utan du måste göra en commit för att spara ändringarna i repot.
{%- endhint %}

```bash
git pull
```

När kommandot körs så kommer du att se en lista över alla filer som har ändrats.

Det går också att hoppa över `git fetch` och köra `git pull` direkt. Detta kommer att göra samma sak som att köra `git fetch` följt av `git pull`.

### Skicka ändringar, push

För att skicka ändringar från ditt lokala repo till remote så använder du kommandot `git push`.

Skapa en ny fil i ditt lokala repository. Lägg till den i staging area och skapa en commit. Kör sedan `git push` för att skicka ändringarna till remote.

```bash
echo "Fil att pusha" > push.txt
git add push.txt
git commit -m "feat: new file push.txt"
git push
```

{% endinstructions %}
