---
title: Skapa ett GitHub repo
eleventyNavigation:
    key: skapa ett github repo
    parent: github
    order: 0
    excerpt: Ett repository är en katalog som innehåller alla filer för ett projekt.
---

{%- intro %}

*[repo]: Repository
*[url]: Uniform Resource Locator, en webbadress

Precis som för Git så är ett repo är en katalog som innehåller alla filer för ett projekt. Skillnaden är att du sparar ditt repo på GitHubs servrar.

För att arbeta mot GitHub så använder Git en [remote](hur/git/git-remotes/). 

### Tänk på
- Ett repos första remote bör alltid vara `origin`.

{% endintro %}

{%- instruktioner %}

För att skapa ett repo på GitHub så behöver du vara inloggad på [GitHub](https://github.com/). Sök sedan reda på knappen **New**, eller hitta **+** tecknet på sidans navbar, där kan du skapa ett nytt repo.

Klicka på detta och du kommer att visas följande dialog:

{% image "newrepogithub.png", "Skapa ett repo på GitHub" %}

Fyll i namnet på ditt repo och en beskrivning. Du kan även välja om du vill att ditt repo ska vara privat eller publikt. Om du väljer att göra det publikt så kommer det att synas på din GitHub profil.

När du är klar så klickar du på **Create repository**. Du kommer då få upp instruktioner på hur du kan koppla ditt GitHub-repo till ditt lokala repo.

{% image "githubcreatednew.png", "Ditt nya repo på GitHub" %}

### Koppla ditt lokala repo till GitHub

När du ska koppla en remote till ett lokalt repo ska du använda de kommandon som går att läsa under  **…or push an existing repo from the command line**. 

Öppna terminalen och navigera till ditt `test` repo. Kopiera repots url till ditt repo. Skriv sedan in följande kommandon:

1. `git remote add origin <url>`, för att koppla ditt lokala repo till en remote, GitHub.
2. `git branch -M main`, för att byta namn på din master branch till main (behövs inte om ditt branch-namn redan är `main`).
3. `git push -u origin main`, detta laddar upp dina ändringar till GitHub, det kallas för pusha, `-u` flaggan sätter `origin` som default remote för din branch.

{% image "credmanager.png", "Autentisering mot GitHub" %}{.float-right .w-50}

När du kör det sista kommandot bör du få upp en dialog för att autentisera mot GitHub. Detta är **Git-credential-manager** du installerade tidigare med [Git-scm](/introduktion/kom-igang/installera-git/). 

Logga in med din webbläsare (Sign in with your browser) och följ instruktionerna. Du bör då få en ny dialog där du kan välja att spara dina inloggningsuppgifter i ditt operativsystem. Detta gör att du inte behöver logga in varje gång du pushar till GitHub.

Om allt fungerar som det ska så kommer du se att Git laddar upp dina ändringar till GitHub. Du kan nu surfa till den url som du kopierade från GitHub och se att ditt repo finns där.

{% image "mynewrepo.png", "Ditt repo på GitHub" %}

{% endinstruktioner %}
