# PCTool - Windows kliens
> Egy olyan számítógépes eszköz mely sok olyan funkciót is tartalmaz, amelyet telefonon keresztül irányíthatunk az ehhez készült alkalmazással *TODO: LINK*. 

## Telepítés
************

Letöltöd a **PCTool.exe**-t a master branchről. A telepítő utasításaid követve felrakod.

### A port engedélyezése
> Ahhoz, hogy a program tudjon kommunikálni a telefonos alkalmazással szükséges engedélyezni a *7171* portot a Windows tűzfalban. *Vagy azt kikapcsolni, bár ezt nem javaslom.*
Ezt a program a telepítéskor megcsinálja. Amennyiben mégse az itt leírtak szerint tudod engedélyezni / ellenőrizni.

1. Windows keresőben megkeresed a **Fokozott biztonságú Windows Defender tűzfal**
2. Baloldali menü oszlopban kiválasztod a **Bejövő szabályok** pontot
3. Jobb oldali menü oszlopban kiválasztod a **Új szabály...** pontot
4. A varázslóban az alábbiak szerint jársz el:
    1. Szabály típusa: **Port**
    2. **TCP** protokoll legyen kipipálva, **Adott helyi portok:** legyen kipipálva majd ott add meg az alábbi portot: **7171**
    3. Művelet: **Engedélyezze a kapcsolatot**
    4. Profil opcionálisan állítható
    5. Név: Amit Te szeretnél, átlathatóság kedvéért: PCTool *(Amennyiben a telepítő sikeresen hozzá adta a portot a listához ezen a néven találod meg!)*

TODO: Mozgó kép a port engedélyezéshez

> Amennyiben használsz más fajta tűzfalat is elképzelhető, hogy ott is át kell engedni a portot. Akár még a programot is !

## Funkciók
************
> A program fő funkciója, hogy a számítógépedet bizonyos műveleteket tudj időzítve végre hajtani. Egyszerre több művelet is elindítható.

### Végrehajtható műveletek

1. Kikapcsolás
2. Újraindítás
3. Alvás
4. Lezárás
5. Hibernálás *(Ha a gépeden engedélyezett!)*
6. Kijelentkezés
7. Saját művelet *(A program saját művelet szerkesztőjével készítve)*
    * Adott futtatható fájl futtatása *(Tallózással választva)*
    * Adott folyamat leállítása *(Feladatkezelőből választott)*
    * Makró lejátszása

### Távirányíthatóság

Ahhoz, hogy a program távirányítható legyen az alábbiak szükségesek:

* **Rendszergazdaként futtatni a programot** *(Jobb klikk - futtatás rendszergazdaként, vagy beállítani, hogy mindig rendszergazdaként futtassuk: Jobb klikk - Tulajdonságok - Kompatibilitás - Program futtatása rendszergazdaként opció kipipálása majd alkalmazása)*
* **Ugyanazon a hálózathoz** *(internet nem szükséges)* **legyen csatlakoztatva a két eszköz**
* Fájl - Beállítások - **Távirányíthatóság funkció ki legyen pipálva** a kliensben 

Amennyiben több hálózathoz is csatlakoztatva vagyunk akkor egy felugró ablakban választhatjuk ki, hogy melyik címen szeretnénk elérhetővé tenni a gépünket.
Amint engedélyezve van a menüsorban láthatjuk az IP címet amelyiken keresztül majd elérhetjük a telefonos alkalmazásban.

#### Távirányíthatóság funkciói 
TODO: API hívások
* Adott végrehajtható műveletek listázása
* Végrehajtható művelet indítása
* Jelenleg futó művelet leállítása
* Jelenleg futó műveletek listázása
* A jelenleg futó folyamatok lekérése *(feladatkezelő)*

### Saját művelet készítése

A programban saját műveleteket is definiálhatunk. Ezeknek 2 típusa lehet:
* Adott futtatható fájl futtatása 
* Adott folyamat leállítása

#### Adott futtatható fájl futtatása

Kiválasztunk tallózással egy futtatható fájlt a gépünkról. TODO: Melyik futtatható típusokat támogatjuk ? Mi a helyzet a speciális fájlokkal .jar, .reg ... stb ? 

#### Adott folyamat leállítása

Kiválasztunk a listából egy folyamatot amelyiket le szeretnénk állítani. Ezek a folyamatok megegyeznek a feladatkezelő folyamatival, hiszen onnan kapjuk azt a listát amelyik csak a felhasználói folyamatokat tartalmazza.

Továbbá nevet is adunk egy saját műveletnek, annak érdekében, hogy *Futtatható műveletek* listájában átláthatóan találjuk azt meg.

## Készítők
************
Dancs Bertalan 

## Licensz
************

TODO: Milyen licenszek érvényesek ??