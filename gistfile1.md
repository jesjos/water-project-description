# Water: en ersättning för Fire, baserad på versionshantering

## Bakgrund:

Arbetsflöden som används på Chalmers bör spegla dem som används på hög nivå i branschen.
Där ingår modern versionhantering.
Fire-systemet för hantering av inlämningsuppgifter är undermåligt:

- Nya användaridentiteter för varje kurs
- Filuppladdningen fungerar dåligt, filer måste laddas upp en och en
- Ingen inbyggd validering
- Kommunikation mellan rättare och inlämnare fungerar dåligt

## Projektbeskrivning / Problembeskrivning

Uppgiften är att konstruera Water: ett system för hantering av inlämningsuppgifter 
som baserar sig på modern versionshantering. Water är en webbapplikation.
Systemets användargränssnitt är segmenterat för att hantera olika användares behov. Inlämning kan ske genom olika kanaler - till exempel direkt push till ett repositorie i systemet från versionshanteringsklienten, filuppladdning i webbläsare eller som bifogade filer i ett e-postmeddelande.
Även handledarna kan interagera på olika sätt med systemet.

Förslag på features:

- Inbyggd plagiatkontroll
- Handledare kan definiera valideringar för inlämningsuppgifterna. Till exempel kontrollera att en given radbredd inte överskrids. Inlämningar som inte klarar av valideringen kan nekas direkt. Sparar mycket handledartid.
- Readme-filer integrerade i systemet - en fil som uppfyller definitionen av en readme-fil renderas automatiskt på inlämningsuppgiftssidan

Systemet ska baseras på en befintlig öppen plattform. 
