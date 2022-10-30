## Menyhárt Tamás és Posta András
### Virtual Reality: Témakör 10: Interaction (kölcsönhatások)
-----------------------------------

Itt az ember kölcsönhatásairól a virtuális valóságban, motoros képességekről, gépi tanulásról, remappingról, mozgásokról, virtuális tér manipulálásáról és a szociális interakciókról lesz szó.

> Források:

> Könyv szerzője, címe: Steven M. LaValle: Virtual Reality

> Kiadó neve, kiadás éve, oldalszám: Cambridge University Press, 2016, 418 oldal

## Kölcsönhatások a virtuális valóságbam

Az ember és a virtuális tér kapcsolatán az alábbi kérdések merülhetnek fel:
- Hogyan
  - lépjenek kapcsolatba a felhasználók a virtuális világgal? 
  - kellene mozogniuk?
  - tudnak tárgyakat megragadni, mozgatni és elhelyezni?
  - viszonyulnak más entitásokhoz?
  - működjenek együtt a fájlokkal vagy az internettel?

> **<u>Univerzális szimulációs elv:</u>** A valós világ bármely mechanizmusa szimulálható VR-ben.

Példák:
- A felhasználó
  - kinyithat egy ajtót egy gomb (F) megnyomásával
  - egy virtuális repülőgépet üzemeltethet úgy, hogy egy pilótafülkében ül

Az univerzális szimulációs elv nem feltétlenül realizmus. Gyakran jobb az interakció jobbá tétele mint a valóság. Ezért ez a fejezet olyan interakciós mechanizmusokat mutat be, amelyek esetleg nincs megfelelője a fizikai világban. Az 1. szakasz bemutatja az általános gépi tanulási és szabályozási fogalmakat.

> **remapping**: a való világban való mozgás leképezése egy lényegesen eltérő mozgásra a virtuális világban.

Fontos feladataink a virtuális valóság használatához:
- Felhasználó számára a működés, mozgás:
    - könnyen megtanulható
    - használható
    - kényelmes
    - hatékony feladathoz
- Felhasználó számára mozgás megvalósítása a virtuális térben úgy, hogy a valóságban marad.
- A térrel (pl.: tárgyakkal) való interakciók, manipulációk leírása
- A felhasználók egymás közötti interakcióinak, kommunikációjának megoldása

### 1. Motoros képességek és remapping
-------------------------------

> **Motoros képességek**: Életünk során fejlesztjük finommotorikus készségeinket számos konkrét feladat elvégzéséhez, mint például szövegírás, cipőfűző kötözés, labdadobás, és biciklizés. Ezeket gyakran motoros kéépességeknek (számítógép esetén gépi tanulásnak) nevezik, és megtanulják ismétlődő próbák révén, a pontosság és a könnyűség fokozatos javulásával, ahogy az elvégzett gyakorlatok száma nő. Végül előállítjuk a mozgásokat anélkül, hogy figyelni is kelljen rájuk. Például a legtöbb ember tud autót vezetni figyelmen kívül hagyva a kormánykerék, a fékek bizonyos műveleteit.

Ezzel a módszerrel mi is megtanultuk pl.: kezelni a számítógépen található interfészt. Próbálkozásokon keresztül az egér hasznalatát könnyen- és hamar el lehet sajátítani, míg a billentyűzeten való vakon gépelés megtanulása akár évekig tarthat.


Tervezési szempontok A VR interakciós mechanizmusainak fejlesztése során:
1. Magas hatékonyság elérése a 
    - feladat elvégzésének gyorsaságában
    - pontosságában
    - mozgási tartomány meghatározásában (opcionális)
2. Az új motoros képességek elsajátításának nehézségei
    - ideális esetben a felhasználónak nem kellene sok hónapot tölteni egy új mechanizmus elsajátításával.
