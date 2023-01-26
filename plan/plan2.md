# create a project

Hur sparas filerna / spara filerna i repot.

Git workflow and the 3 state model?

bash / git commands

folder mapp directory ~= git repo

Snapshot of all files at a given time

mkdir (make directory) för att skapa ny mapp

cd mappnamn (change directory) för att byta mapp

ls (list) för att lista filer i mappen

git init för att initializera ett repo i mappen
### VISA HUR EN GÖR DETTA I  VSCODE OCKSÅ

git filerna är dolda 

ls -la för att visa dolda filer

- working directory
    - make changes to files
- staging area
- repository


## working dir

show how it works, create a file, change it, save it
README.md 
touch README.md för att skapa filen

git status för att se status

git vet att filen finns men ändringarna är ännu inte sparade

För att sparar ändringar så behöver vi lägga till filen i staging area
För att lägga till filen i staging area så använder vi git add

git add README.md

git status för att se status

Filen är nu sparad i git och vi kan se att den är i staging area och dess nuvarande form är redo för att bli committad till repository

Sista steget är att committa filen till repository. Då sparar vi den i git och den är nu sparad i historiken.
Commit = snapshot av filen i ett givet tillstånd

git commit -m "add README.md" för att committa filen, detta måste ske med ett meddelande som beskriver vad som har ändrats

git status för att se status

git log för att se historiken

