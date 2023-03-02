---
title: Bash kommandon
eleventyNavigation:
    key: bash kommandon
    parent: kom igång
    order: 4
    excerpt: Här hittar du några vanliga bash kommandon.
---

{%- intro %}

Den här sidan försöker inte vara någon utförlig guide till Bash, men det kan vara bra att känna till lite fler kommandon. Det så att du kan navigera, skapa och ta bort filer och kataloger.

{% endintro %}

{%- instruktioner %}

Här nedan hittar du ett antal kommandon för att navigera och manipulera filer.

{%hint %}
Kom ihåg att du nästan alltid kan köra ett kommandon med `--help` för att få mer information om det.
{% endhint %}

| Kommando                       | Beskrivning                                                                                                                     |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| `ls`                           | Listar innehållet i en katalog, `-la` för att se allt                                                                           |
| `cd <katalog>`                 | Går till en annan katalog, enbart `cd` tar dig till `/home/<user>`                                                              |
| `mkdir <katalog>`              | Skapar en ny katalog                                                                                                            |
| `touch <filnamn>`              | Skapar en fil                                                                                                                   |
| `rm <filnamn>`, `rm <katalog>` | Tar bort en fil, ska du ta bort en katalog lägg till `-r`, recursive. Innehåller katalogen filer kan du behöva `-rf` för force. |
| `cp <filnamn> <destination>`   | Kopierar en fil till angiven destination                                                                                        |
| `mv <filnamn> <destination>`   | Flyttar en fil till angiven destination                                                                                         |
| `cat <filnamn>`                | Läser en fil och skriver ut den i terminalen                                                                                    |
| `history`                      | Listar din kommando-historik, du kan seadan köra kommandot från historiken med `!nummer`                                        |

### Navigera i filsystemet

För att navigera i filsystemet så kan du använda dig av kommandot `cd`. Detta kommando tar dig till en annan katalog. En viktig del att förstå i detta är att alla kataloger innehåller `.`, som representerar den katalogen du befinner dig i och `..`, vilket representerar den katalogen som ligger ovanför den du befinner dig i.

Så för att referera till nuvarande katalog så använder du dig av `.`. Det är viktigt att känna till när du till exempel ska kopiera eller flytta filer.

Så för att kopiera en fil från mappen `test` till den nuvarande katalogen så skriver du:

```bash
cp test/<filnamn> .
```

### Redigera textfiler

För att redigera textfiler så kan du använda dig av kommandot `nano`. Det är ett enkelt textredigeringsprogram som är enkelt att använda.

```bash
nano <filnamn>
```

### Superuser

Vissa kommandon i Linux kräver att du kör dem med superuser-rättigheter. Det gör du genom att skriva `sudo` följt av kommandot du vill köra. Det kommer att be dig om ditt lösenord och sedan köra kommandot.

{%- hint -%}
Var försiktig med att köra kommandon med `sudo`, det kan leda till att du skadar din dator.
{% endhint %}

```bash
sudo <kommando>
```

{% endinstruktioner %}