3. Könnyű használhatóság a kognitív terhelés szempontjából
    - az interakciós mechanizmusnak kevés vagy egyáltalán nem kell koncentrált figyelmet igényelnie némi gyakorlás után.
4. Általános kényelem hosszabb ideig tartó használat során
    - Ne alakuljon ki izomfáradtság, hacsak nem valamilyen fizikai gyakorlat a feladat.

Az agy a mozgás megvalósításához elektromos inpulzusokat küld az izmokba, ezáltal mozgásra kényszerítve őket.

![kép az agyról](./media/kep1.png)

(a) Az agykéreg egy része a mozgásnak van szentelve.

(b) Sok más részek kölcsönhatásba lépnek a kéreggel, hogy mozgásokat hozzanak létre és hajtsanak végre, beleértve a talamusz, a gerincvelő, a bazális ganglion, az agytörzs és a kisagy.

> **A mozgás neurofiziológiája**: először is vegyük figyelembe az akaratlagos mozgások (harántcsikolt izomszövet hajtja végre a mozgásokat) tanulásában, irányításában és végrehajtásában részt vevő idegi részt az (a) ábrán. Az elsődleges motoros kéreg a mozgást szabályozó idegi jelek fő forrása, míg a premotoros kéreg és a kiegészítő motoros terület érintett a mozgás előkészítésében és tervezésében. A kommunikáció neutrális jeleken keresztül megy végbe, ahogy azt a (b) ábra mutatja. A kisagy egy speciális feldolgozó egység, amely többnyire a mozgásnak van szentelve, de más funkciókat is betölt.

A **kisagy** egy feldolgozó egység, ami:
-------------
-  101 milliárd neuront tartalmaz, ami jóval több, mint a teljes agykéreg, amely 20 milliárdot
- a mozgást, koordinációs kézségeket, precíz,- finom mozgásokat segíti, teszi lehetővé
- részt vesz a figyelem megtartásában, nyelvben és a beszédben
- a motoros képességek tárolási központja
- széles körű megfigyelések szerint károsodás esetén romlik a:
    - finommotoros kontroll
    - új motoros képességek tanulása
- felhasználása a VR számára a szenzomotoros kapcsolatok tanulása (pl.: szem kéz koordináció).

![Kép az Atari breakout játékról](./media/kep2.png)

(a) Atari 2600 lapátvezérlő.

(b) Az Atari Breakout játék, amelyben az alsó vonal szegmense egy virtuális lapát, amely lehetővé teszi a labda pattogását, cél, hogy a labda minden téglának nekiütközzön, ezáltal a téglák megszűnnek.


A motorvezérlő jelek és a szenzoros és észlelési jelek közötti szoros kapcsolat kialakítása kulcsfontosságú számos feladatnál. Ezek a mérnöki területen is széles körben ismert rendszerek, amelyekben az érzékelő-visszacsatolás és a motorvezérlés egyesítik az alkalmazásokban mint például a robotika és a repülőgépek stabilizálása; az ezzel foglalkozó entitás az ún. vezérlőrendszerek. Köztudott, hogy a zárt hurkú rendszert részesítik előnyben, amelyben
az érzékelő információi visszacsatolást adnak a végrehajtás során, szemben a nyílt hurokkal, amely a motorjeleket az idő függvényében adja meg.

Fontos szempont, hogy egy motoros képesség megtanulása mennyi időt vesz igénybe. Ez személyenként eltérő, de van egy várható értéke, ami megfelel a valóságnak (pl.: egér mozgását mindenki hamarabb megtanulja, mint a vakon gépelést a billentyűzeten).

