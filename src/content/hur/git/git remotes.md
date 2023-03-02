---
title: Git remotes
eleventyNavigation:
    key: git remotes
    parent: git
    order: 5
    excerpt: Ett repository är en katalog som innehåller alla filer för ett projekt.
---

{%- intro %}

För att kunna använda GitHub med Git och för att kunna sammarbeta kring kod så behöver du förstå hur du kan använda remotes. En remote är en kopia av ditt repository som ligger på en server. Det kan vara en server som du har på din dator eller en server som du har på en tjänst som GitHub.

### Tänk på

-   En remote måste inte nödvändigtvis vara GitHub. Det kan vara en annan form av server eller Git-tjänst.

{% endintro %}

{%- instruktioner %}

Kommandot för att kontrollera om du har en remote är `git remote`. Det kommer att visa dig vilka remotes som finns för ditt repository.

För vårt testrepository så är det tomt, så för att arbeta med en remote så kommer vi att testa att klona ett repository från GitHub.

### Klona ett repository

För att klona ett repository från GitHub så behöver du en URL till det. För den här kursen finns det ett testrepository att använda.

I bash så behöver du gå till en katalog där du vill spara detta (kontrollera med `pwd`). Om du fortsätter så kan du skriva:

```bash
cd ..
pwd
```

För att klona ett repo så är kommandot `git clone <url> <katalog>`, där output katalogen är valfri. För att klona det här testrepo så skriver du:

```bash
git clone https://github.com/NTIG-Umea/tod-github-prac
```

Du kan nu `cd tod-github-prac` och se att du har en katalog med filerna i. Du kan också se att du har en remote med kommandot `git remote -v`.

{%- hint -%}
Eftersom du inte har skrivbehörighet till det här repot så kommer du inte kunna pusha till det (det vill säga spara din ändringar till det).
{%- endhint %}

### Lägg till en remote

För att lägga till en remote så behöver du en URL till den. Det kan vara en URL till en tjänst som GitHub eller en URL till en server som du har på din dator.

För att lägga till en remote så skriver du `git remote add <namn> <url>`. Där namnet är valfritt men praxis är att benämna den första remote som `origin`.

### En egen remote

Nästa steg är att använda en egen remote. Det kommer att introduceras i området om [GitHub](/hur/github/).

{% endinstruktioner %}
