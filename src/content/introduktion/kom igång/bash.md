---
title: Bash
eleventyNavigation:
    key: bash
    parent: kom igång
    order: 3
    excerpt: Bash är en kommandotolk till Linux.
---

{% intro %}

Bash är en kommandotolk till Linux. Det är en textbaserad gränssnitt som används för att kommunicera med datorn. Bash är en av de vanligaste kommandotolken för Linux.

För att köra den här kursen och använda dig av Git så underlättar det om du har lite grundläggande kunskap om hur du navigerar i filsystemet med bash.

{% endintro %}

{% instruktioner %}

Det här avsnittet förutsätter att du har tillgång till Bash eller liknande. Har du följt instruktionerna, [Installera Git](introduktion/kom-igang/installera-git/), så har du sannolikt installerat Git-Bash.

Så för att testa det här behöver du starta Git-Bash.
När du startar Git-Bash så kommer du se en prompt som ser ut ungefär så här:

{% image "gitbashmingw.png", "Git Bash" %}

Nu kan du prova att navigera i filsystemet. För att göra det så behöver du använda kommandot `cd` (change directory). För att navigera till din hemkatalog så skriver du:

```bash
cd ~
```

Prova att skapa en katalog med namnet `test`, kommandot för att skapa en katalog är `mkdir` (make directory).

```bash
mkdir test
```

Prova att navigera till den nya katalogen med `cd`. För att se vilka filer och kataloger som finns i den katalogen så kan du använda kommandot `ls` (list).

Kontrolla att du är i mappen test genom att skriva `pwd` (print working directory). Nu kan du skapa en fil med namnet `test.txt` med kommandot `touch`.

```bash
touch test.txt
```

Om du har följt instruktionerna har du en katalog som heter `test` med en fil som heter `test.txt` i den katalogen.

{% image "cmds.png", "Exempelkommandon i bash" %}

Nu kan du ta bort katalogen `test` med kommandot `rm` (remove). För att ta bort en katalog så behöver du använda flaggan `-r` (recursive).

Men innan du kan göra detta så behöver du gå upp ett steg i katalogstrukturen med `cd ..`. Sedan kör du:

```bash
rm -r test
```

{% endinstruktioner %}

{% uppgifter %}

{% bas %}

#### Uppgift 1

{% endbas %}

{% enduppgifter %}