> **Neuroplaszticitás**: az agy azon képessége, hogy átszervezze idegi struktúráit
és új utakat (idegi pályákat) alakítanak ki az új ingerekhez való alkalmazkodáshoz. Kisgyermekkorban szinaptikus metszés a mértéke a legnagyobb, ami az idő folyamán exponenciálisan csökken (ezért fontos gyerekkorban a tanulás pl.: egy kisgyerek rövid idő alatt képes megtanulni egy egész nyelvet is, ami egy felnőttnek már nehezése esik). Emiatt az egészséges felnőtteknél körülbelül feleannyi szinapszis van neurononként, mint egy két vagy három éves gyermeknek. Viszont a csökkenés mértéke az agy mentális tornáztatásával jelentősen csökkenthető, így megelőzhetőek olyan időskori betegségek, mint a demencia.

> **Motoros képességek tanulása**: legyen egy egyszerű,- klasszikus példa a Breakout videojáték, amit az Atari fejlesztett ki 1976-ban. A játékos elforgatja a gombot, amely az (a) ábrán látható. Ez a képernyő alján lévő vonalszakasz vízszintes elmozdulását okozza. A lapát egy potenciométert tartalmaz, amely kalibrálással lehetővé teszi a gomb orientációjának megbízható becslését. A játékos látja a vonalszakaszt a képernyő alján, és gyorsan társítja a gombok tájolását. A tanulási folyamat tehát magában foglalja a vizuális észlelést, a
propriocepciós jeleket a gomb elforgatásából és a szenzomotor meghatározását.

![kép a virtuális egérről](./media/kep3.png)

(a) Apple Macintosh egér.

(b) Ahogy az egér mozog a táblázatban a virtuális ujj ennek megfelelően mozog, de 90-al el van forgatva fokra és nagyobb távolságot tesz meg.

![CS:GO kép](./media/kep4.webp)

> **Kapcsolatok és a fizika törvényei**: Egy ügyes játékos gyorsan tudja elforgatni az egeret, így a kéz egy kicsi mozgatásával nagy távolságot tud pontosan meghatározni. Például: ha valaki egy mesterlövész puskával a CS:GO nevű játékot játsza, akkor amikor a másodperc tört része alatt megfordul, és fejbelő, akkor az oroszul való káromkodás után elemezhetjük ezt az eseményt. Tehát, a játékos a kezét minimálisan mozgatta, viszont egy egész emberi test képes volt megfordulni, nagy távolságot megtenni. Gyakori eset, hogy a virtuális tér sokkal jobb teljesítményt tud nyújtani, mint a valóság, mert ott nem (feltétlenül) érvényesek a fizika törvényei. Pl.: Amikor el kezdtünk megfordulni a karakterünkkel t=n idő alatt, ahol lim n -> 0, akkor v=0 m/s sebességből lett v=sok m/s, akkor ha felírjuk a gyorsulást, hogy a=Δv/Δt (sebességváltozás/eltelt idő, ahol az eltelt időt kis időegységre kell nézni, így kicsi az időegységre eső sebességváltozás is) akkor ez a Δt=t(összes) olyan kicsi, hogy nem mérhető, így sok/+0 0-val kellene osztani (ami nem nulla, csak elhanyagolhatóan kicsi), tehát végtelen gyorsulással kezdett el fordulni a karakterünk, ami a valóságban lehetetlen. További probléma, hogy a tehetetlenség törvénye (Newton I.) miatt 1/2 * m * v^2 energiát adtunk a karunknak és a puskának t=n lim n-> 0, ami szintén lehetetlen.  Ugyanígy, végtelen gyorsulással állt meg a játékos karaktere (fordul a karakter, és amikor eléri a másik játékos fejét azonnal megáll). Itt ezen kívül olyan problémák is előfordulnak mint hogy a karunknak és a puskának is van tömege, így érvényes rá a lendületmegmaradás törvénye (Newton II.) is. De sorolhatnék még például olyat, hogy a kezéből a puska távcsövét azonnal a szeméhez rakta egy kattintással. Mivel ezek nincsenek jelen a játéban, így a játékosnak csak az ügyessége és a reflexei számítanak (meg az inputlag nagysága (ping), de ezt most hagyjuk ki).

