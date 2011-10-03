# Water: en ersättning för Fire, baserad på versionshantering

## Bakgrund:

Arbetsflöden som används på Chalmers bör spegla dem som används på hög nivå i branschen.
Där ingår modern versionhantering. Genom att införliva versionhantering i arbetet med inlämningsuppgifter
läggs en stabil grund inför arbetslivet.
Fire, det nuvarande systemet för hantering av inlämningsuppgifter, uppmuntrar inte till ett strukturerat arbetssätt och brister även av följande anledningar:

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
Även handledarna kan interagera på olika sätt med systemet. Det ska vara möjligt att använda avancerade funktioner som relaterar till versionshantering, men handledare ska även kunna få uppgifterna mailade till sig och kunna godkänna med ett mailsvar som systemet bearbetar.

Systemet består av en backend som bland annat hanterar git-repositorier samt en frontend som presenterar repositorierna och möjliggör inlämning och rättning och uppgifterna. Backenden tar emot inlämningarna via de olika kanalerna och placerar dem i någon form av köhanterare som behandlar informationen och presenterar den på frontenden.

Systemet ska baseras på en befintlig öppen plattform. 

## Förslag på features:

- Modern versionshantering för avancerade användare (akademiker/ingenjörer)
- Flexibel definition av uppgifter
  - Möjligt att definiera delmål som godkänns separat
- Tydlig översikt över skillnader mellan en första inlämning och successiva svar på returer - handledaren ser snabbt vad som har förändrats
- Kommentarer knutna till specifika rader i koden
  - Tvåvägskommunikation möjlig - kommentarer på kommentarer.
- Inbyggd plagiatkontroll
- Statistik
  - Programspråksanvändning
  - Antal kodrader
  - Andel godkända samt antal försök
  - Olika studenters andel av kodbasen inom en grupp
  - Kursansvarig kan se hur många inlämningar som är avklarade
- Deadline för handledare
- Progressbar för rättningen
  - Det går att se hur många grupper som har fått sin uppgift rättad
  - Studenter ser hur många som ligger före i rättningskön.
- Kursansvarig kan definiera automatiska **valideringar** för inlämningsuppgifterna
  - Möjlighet att validera en given radbredd inte överskrids
  - Automatisk körning av fördefinierade unittester.
  - Definera vilka filer som ska ingå i inlämningen, t.ex. *report.pdf*
  - Inlämningar som inte klarar av valideringen kan nekas direkt. Sparar mycket handledartid.
- Readme-filer integrerade i systemet - en fil som uppfyller definitionen av en readme-fil renderas automatiskt på inlämningsuppgiftssidan
- Online-editering
- Bestämd rättningsordning för handledarna
  - En retur på labb 1 ska rättas före en förstainlämning på labb 2.
- Möjlighet till anonym gransking av labbarna, på samma vis som tentarättningen.
