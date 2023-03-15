---
title: Installera Git
eleventyNavigation:
    key: installera git
    parent: kom igång
    order: 1
    excerpt: För att använda Git så behöver du installera en klient.
---

{%- intro %}

Git är ett gratis och open source system för versionshantering. För att använda Git så behöver du installera en klient på din dator.

Git är släppt under [GPLv2](https://opensource.org/licenses/GPL-2.0)

{% endintro %}

{%- instruktioner %}

{% image "Git-Logo-2Color.png", "Git Logo" %}{".float-right w-50"}

Ladda ned Git-klienten för ditt operativsystem från [Git](https://git-scm.com/downloads).

Med Git-klienten kommer **Git-bash** och **Git-credential-manager**. Båda är program du kommer behöva för den här introduktionsguiden och för att använda Git.

När nedladdningen är klar starta installationen. Du kan med fördel välja att använda standard-inställningarna, du kryssar då i rutan **Only show new options**.

{% image "scm only new.png", "Installationsval för Git-scm" %}

Om du inte väljer detta så ställer installationsprogrammet ett stort antal frågor, här nedan finns det en liten hjälp för att komma igenom dessa.

1. Du behöver inte byta installations-plats för Git.
2. Du behöver inte ändra installations-egenskaperna.
3. För editor så välj ett program du är van att använda.
4. För branch, välj "Override" och "main". Detta är en nyare standard för GitHub.
5. För PATH, så välj "Git from the command line and also from 3rd-party software".
6. Du behöver inte ändra något för SSL och HTTPS.
7. Du behöver inte ändra på line endings.
8. **Viktigt** För terminal emulator så välj att använda MinTTY (instruktionerna på sidan kommer använda denna).
9. Du behöver inte ändra "default behaviour of `git pull`".
10. **Viktigt** Välj att installera Git Credential Manager (du behöver den senare när du använder GitHub).
11. Du behöver inte ändra "extra options" eller "experminental options".

Låt installationsprogrammet arbeta färdigt. Du kan sedan välja att starta Git-bash.

{%- hint -%}
Bash är ett skalprogram/kommandotolk som är vanlig i Unix/Linux miljö. Det är den terminal du kommer använda för att utforska Git.
{%- endhint %}

{% endinstruktioner %}
