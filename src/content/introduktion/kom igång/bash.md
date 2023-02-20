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

Starta Git Bash eller ett annat terminalprogram.
När du startar Git Bash så kommer du se en prompt som ser ut ungefär så här:

{% image "gitbashmingw.png", "Git Bash" %}

Nu kan du navigera i filsystemet. För att göra det så behöver du använda kommandot `cd` (change directory) följt av vilken katalog du vill byta till. För att navigera till din hemkatalog så skriver du:

```bash
cd ~
```

Skapa en katalog med namnet `test`, kommandot för att skapa en katalog är `mkdir` (make directory) följt av namnet på katalogen.

```bash
mkdir test
```

För att byta från din nuvarande katalog till katalogen test som du skapade behöver du använda `cd test`. För att se vilka filer och kataloger som finns i den katalog du befinner dig i så kan du använda kommandot `ls` (list).

Kontrolla att du är i mappen test genom att skriva `pwd` (print working directory). Programmet skriver då ut den fullständiga sökvägen till den katalog du befinner dig i.

Skapa sedan en fil med namnet `test.txt`, för att göra det använd dig av kommandot `touch`. `touch` skapar en tom fil.

```bash
touch test.txt
```

Om du har följt instruktionerna har du nu en katalog som heter `test` med en fil som heter `test.txt` i den katalogen. Kontrollera detta med `ls`.

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
