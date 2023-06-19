---
title: Branches
eleventyNavigation:
    key: branches
    parent: arbetsflöde
    order: 0
    excerpt: Branches, eller grenar är centralt i arbetsflödet för repos.
---

{% instructions %}

## Introduktion

Branches eller grenar på svenska är en viktig del av Git och GitHub. 

En branch är en parallell version av ditt repo, en kopia, där du kan göra ändringar utan att påverka ditt projekt. Du kan sedan välja att spara dina ändringar i din `main` branch eller kasta dem. Du kan likna det med att du gör en kopia av dokumentet du arbetar med för att sedan kunna göra ändringar utan att påverka det ursprungliga dokumentet.

## Instruktioner

Kommandot `git branch` används för att skapa en ny branch. För att bestämma vilken branch som är aktiv, där dina ändringar sparas så är kommandot `git checkout <branchnamn>`.


Använd ett repo och skapa en ny branch, kalla den `dev`, och byt sedan aktiv branch till `dev`.

```bash
git branch dev
git checkout dev
```

Du har nu en komplett historik av ditt repo i `main` branchen och en ny branch som heter `dev`. I `dev` kan du nu skapa ny commits som sparas i `dev` och detta påverkar inte `main`.

{% image "content/images/nybranch.svg", "Illustration, ny branch" %}

För att se vilka brancher som finns skriver du `git branch`.

```bash
git branch
```

Skapa en ny fil i `dev` och spara den. Byt sedan till `main` branchen och kontrollera att filen inte finns där.

```bash
git checkout dev
touch newfile.txt
git add newfile.txt
git commit -m "Added new file"
git checkout main
ls
```

När du är klar med en branch så är kommandot för att ta bort den `git branch -d <branchnamn>`.

{%- hint -%}
Det är viktigt att du kommer ihåg att spara dina ändringar i din branch innan du byter till en annan branch. Om du inte gör det så kommer du att förlora dina ändringar.
{%- endhint -%}

{% endinstructions %}