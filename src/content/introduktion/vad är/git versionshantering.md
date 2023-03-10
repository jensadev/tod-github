---
title: Git versionshantering
eleventyNavigation:
    key: git versionshantering
    parent: vad är
    order: 1
    excerpt: Git är ett system för versionshantering.
---

{%- intro %}

*[repo]: Repository

Git är ett versionshanteringssystem som används för att spara och hantera ändringar i filer. Git systematiserar hela arbetsflödet med att spara ändringar och skapa en historik över dokuments tidigare innehåll. Git gör det i något som kallas för **repositories** eller **repos**. Ett repo är en katalog som innehåller ditt projekt. Git är ett så kallat distribuerat versionshanteringssystem, vilket betyder att varje kopia av ett repo är en fullständig kopia av hela historiken. Detta gör att du kan arbeta på projektet lokalt och sedan synka med andra kopior av samma repo.

### Tänk på

-   Ett repository är en katalog som innehåller alla filer för ett projekt, tillsammans med dess historik.
-   Git körs lokalt, så för att köra Git behöver du inte vara ansluten till internet eller registrera ett konto.

{% endintro %}

{%- instruktioner %}

När du använder Git så behöver du köra vissa kommandon för att spara filernas ändringar, så kallade commits. När du gör en commit så sparar Git en snapshot av filerna i ditt repository, deras nuvarande tillstånd.

Så för att använda illustrationen från föregående förklaring så får varje steg nu en commit. Varje commit innehåller nu en komplett historik över dina filer.

{% image "commits.svg", "Illustration av versionshantering" %}

### Tre tillstånd (states)

Git har tre stycken tillstånd för filerna i ett repo. Detta är:

1. **Modified**, filen är ändrad men inte sparad i Git-historiken.
2. **Staged**, filen är ändrad och kommer att sparas i Git-historiken med nästa commit.
3. **Committed**, filen är sparad i Git-historiken.

### Mer läsning

[Git](https://git-scm.com/) skapades av [Linus Torvalds](https://sv.wikipedia.org/wiki/Linus_Torvalds), skaparen av [Linux](<https://sv.wikipedia.org/wiki/Linux_(k%C3%A4rna)>), för att hantera källkoden till Linux.

Git är i grunden terminalbaserat. Men det går att köra Git genom de flesta utvecklingsmiljöer ([IDE](https://sv.wikipedia.org/wiki/Integrerad_utvecklingsmilj%C3%B6)). Det finns ett flertal olika klienter för att arbeta med Git, bland annat Git-scm och GitHub.

{% endinstruktioner %}

{% uppgifter %}

{% bas %}

#### Uppgift 1

Vilka tre tillstånd har filerna i ett Git-repo?

{% endbas %}

{% enduppgifter %}
