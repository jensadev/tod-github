---
title: Skapa ett Git repo
eleventyNavigation:
    key: skapa ett git repo
    parent: git
    order: 0
    excerpt: Ett repository är en katalog som innehåller alla filer för ett projekt.
---

{% instructions %}

## Introduktion

*[repo]: Repository

Ett Git repo  är en katalog som innehåller alla filer för ett projekt. Det är en katalog som du behöver skapa och initiera för att Git ska kunna spåra ändringar i filerna.

## Instruktioner

För att arbeta med Git behöver du först skapa ett Git repo. Detta gör du genom att skapa en katalog och initiera den med Git. Skapa först en katalog och gå in i den.

```bash
mkdir <namn på katalog>
cd <namn på katalog>
```

Kommandot för att initiera katalogen som ett Git repo är `git init`. Detta kommando skapar en `.git` katalog i den aktuella katalogen. Detta är den katalog som Git använder för att spåra ändringar i filerna för repot i den aktuella katalogen.

```bash
git init
```

Filer och kataloger som börjar med `.` är dolda i Linux. Detta gäller även `.git` katalogen. För att se dolda filer och kataloger i Linux kan du använda kommandot `ls -la`.

{%- hint "varning" -%}
Generellt sett bör du inte ändra i `.git` katalogen. Om du gör det kan du förstöra ditt Git repo och du förlorar då all historik och ändringar.
{%- endhint %}

### Klona

Om du vill använda ett befintligt Git repo kan du använda kommandot `git clone` för att klona det. Detta kommer att skapa en katalog med samma namn som repot och kopiera in allt innehåll från repot i den nya katalogen.

```bash
git clone <repo url>
```

{% endinstructions %}
