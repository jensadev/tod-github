---
title: Git historik
eleventyNavigation:
    key: git historik
    parent: git
    order: 2
    excerpt: Ett repository är en katalog som innehåller alla filer för ett projekt.
---

{%- intro %}

En av styrkorna med Git är att du får en historik över alla ändringar som gjorts i ditt projekt. Detta gör att du kan återgå till tidigare versioner av ditt projekt om du skulle behöva det.

Historiken sparas i ditt repo i form av commits, där varje commit är en version av ditt projekt. Det är alltså inte bara filerna som sparas utan även en beskrivning av vad som ändrats i filerna.

{% endintro %}

{%- instruktioner %}

Fortsätt arbeta på det repo du skapade i föregående moment. Du kan nu se en historik över alla ändringar som gjorts i ditt repo genom att skriva `git log`.

```bash
git log
```

### Fler commits, repetition

Prova att lägga till en eller flera filer samt ändra på befintliga filer. När du är klar så gör en commit.

Repetera kommandona och använd dem.

-   Redigera textfilen med nano, `nano hello.txt`, lägg till en rad med text.
-   Lägg till en ny fil, `touch newfile.txt`.

Lägg till filerna i **staging area** genom att skriva `git add <filnamn>`. Du kan lägga till flera filer genom att skriva `git add <filnamn1> <filnamn2>`.

Kontrollera sedan statusen för ditt repo genom att skriva `git status -s`. Detta kommer att skriva ut statusen för ditt repo på ett kortare sätt.

Gör sedan en commit genom att skriva `git commit -m "<meddelande>"`.

### Historik

Du kan nu se historiken för ditt repo genom att skriva `git log`. Detta kommer att skriva ut en lista med alla commits som gjorts i ditt repo.

{% endinstruktioner %}
