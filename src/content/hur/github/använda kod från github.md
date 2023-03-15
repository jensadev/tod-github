---
title: Använda kod från GitHub
eleventyNavigation:
    key: använda kod från github
    parent: github
    order: 5
    excerpt: Ett stort användningsområde med GitHub är att kunna använda någon annas repo eller ladda ned kod.
---

{%- intro %}

*[url]: Uniform Resource Locator, en webbadress

Tidigare i materialet så klonade du ett repo från GitHub. Det var ett sätt att ladda ned koden. Men eftersom du saknade skrivbehörighet till repot så kunde du inte göra ändringar i det.

För att arbeta med kod från en annan användares repo så kan du göra en så kallad **fork** av det. En fork är en kopia av ett repo som du får skrivbehörighet till. Du kan sedan göra ändringar i din fork. Du kan även skicka in en så kallad **pull request** till den ursprungliga användaren för att föreslå att dina ändringar ska läggas till i deras repo.
{% endintro %}

{%- instruktioner %}

Surfa till [övningsrepot på GitHub](https://github.com/NTIG-Umea/tod-github-prac) och klicka på **Fork** i högra hörnet. Detta öppnar dialogen för att skapa en fork.

{% image "fork.png", "Skapa en fork av ett repository" %}

Fyll i formuläret och klicka på **Create fork**. GitHub skapar då en kopia av repot på ditt konto.

### Klona din fork

När GitHub har skapat din fork så kommer du att bli omdirigerad till din fork. Klicka på **Code** för att kopiera repots url. Öppna terminalen och navigera till en katalog där du vill spara repot lokalt.

Kommandot för att klona repot är:

```bash
git clone <url>
```

Kommandot gör att Git laddar ned repot och alla filerna som hör till det. När det är klart så kommer du att se en ny katalog med samma namn som repot.

### Pusha dina ändringar

Byt katalog till repots katalog och öppna filen `README.md`. Gör några ändringar i filen och spara den.

Nu ska du pusha dina ändringar till GitHub. Innan du pushar dina ändringar behöver du spara dem som en commit.

```bash
git add README.md
git commit -m "Ändrade README.md"
git push
```

Git laddar nu upp, pushar dina ändringar till GitHub. Du kan nu öppna din fork på GitHub och se att filen har ändrats.

### Pull request till det ursprungliga repot

Om du vill att dina ändringar ska läggas till i det ursprungliga repot så kan du skicka in en pull request till ägaren av repot. För att skapa en pull request så klickar du på **Pull requests** i menyn till vänster. Klicka sedan på **New pull request**.

Det tar dig till en dialog där du kan se dina commits och vilka filer som ändrats. För att skapa en pull request så klickar du på **Create pull request**.

{% image "pullreq.png", "Skapa en pull request" %}

Den användare som äger det ursprungliga repot kommer nu att få en notis om att du har skickat in en pull request. Hen kommer att kunna se vilka ändringar du har gjort och kan välja att godkänna eller avvisa dem.

### Synka din fork

Om det ursprungliga repot har ändrats efter att du skapade din fork så kan du synka din fork med det ursprungliga repot. På sidan för ditt repository så finns det en notis om att du kan synkronisera detta. GitHub kommer då att guida dig genom processen, men om du har gjort ändringar i filerna så kommer du att få konflikter. Du behöver då manuellt lösa konflikterna och välja vilka ändringar som ska behållas.

{% endinstruktioner %}
