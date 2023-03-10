---
title: Branches
eleventyNavigation:
    key: branches
    parent: arbetsflöde
    order: 0
    excerpt: Ett repository är en katalog som innehåller alla filer för ett projekt.
---

{% intro %}

Branches eller grenar på svenska är en viktig del av Git och GitHub. 

En branch är en parallell version av ditt repo, en kopia, där du kan göra ändringar utan att påverka ditt projekt. Du kan sedan välja att spara dina ändringar i din `main` branch eller kasta dem. Du kan likna det med att du gör en kopia av dokumentet du arbetar med för att sedan kunna göra ändringar utan att påverka det ursprungliga dokumentet.

{% endintro %}

{% instruktioner %}

Kommandot `git branch` används för att skapa en ny branch. För att bestämma vilken branch som är aktiv, där dina ändringar sparas så är kommandot `git checkout <branchnamn>`.

Skapa en ny branch `dev` och byt till den.
```bash
git branch dev
git checkout dev
```

{% endinstruktioner %}