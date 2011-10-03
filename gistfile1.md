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
Systemets användargränssnitt är segmenterat för att hantera olika användares behov. Inlämning kan ske genom olika kanaler - till exempel direkt push till ett repositorie i systemet från versionshanteringsklienten, filuppladdning i webbläsare eller som bifogade filer i ett e-postmeddelande.
Även handledarna kan interagera på olika sätt med systemet.

Systemet består av en backend som bland annat hanterar git-repositorier samt en frontend som presenterar repositorierna och möjliggör inlämning och rättning och uppgifterna. Backenden tar emot inlämningarna via git, mail eller andra kanaler och placerar dem i någon form av köhanterare som behandlar informationen och presenterar på den frontenden.

## Förslag på features:

- Modern versionshantering för avancerade användare (akademiker/ingenjörer)
- Flexibel definition av uppgifter
  - Möjligt att definiera delmål som godkänns separat
- Enkel översikt mellan första inlämning och retur
- Kommentarer knutna till specifika rader i koden
  - Tvåvägskommunikation möjlig - kommentarer på kommentarer.
- Inbyggd plagiatkontroll
- Statistik - t.ex:
  - Programspråksanvändning
  - Antal kodrader
  - Andel godkända samt antal försök
  - Olika studenters andel av kodbasen inom en grupp
  - Kursansvarig kan se hur många inlämningar som är avklarade
- Deadline för handledare
- Progressbar för rättningen
  - Det går att se hur många grupper som har fått sin uppgift rättad
  - Studenter ser hur många som ligger före i rättningskön.
- Kursansvarig kan definiera automatiska valideringar för inlämningsuppgifterna
  - Möjlighet att validera en given radbredd inte är överskrids
  - Automatisk körning av fördefinierade unittester.
  - Inlämningar som inte klarar av valideringen kan nekas direkt. Sparar mycket handledartid.
- Readme-filer integrerade i systemet - en fil som uppfyller definitionen av en readme-fil renderas automatiskt på inlämningsuppgiftssidan
- Online-editering - små 
- Bestämd rättningsordning för handledarna
  - En retur på labb 1 ska rattas före en förstainlamning på labb 2.
- Möjlighet till anonym gransking av labbarna, på samma vis som tentarättningen.

Systemet ska baseras på en befintlig öppen plattform. 
