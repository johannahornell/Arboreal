# Individuell examination 1

Uppgiften går ut på att skapa en hemsida åt företaget Arboreal med HTML och CSS. Jag skapade en single-page application. Detta fungerar bra då sidan inte har så mycket text och det går snabbt att scrolla sig igenom sidan. Jag valde att lägga till lite kod i media queries för att den ska fungera okej på mindre enheter, men fokus har legat på att första versionen ska fungera på desktops. 

## Validation HTML: 
> Document checking completed. No errors or warnings to show.

## Validation CSS: 
> Unrecognized at-rule @supports

## breakpoints

Jag har valt att skapa designen för mobile first. De breakpoints som jag använt är: 

* min-width: 480px
* min-width: 768px
* min-width: 1200px

För mobiler (under 480px) är designen nästan likadan som skärmar mellan 480px och 768 px. Det enda som ändrats är att höjden på headern, samt texten i headern, blir en aning större på skärmar mellan 480px och 768px samt att kolumnerna i footern är 33% istället för 100%. Detta för att det finns plats för footern att ha den layouten på dessa skärmar. 

Då sidan som högst har 3 kolumner i en rad fungerar layouten för en desktops lika bra som layouten för en tablet. Därför har jag valt 768px som en breakpoint.

Till sist är det en breakpoint på 1200px där den enda skillnaden är att headerbildens höjd är större då jag anser att den annars ser kort ut på dessa skärmar. 

## Responsive patterns

Jag har främst använt mig av 3-column och 2-columns layout på sidan. Sidan är fluid och jag har valt att på mindre enheter främst använda 1-columns layout då det annars ser så ihoptryckt ut, plus att det blir svårt att läsa. 

För navigationen har jag använt mig av en toggle fixed nav. För tablets och mobiler blir den till en hamburger meny. Jag har valt att göra detta då menyn tar upp för mycket plats på mindre enheter. 

Bilderna som används är basic fluid images. De anpassar sig efter layouten vilket är snyggt. 

## Feedback från Cecilia

### Design/Själva hemsidan:

* Enhetlig och bra, men kanske hade velat se färgen som submit knappen har på fler ställen. Den sticker ut lite extra just nu, vilket på sitt sätt kan vara bra.

> Jag valde att ta upp den turkosa färgen på alla h2 rubriker 

### HTML

* Mycket divs pga phone/responsivt (grid:en med bilder under 'om företaget' text), inget att göra åt såvis, men blir lite extra att läsa.

> Jag lät divarna vara kvar som de är då de används för styling-syfte. Håller med om att det kan se lite rörigt ut men vet inte hur man kan lösa detta på ett annat sätt

* col-1-2 kanske inte någon super namngivning

> Jag ändrade classen col-1-2 till column-half och col-1-3 till column-third för att förtydliga vad som menas med dom 

### CSS

* Se första punkten på HTML

## Feedback från Amir 

Very good work and nice website! Few things to perfectionate it!

### Overall review:

* The slogan (typo)! A workplace that is alive, creates ideas that live on! (a should be taken away)

* Our mission: The better English writing is: Arboreal revolutionizes the way you think about plants in an office environment. Arboreal isn't just a delivery service for plants, rather it's a service to deliver new ideas. Arboreal makes it easy to keep your workplace fresh and oxygenated.

> De två första punkterna har jag bortsett ifån då det inte är jag som är ansvarig för texten på sidan. Tycker dock inte att det är något fel på texten och det han nämner är bara ett annat sätt att formulera det på.

* Responsiveness: When changing the size to smaller the footer area does not look good! Check what the problem is in CSS review!

* Address is a contact info. So instead of writing contact I guess you should write Telephone number and Email! So maybe you want to rearrange the footer section!

> Mer av en smaksak skulle jag säga. Tycker det fungerar som det är. 

### HTML

* Menu has not sub-menu under Themes

> Anser inte att det är nödvändigt då de inte tar upp sån stor plats samt att de kommer direkt efter varandra. 

* hide-phone name is better change to hide-phone-size

> Valde att ändra det till desktop-only för att göra det tydligare 

* when decreasing width, the footer area is not homogeneous! when width is less than 480px, to solve this you should change the flex-basis to 100% to have all the columns right after each other!

> Fixade det så att de får 100% bredd på mobila enheter under 480px

* In real dynamic website you should write "<div class="section-wrapper picture-wrapper">" in a loop instead of writing many li and pictures

> Inte helt hundra på vad som menas med detta. Har ej hört att man kan använda loops i HTML. 

### CSS

* I am nit sure if box-sizing by default should be border-box. Maybe defining that in div or sections is safer!

> [https://css-tricks.com/box-sizing/](https://css-tricks.com/box-sizing/)

* defining box-sizing is repeated again in *

> [https://css-tricks.com/box-sizing/](https://css-tricks.com/box-sizing/)

* background color by default is white. line 37

> Navigationen har inte by default en bakgrundsfärg. Jag måste lägga till en bakgrundsfärg på hela navigationen då innehållet är floatade åt båda hållen vilket lämnar ett tomt space mellan dom.

## Övriga ändringar

Utöver feedbacken har jag valt att göra vissa ändringar för att förbättra designen och layouten i olika webbläsare. 

* Ändrat padding från procent till em på vissa ställen för att det ska fungera korrekt i FireFox. 

* Fixade hamburgermenyn. Kopplade ett nytt clickevent, closeMenu(), till varje a-element i navigationen. Detta gör så att den stänger sig när man klickar på en av länkarna i navigation.

* Använde main {display:block;} för att main-taggen ska fungera i IE

* Lagt till prefixes för flexbox

* Lagt till @support för flexbox 