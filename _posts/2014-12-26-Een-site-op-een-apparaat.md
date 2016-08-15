---
layout: post
title: Een site op een apparaat is ook maar gewoon een site, maar dan op een apparaat...
---
**"De website is volledig responsive..." Een zin die je nog steeds vaak ziet. Maar je kunt het eigenlijk tegenwoordig niet meer zeggen. Natuurlijk is het ding responsive! Zo ongeveer 67,3%* van al je bezoekers bekijkt je website op iets wat niet een "standaard desktop versie" is. Het zou strafbaar moeten zijn als je site niet goed werkt op een telefoon! Maar waar moeten wij frontenders nou op letten?**

<small>\* Dit percentage is volkomen fictief en door mijzelf verzonnen. Ik vermoed dat ie wel ongeveer klopt, maar vind dat eigenlijk niet zo belangrijk...</small>

## Responsive
Responsive design houdt eigenlijk in dat er één codebase is die zich volledig flexibel gedraagt binnen de viewport. Door gebruik te maken van media queries, responsive images en flexibele grid systemen kunnen we zorgen dat een site er op alle breedtes lekker uitziet. Maar! Eén codebase, dus alles wordt altijd ingeladen. Ook als je met je mobieltje in de trein van Bedum naar Appingedam zit...

## Adaptive
Bij adaptive design kijken we eerst even wat het apparaat is en aan de hand daarvan bepalen we wat er allemaal nodig is om de pagina te laden. Het is een vorm van Progressive Enhancement. Naast het devicetype kunnen nog meer externe factoren bekeken worden zoals bijvoorbeeld netwerksnelheid. Maar essentieel is: we halen alleen die assets op die we nodig hebben, dus minder laadtijd! Binnen adaptive kun je natuurlijk verder ook gewoon gebruik maken van dezelfde technieken als bij responsive.

## Breakpoints
Vastgestelde punten op de breedte van een viewport waarop <em>iets</em> gebeurt. Eigenlijk is dit iets waarmee je globaal aan je code meegeeft: ¨Hey! Ik ben iets van een tablet, denk ik!". Je krijgt al iets meer zekerheid als je feature detecting gaat toevoegen, zoals "touch". Dus het venster is ergens tussen de 481px en 1024px breed, én is een touch-screen. Vermoedelijk heb je een tablet te pakken. Tegenwoordig gebruiken we de breakpoints eigenlijk alleen om aan te geven dat we op een palm, lap of desk breedte zitten.

## Tweakpoints
Veel interessanter zijn de tweakpoints. Ze klinken minder belangrijk, maar dit is waar alle magie in gebeurt. Het is natuurlijk van belang om te weten binnen welke breakpoints je zit voor het bepalen welke code er geserveerd moet worden. Maar binnen die breakpoints kan er nog steeds vanalles omvallen. Daar zijn tweakpoints voor. Wat je wil doen is: per element op je pagina kijken wat er gebeurt op een bepaalde breedte en daarop handelen. Dus: breakpoints voor je site, tweakpoints voor wat er op je site staat!

## Maar hij doet het niet als ik mijn scherm verklein...
Hierin moet je flexibel zijn, je zit op een desktop en wil je scherm zo klein maken als een mobiel, en dan zien hoe het er op een mobiel uitziet? Zo werkt het niet, een site 'voelt' namelijk anders aan als je hem op een mobiel bekijkt. De boel moet niet stukgaan als er gesleept wordt met het desktopscherm. Je zou namelijk een heel klein scherm met een keilage resolutie kunnen hebben. Maar dat vang je af met je tweakpoints, als het goed is. Maar bij het ontwikkelen voor alle devices, moet je ook testen in alle devices en zorgen dat het op alle devices optimaal werkt, voor dát device...

## Oja!
Het bepalen van de devices kan best rechtoe rechtaan zijn. Mobiel, tablet en "vast scherm". Maar je zou ook los kunnen gaan en bijvoorbeeld een printer of screenreader als device kunnen rekenen. Of een Google-bot. Overigens kijkt en toont Google tegenwoordig hoe mobile-friendly je site is en rankt beter als je performance goed is. Maar die onderwerpen zijn een blogpost op zichzelf waard.

## Eigenlijk is het allemaal onzin...
Responsive, adaptive, mobile first, al die termen vind ik eigenlijk compleet nutteloos. Het gaat om een zo goed mogelijke ervaring leveren, aan elke gebruiker, ongeacht het ding waarmee hij de site bezoekt.

Performance, optimaal gebruik van resources, zorgen dat je niet teveel in hoeft te laden, zorgen dat de browser de pagina zo snel mogelijk weergeeft, of in ieder geval iets op de pagina laat zien. Dát vind ik pas echt een strategie. Ik noem het "think first"! Net als alle naamgevingen, het zijn maar termen. Maar denk erover na, wat heb je nodig? Je kunt natuurlijk je superdikke responsive template van 28 MB over een GPRS lijntje sturen, maar heeft dat zin? Het hangt van de situatie af en die is voor elk project anders, daarom: think first!
