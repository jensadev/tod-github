# köra git config och annat

Kör från home

```bash
cd ~
```

Skapa en ny mapp

```bash
mkdir test
```

Gå in i mappen

```bash
cd test
```

Kör git init för att det ska bli en git mapp

```bash
git init
```

Skapa en fil

```bash
touch readme.md
```

Kolla status

```bash
git status
```

Lägg till filen

```bash
git add readme.md
```

Kolla status

```bash
git status
```

Commita filen

```bash
git commit -m "first commit"
```

Nu blir det fel eftersom det saknas viss konfiguration kring din identitet.

För att ange och redigera identiten så kan du köra

```bash
git config --global --edit
```

Detta öppnar redigeringsprogrammet i bash och du kan redigera filen. Problemet är att detta redigersprogrammet är vim och det är inte så lätt att använda.

Så för att ändra till nano

```bash
git config --global core.editor "nano"
```

Nu kan du köra

```bash
git config --global --edit
```

och redigera filen med nano. Ta bort kommentarerna och lägg till dina egna värden.

```bash
[user]
    name = Ditt namn
    email = Din email
```

Spara sedan filen med `CTRL+O` och avsluta med `CTRL+X`

eller så går detta konfigurera direkt i bash med

```bash
git config --global user.name "Ditt namn"
git config --global user.email "Din email"
```

Med dina credentails sparade så kan du nu göra en commit igen

```bash
git commit -m "first commit"
```

Kolla status

```bash
git status
```

Nu är filen committad. För att pusha filen till GitHub så behöver vi först lägga till en remote. Dvs. berätta för Git att vi vill pusha till GitHub och till vilket repo.

Kommandot för detta är:

```bash
git remote add origin URL
```

URL hittar du på GitHub när du skapar ett nytt repo.
Så surfa till GIThub och skapa ett nytt repo.

Det ser ut ungefär så här.
newgithubrepoimg

Välj new repository och fyll i namnet på ditt repo och klicka på create repository.

Om du har skapat ett tomt repo så ger github dig all kod för att initera det. Eftersom vi redan har gjort det så behöver vi bara kopiera URL:en.

```bash
git remote add origin URL
```

Nu kan vi pusha filen till GitHub

```bash
git push -u origin main
```

Detta kommer att fråga om dina GitHub credentials. Så skriv in ditt användarnamn och lösenord.

```bash
echo "# testtest" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/jensnti/testtest.git
git push -u origin main
```

```bash
history
22 git log
23 git diff
24 echo "# hej" > readme.md
25 git add readme.md
26 git diff
27 git r readme.md
28 git diff --staged
29 git commit -m"update"
30 git log
31 git status
```
