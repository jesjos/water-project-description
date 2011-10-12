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

Studenter kan editera filerna direkt i webbläsaren, kan se hur rättningsarbetet fortskrider (hur många grupper som har fått sina inlämningar rättade) och möjlighet finns att lämna in anonymt om kursansvarig väljer det.
Även handledarna kan interagera på olika sätt med systemet. Det ska vara möjligt att använda avancerade funktioner som relaterar till versionshantering, men handledare ska även kunna få uppgifterna mailade till sig och kunna godkänna med ett mailsvar som systemet bearbetar.

Handledarna erbjuds även andra tjänster. Flexibel definition av uppgifter med delmål. Automatisk validering kan användas för att snabba upp rättningsprocessen genom att direkt förkasta inlämningar som inte uppfyller vissa tekniska krav - till exempel mappstruktur eller maximal radbredd. Kursansvarig kan även definiera unittest som automatiskt körs när uppgiften lämnas in. Studenten får snabb återkoppling om inlämningen refuseras. Kommentarer kan knytas till specifika kodrader vilket möjliggör tvåvägskommunikation mellan handledare och studenter. Automatisk plagiatkontroll och avancerad insamling av statistik finns inbyggt i systemet. Vid returer ger systemet handledaren en översikt där det framgår vilka förändringar som har skett. 

Systemet består av en backend som bland annat hanterar git-repositorier samt en frontend som presenterar repositorierna och möjliggör inlämning och rättning och uppgifterna. Backenden tar emot inlämningarna och handledarkommunikation via de olika kanalerna och placerar dem i någon form av köhanterare som behandlar informationen och presenterar den på frontenden.

Systemet ska baseras på en befintlig öppen plattform. 

## Förslag på features:

- Tydlig översikt över skillnader mellan en första inlämning och successiva svar på returer - handledaren ser snabbt vad som har förändrats
- Deadline för handledare
- Readme-filer integrerade i systemet - en fil som uppfyller definitionen av en readme-fil renderas automatiskt på inlämningsuppgiftssidan
- Bestämd rättningsordning för handledarna
  - En retur på labb 1 ska rättas före en förstainlämning på labb 2.

## Kostnader
Det kan bli nödvändigt att hyra in server-resurser i form av VPS eller någon molntjänst.

## Förslagslämnare

- [Linus Oleander](http://github.com/oleander)
- [Jesper Josefsson](http://github.com/jesjos)
- [Arash Rouhani](https://github.com/Tarrasch)