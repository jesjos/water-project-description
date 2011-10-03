# Water: en ersättning för Fire, baserad på versionshantering

## Bakgrund:

Arbetsflöden som används på Chalmers bör spegla dem som används på hög nivå i branschen.
Där ingår modern versionhantering. Genom att införliva versionhantering i arbetet med inlämningsuppgifter
läggs en stabil grund inför arbetslivet.
Därtill är Fire-systemet, det nuvarande systemet för hantering av inlämningsuppgifter, undermåligt av följande anledningar:

- Nya användaridentiteter för varje kurs
- Filuppladdningen fungerar dåligt, filer måste laddas upp en och en
- Ingen inbyggd validering
- Kommunikation mellan rättare och inlämnare fungerar dåligt
- Stelt användargränssnitt

## Projektbeskrivning / Problembeskrivning

Uppgiften är att konstruera Water: ett system för hantering av inlämningsuppgifter 
som baserar sig på modern versionshantering med git. 
Water är en webbapplikation.
Systemet består av en backend som bland annat hanterar git-repositorier samt en frontend som presenterar repositorierna och möjliggör inlämning och rättning och uppgifterna.
Systemets användargränssnitt är segmenterat för att hantera olika användares behov. Inlämning kan ske genom olika kanaler - till exempel direkt push till ett repositorie i systemet från versionshanteringsklienten, filuppladdning i webbläsare eller som bifogade filer i ett e-postmeddelande.
Även handledarna kan interagera på olika sätt med systemet.


Förslag på features:

- Inbyggd plagiatkontroll
- Kursansvarig kan definiera valideringar för inlämningsuppgifterna. Till exempel kontrollera att en given radbredd inte överskrids. Inlämningar som inte klarar av valideringen kan nekas direkt. Sparar mycket handledartid.
- Readme-filer integrerade i systemet - en fil som uppfyller definitionen av en readme-fil renderas automatiskt på inlämningsuppgiftssidan

Systemet ska baseras på en befintlig öppen plattform. 
