# Grid-template with China | JSON, wu2  | Post Mortem 

- titel: China
- tagline: The best page about China
- url: Netlify broke :(
- git: https://github.com/Alex-mp4/wu2-unsplash

## Inledning
Målet med denna uppgift var att använda och ta information från en JSON-fil och implementera den på en 11ty anpassad sida med HTML, CSS och Nunjucks. Innehållet av JSON-filen bestod utav information kring ett land. I mitt fall blev det Kina.

## Bakgrund
Jag började med att undersöka hur apk delen fungerade. Jag tog en titt på hemsidan och råkade göra fel genom att gå en mycket komplicerad väg där jag försökte ladda ned filen istället för att bara hänvisa till en länk via namn. Sedan var det att implementera de bilder jag kunde utse i JSON-filen. Flaggan och Coats of Arms. Det framkom diverse problem kring "size" men det löste sig tillslut genom att redigera shortcode picture stycket.

Istället för att påbörja ett gridsystem direkt använda jag mig av en hastig display flex version. Bara för att vara en temporär template. Denna användas för att utveckla en fungerande mobil-version genom att bara föra över allting till en media-query. Efter några problem kring children fick jag tillslut en snygg och välfungerande grid-template på dator-versionen. Det jag inte insåg förrän efter allt fixande var att "halloween.njk", det vill säga original uppgiften med Unsplash är helt förstörd. Den funkar fint om man går tillbaka i commitsen dock.

Netlify var ej brukbar. Den ville inte hosta min sida och gav mig två errors (exit code: 1 & exit code: 2). Efter att ha kollat igenom jensa.xyz på artikeln "Node version, obehagliga överraskningar" gick jag igenom alternativen och fick inte fram en lösning.

Wave-valideringen gav mig två (2) kontrastfel på två små text-stycken. Eftersom rubriken använder sig av samma färgsystem blev jag lite förvånad av detta men insåg efter vidare försök att det endast fungerade på grund av tjockleken av texten. Jag gjorde den "bolded" och gick vidare. CSS:en funkade bra, med en liten varning vid min användning av "use reset". Å andra sidan gav HTML valideringen mig ett par errors. Båda handlade om användningen av divs och h1 respektive inom ramarna av "pre". Nu har jag ingen aning vad som kan och inte kan användas i pre så jag har det i åtanke till nästa gång för att inte behöva förändra hela min index.njk. 

## Positiva erfarenheter
Att bevisa mina kunskaper kring grid-template för första gången var kul. Det är en mycket logisk teknik när allt är sagt och gjort samt skapar den konsekventa utseenden på hemsidan.

## Negativa erfarenheter
Det hade varit kul om Netlify fungerade och på så sätt skulle det finnas ett lätt sätt att framföra min super utvecklade UI ;).

## Sammanfattning
Jag har skapat en hemsida som tar information från en JSON-fil och visar upp den på en anpassad hemsida för ett land. Det hade varit kul att tillföra mer information på hemsidan men jag behövde debugga lite för mycket problem i min CSS. Tillslut blev allting okej ändå.