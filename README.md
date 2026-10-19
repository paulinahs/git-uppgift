# Git-uppgift

## Fråga 1: Versionshantering vs vanliga filer

Versionshantering innebär att Git sparar olika versioner av ett projekt så att man kan följa alla förändringar som görs över tid. När man sparar med editorns vanliga sparaknapp uppdateras bara den aktuella filen på datorn. När man sparar med Git genom en commit skapas en permanent version som kan hittas och återställas senare.

Git sparar en tidslinje av frysta ögonblicksbilder, så kallade commits. Varje commit visar exakt hur projektet såg ut vid ett visst tillfälle. Att jag fortfarande kan öppna min första commit på GitHub och se alla tre TODO-kommentarer kvar i koden, trots att filen ser annorlunda ut idag, bevisar att Git sparar hela historiken och inte bara den senaste versionen av filen.

---

## Fråga 2: Arbetsytan, Staging och Commits

Kommandot `git status` används för att se vilka filer som har ändrats och vad Git känner av i projektet. Kommandot `git add` används för att lägga till ändringar i staging-området. Kommandot `git commit` används för att spara de stagade ändringarna som en ny version i projektets historik.

Man kan jämföra arbetsytan med ett papper på skrivbordet där jag gör mina ändringar. Staging fungerar som ett kuvert där jag väljer vilka ändringar som ska skickas vidare. En commit är som en arkivlåda där innehållet sparas permanent. Om jag ändrar en fil i editorn men försöker köra `git commit` utan att först köra `git add` får jag felmeddelandet `no changes added to commit`. Det beror på att Git bara kan skapa commits av sådant som finns i staging-området, alltså i "kuvertet".

---

## Fråga 3: Lådan hemma vs Montern på GitHub

Mappen på min dator innehåller de filer och commits som jag arbetar med lokalt. Repot på GitHub är en kopia av projektet på internet där historiken kan delas, granskas och säkerhetskopieras. Kommandot `git push` skickar mina lokala commits till GitHub.

Man kan tänka på den lokala Git-historiken och GitHub som två olika minnesytor. Den ena finns på min dator och den andra finns på GitHub. Om jag ändrar kod men glömmer att köra `git add` och `git commit` finns det inga nya commits att skicka upp till GitHub. Därför svarar `git push` med `Everything up-to-date`, eftersom GitHub redan har alla commits som finns sparade i den lokala historiken.