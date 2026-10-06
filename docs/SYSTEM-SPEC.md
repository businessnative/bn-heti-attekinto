### 09 — Vezetői / heti áttekintő rendszer

**Eredmény:** ellenőrizhető heti helyzetkép és néhány forráshoz kötött vizsgálati javaslat.

**Bemenet:** CSV vagy közös modulok adatai: leadek, foglalások, lezajlott konzultációk, kiküldött ajánlatok, nyert ügyletek, befizetések és nyitott feladatok. Minden importhoz forrás és frissítési idő tartozik.

**MVP:** CSV-mezőpárosítás előnézettel; hibás sorok külön; determinisztikus heti számítás; előző teljes héttel összehasonlítás; adatminőség-jelzés; legfeljebb 3 AI-javaslat; mentett heti pillanatkép; Markdown/CSV export.

**Definíciók:** hétfő 00:00–következő hétfő 00:00 a profil időzónájában, balról zárt, jobbról nyitott intervallum. Új lead: létrehozási esemény. Foglalás: időszakban létrejött, az időszak végéig nem lemondott foglalás, külön mutató a megtartott konzultáció a megtartás dátuma szerint. Ajánlat: első szolgáltató által igazolt küldés; új verzió nem új ajánlat. A kézzel elküldöttnek jelölt ajánlatok külön mutató, nem olvadnak bele az igazolt küldésekbe. Új ügyfél: első nyert megbízás a kontaktushoz. Befolyt összeg: rögzített és megerősített fizetési események mínusz visszatérítések pénznemenként, forráseredettel; várható ajánlatérték külön. Nyitott feladat: az állapottörténet szerint az időszak zárásakor nem lezárt; lejárt: ezen belül határidő kisebb a záró időpontnál. A szükséges időszaki előzmény hiányában a történeti mutató „nem rekonstruálható”, nem a mai státuszból számolt érték.

**Képernyők:** heti összefoglaló; adatok és frissesség; források; mutatódefiníciók; AI-észrevételek; korábbi hetek.

**AI feladata:** a már kiszámolt számokat értelmezi; minden állítás mutatóazonosítóhoz kapcsolódik. Nem számol fejben, nem állít ok-okozatot puszta együttjárásból. Javaslat formája: megfigyelés → lehetséges magyarázat → ellenőrzendő adat → következő lépés.

**Bekötött verzió:** rendszeres import a többi modulból és ütemezett pillanatkép. **Egyedi:** kapacitás, üzleti célok, projekteredményesség. Könyvelési rendszer nem része.

**Mérés:** adatforrások frissessége, hiányzó mezők, heti áttekintés elkészülése, megvizsgált javaslatok.

**Elfogadási esetek:** 09-A: hiányzó bevételforrás → „nincs adat”, nem 0. 09-B: előző hét 0 → százalékváltozás nem végtelen. 09-C: HUF és EUR → külön összeg, nincs spontán átváltás. 09-D: későn beérkező adat → új riportverzió, régi megmarad. 09-E: lead és ajánlat eltérő heti kohorszból → nem címkézi automatikusan konverziónak. 09-F: AI-állításban eltérő szám → kimenet elutasítva/javítandó.


Tényleges készültség: CAPABILITIES.md. A specifikáció nem készültségi állítás.
