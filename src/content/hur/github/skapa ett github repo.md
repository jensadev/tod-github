---
title: Skapa ett GitHub repo
eleventyNavigation:
    key: skapa ett github repo
    parent: github
    order: 0
    excerpt: Ett repository är en katalog som innehåller alla filer för ett projekt.
---

{%- intro %}

Precis som för Git så är ett repository är en katalog som innehåller alla filer för ett projekt. Skillnaden är att du sparar ditt repository på GitHubs servrar.

För att arbeta mot GitHub så använder Git en [remote](hur/git/git-remotes/). Den remote som sparas på GitHub kallas för `origin`.

{% endintro %}

{%- instruktioner %}

{% image "newrepo.png", "Skapa ett repository på GitHub" %}{.float-right .w-30}

För att skapa ett repository på GitHub så behöver du vara inloggad på [GitHub](https://github.com/). Sök sedan reda på knappen New, eller hitta + tecknet på sidans navbar, där kan du skapa ett nytt repository.

Klicka på detta och du kommer att visas följande dialog:

{% image "newrepogithub.png", "Skapa ett repository på GitHub" %}

Fyll i namnet på ditt repository och en beskrivning. Du kan även välja om du vill att ditt repository ska vara privat eller publikt. Om du väljer att göra det publikt så kommer det att synas på din GitHub profil.

När du är klar så klickar du på Create repository. Du kommer då få upp instruktioner på hur du kan koppla ditt repository till ditt lokala repository.

{% image "githubcreatednew.png", "Ditt nya repository på GitHub" %}

### Koppla ditt lokala repository till GitHub

De instruktioner som du ska använda i det här fallet är de som står under "…or push an existing repository from the command line". Detta är för att du redan har ett repository som du vill koppla till GitHub.

Öppna terminalen och navigera till ditt `test` repository. Kopiera urlen till ditt repo. Skriv sedan in följande kommandon:

1. `git remote add origin <url>`, detta kopplar ditt lokala repository till en remote, GitHub.
2. `git branch -M main`, detta byter namn på din master branch till main (behövs inte om din branch redan är `main`).
3. `git push -u origin main`, detta laddar upp dina ändringar till GitHub, det kallas för pusha, `-u` flaggan sätter `origin` som default remote för din branch.

{% image "credmanager.png", "Autentisering mot GitHub" %}{.float-right .w-50}

När du kör det sista kommandot så kommer du med största sannolikhet få en förfrågan om autentisering mot GitHub. Välj att logga in med din webbläsare och följ instruktionerna. Du kommer då att få en ny dialog där du kan välja att spara dina inloggningsuppgifter i ditt operativsystem. Detta gör att du inte behöver logga in varje gång du pushar till GitHub.

Om allt fungerar som det ska så kommer du se att Git laddar upp dina ändringar till GitHub.

Du kan nu surfa till den url som du kopierade från GitHub och se att ditt repository finns där.

{% image "mynewrepo.png", "Ditt repository på GitHub" %}

{% endinstruktioner %}
