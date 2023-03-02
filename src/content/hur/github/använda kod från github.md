---
title: Använda kod från GitHub
eleventyNavigation:
    key: använda kod från github
    parent: github
    order: 5
    excerpt: Ett repository är en katalog som innehåller alla filer för ett projekt.
---

{%- intro %}

Tidigare i materialet så klonade du ett repository som fanns på GitHub. Det var ett sätt att ladda ned koden. Men det gick då inte att göra några ändringar i koden eftersom du inte hade skrivbehörighet till det repot.

För att arbeta med kod från en annan användares repo så kan du göra en så kallad **fork** av det. En fork är en kopia av ett repository som du får skrivbehörighet till. Du kan sedan göra ändringar i din fork och om du önskar så kan du sedan skicka in en **pull request** till den ursprungliga användaren.
{% endintro %}

{%- instruktioner %}

Surfa till [övningsrepot på GitHub](https://github.com/NTIG-Umea/tod-github-prac) och klicka på **Fork** i högra hörnet. Den kommer då att ta dig till en dialog för att skapa en fork.

{% image "fork.png", "Skapa en fork av ett repository" %}

Fyll i formuläret och klicka på Create fork. GitHub kommer nu att göra en kopia av repot på ditt konto.

### Klona din fork

När GitHub har skapat din fork så kommer du att bli omdirigerad till din fork. Klicka på **Code** och kopiera urlen till repot. Öppna sedan terminalen och navigera till en katalog där du vill ha ditt repository. Skriv sedan in följande kommandon:

```bash
git clone <url>
```

Git kommer att klona repot till din dator. Navigera in i katalogen och öppna filen `README.md` i din favorit texteditor. Ändra något i filen och spara den.

### Pusha dina ändringar

När du har gjort ändringar i filen så kan du pusha dina ändringar till GitHub. För att göra det så skriver du följande kommandon:

```bash
git add README.md
git commit -m "Ändrade README.md"
git push
```

Git kommer nu att pusha dina ändringar till GitHub. Du kan nu öppna din fork på GitHub och se att filen har ändrats.

### Pull request till det ursprungliga repot

Om du vill att dina ändringar ska hamna i det ursprungliga repot så kan du skicka in en pull request. För att göra det så klickar du på **Pull requests** i menyn till vänster. Klicka sedan på **New pull request**.

Du får då upp en dialog där du kan se commits och vilka filer som ändrats. För att sedan skicka in en pull request så klickar du på **Create pull request**.

{% image "pullreq.png", "Skapa en pull request" %}

Den användare som äger det ursprungliga repot kommer nu att få en notis om att du har skickat in en pull request. Den kommer att kunna se vilka ändringar du har gjort och kan välja att godkänna eller avvisa din pull request.

### Synka din fork

Om det ursprungliga repot har ändrats sedan du gjorde din fork så kan du synka din fork med det ursprungliga repot. På sidan för ditt repository så finns det en notis om att du kan synkronisera ditt repository med det ursprungliga repot. GitHub kommer då att guida dig genom processen, men om du har gjort ändringar i filerna så kommer du att få konflikter. Du behöver då manuellt lösa konflikterna och välja vilka ändringar som ska behållas.

{% endinstruktioner %}
