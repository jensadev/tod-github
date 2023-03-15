---
title: Git remotes
eleventyNavigation:
    key: git remotes
    parent: git
    order: 5
    excerpt: Git körs lokalt på din dator. För att koppla Git till en server så behöver du en remote. En remote är en kopia av ditt repo som ligger på en server, som GitHub.
---

{%- intro %}

*[repo]: Repository
*[klona]: Spara en kopia av

För att kunna använda GitHub med Git och för att kunna sammarbeta kring kod så behöver du förstå hur du kan använda remotes. En remote är en kopia av ditt repo som ligger på en server. Det kan vara en server som du har på din dator eller en server som du har på en tjänst som GitHub.

### Tänk på

-   En remote måste inte nödvändigtvis vara GitHub. Det kan vara en annan form av server eller Git-tjänst.

{% endintro %}

{%- instruktioner %}

Kommandot för att kontrollera om du har en remote är `git remote`. Det kommer att visa dig vilka remotes som finns för ditt repo.

För det repo som du har arbetat med, `test`, så är det såklart tomt. För att prova arbeta med en remote kommer du klona ett repo från GitHub.

### Klona ett repository

För att klona ett repo från GitHub så behöver du en URL till det. För den här kursen finns det ett testrepo att använda.

I bash så behöver du gå till en katalog där du vill spara detta (kontrollera med `pwd`). Om du fortsätter så kan du skriva:

```bash
cd ..
pwd
```

Kommandot för att klona ett repo är: `git clone <url> <output>`, där output-katalogen är valfri. 

För att klona test-repot för kursen skriver du:

```bash
git clone https://github.com/NTIG-Umea/tod-github-prac
```

Du kan nu använda `cd tod-github-prac` för att byta till den nya katalogen. Du kan också kontrollera att repot har en remote med kommandot `git remote -v`.

{%- hint -%}
Eftersom du inte har skrivbehörighet till det här repot så kommer du inte kunna pusha till det (det vill säga spara din ändringar till det).
{%- endhint %}

### Lägg till en remote

För att lägga till en remote så behöver du en URL till den. Det kan vara en URL till en tjänst som GitHub eller en URL till en server som du har på din dator.

För att lägga till en remote så skriver du `git remote add <namn> <url>`. Där namn är valfritt men praxis är att benämna den första remote som `origin`.

### En egen remote

Nästa steg är att använda en egen remote. Det kommer att introduceras i området om [GitHub](/hur/github/).

{% endinstruktioner %}
