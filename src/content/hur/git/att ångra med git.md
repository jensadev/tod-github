---
title: Att ångra med git
eleventyNavigation:
    key: att ångra med git
    parent: git
    order: 4
    excerpt: För att arbeta med historiken i Git så behöver du veta hur du kan ångra ändringar.
---

{% instructions %}

## Introduktion

Att ångra ändringar i ditt projekt är något som kommer att hända förr eller senare. Det är därför viktigt att veta hur du kan ångra ändringar i Git.

### Tänk på

-   Det är viktigt att tänka på att du inte kan ångra en commit som du har pushat till en remote.
-   Att ändra eller återställa filer kan leda till att du förlorar ändringar som du inte har committat.

## Instruktioner

Fortsätt att arbeta på det repo du skapade i föregående moment.

### Om du glömde något i din senaste commit

Öppna filen `hello.txt` och lägg till en rad med text, du glömde skriva den innan du gjorde din senaste commit. Lägg sedan till filen i **staging area** genom att skriva `git add hello.txt`.

Du kan nu lägga till den i din senaste commit genom att skriva `git commit --amend`. Detta kommer att öppna din texteditor och låta dig redigera ditt senaste commit meddelande. Spara sedan filen och stäng texteditorn och Git kommer att uppdatera din senaste commit med den nya filen.

{%- hint "warning" -%}
Använd bara `git commit --amend` om du inte har pushat din senaste commit till en remote.
{%- endhint %}

### Ta bort ändringar från staging area

Redigera filen `hello.txt` och ta bort den rad med text du la till tidigare. Skapa sedan en ny fil, `touch remfile.txt`. Lägg sedan till båda filerna i **staging area** genom att skriva `git add *`.

Om du nu kör `git status` så kommer du att se att båda filerna är i **staging area**. Git ger dig nu instruktioner om hur du kan ta bort filer från **staging area**.

Du kan ångra ändringar med `git restore --staged <filnamn>`. Detta kommer att ta bort filen från **staging area**. Git visar det genom att skriva ut att följande ändringar inte är `staged for commit`.

Det går även att återställa filen till den senaste versionen genom att skriva `git restore <filnamn>`.

{% endinstructions %}
