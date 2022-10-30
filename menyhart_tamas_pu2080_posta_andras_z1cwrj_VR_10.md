## Menyhárt Tamás és Posta András
### Virtual Reality: Témakör 10: Interaction (kölcsönhatások)
-----------------------------------

Itt az ember kölcsönhatásairól a virtuális valóságban, gépi tanulásról, remappingról, mozgásokról, virtuális tér manipulálásáról és a szociális interakciókról lesz szó.

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

<u>Univerzális szimulációs elv:</u> A valós világ bármely mechanizmusa szimulálható VR-ben.

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

### 1. Motor programok és remapping
-------------------------------

> **Motor program**: Életünk során fejlesztjük finommotorikus készségeinket számos konkrét feladat elvégzéséhez, mint például szövegírás, cipőfűző kötözés, labdadobás, és biciklizés. Ezeket gyakran motoros programoknak (gépi tanulásnak) nevezik, és megtanulják ismétlődő próbák révén, a pontosság és a könnyűség fokozatos javulásával, ahogy az elvégzett gyakorlatok száma nő. Végül előállítjuk a mozgásokat anélkül, hogy figyelni is kelljen rájuk. Például a legtöbb ember tud autót vezetni figyelmen kívül hagyva a kormánykerék, a fékek bizonyos műveleteit.

Ezzel a módszerrel mi is megtanultuk pl.: kezelni a számítógépen található interfészt. Próbálkozásokon keresztül az egér hasznalatát könnyen- és hamar el lehet sajátítani, míg a billentyűzeten való vakon gépelés megtanulása akár évekig tarthat.


Tervezési szempontok A VR interakciós mechanizmusainak fejlesztése során:
1. Magas hatékonyság elérése a 
    - feladat elvégzésének gyorsaságában
    - pontosságában
    - mozgási tartomány meghatározásában (opcionális)
2. Az új motoros programok elsajátításának nehézségei
    - ideális esetben a felhasználónak nem kellene sok hónapot tölteni egy új mechanizmus elsajátításával.
3. Könnyű használhatóság a kognitív terhelés szempontjából
    - az interakciós mechanizmusnak kevés vagy egyáltalán nem kell koncentrált figyelmet igényelnie némi gyakorlás után.
4. Általános kényelem hosszabb ideig tartó használat során
    - Ne alakuljon ki izomfáradtság, hacsak nem valamilyen fizikai gyakorlat a feladat.