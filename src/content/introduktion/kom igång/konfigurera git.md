---
title: Konfigurera Git
eleventyNavigation:
    key: konfigurera git
    parent: kom igång
    order: 2
    excerpt: .
---

{%- intro %}

När du installerat färdigt Git så är du nästan redo att börja använda Git. Men för att arbeta med Git så behöver du ange ditt namn och din e-postadress. Det är för att kunna identifera vem som har arbetat med koden.

{% endintro %}

{%- instruktioner %}

För att konfigurera användainformationen i Git så behöver du starta **Git Bash** på din dator. När du har startat programmet så är det enklast att använda följande kommandon i terminalen för att spara dina uppgifter:

```bash
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
```

Använd samma uppgifter som du använde när du registrerade ditt konto på GitHub.

Om du vill redigera din konfiguration så kan du använda följande kommando, det öppnar en textfil i din textredigerare där du kan ändra dina uppgifter.

```bash
  git config --global --edit
```

{%- hint -%}
Om du inte har valt redigeringsprogram så använder Git Vim som redigeringsprogram. Vim är notoriskt svårt att använda.
{% endhint %}

För att redigera filen i Vim så behöver du följa dessa steg:

1. Tryck på `i` för att gå in i redigeringsläge.
2. Ändra dina uppgifter.
3. Tryck på `esc` för att gå ur redigeringsläge.
4. Tryck `:x` för att spara och avsluta.

Behöver du avbryta utan att spara så trycker du `:q!` istället.

{% endinstruktioner %}
