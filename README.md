❄️ LidFrost

LidFrost is a macOS menu bar app that watches your MacBook's lid angle in real time and reacts with a striking visual effect as you close the display — as if the screen were actually freezing over, fogging up, or otherwise responding to being shut.

How it works

Modern Apple Silicon MacBooks (2021 MacBook Pro/Air or newer) have a built-in hardware sensor that measures the lid's angle. LidFrost reads this in real time and gradually intensifies the selected visual effect based on that angle — the more you close the lid, the stronger the effect gets.

The effect is driven by a live screen capture (ScreenCaptureKit), processed through Core Image — so the actual desktop content (icons, windows, wallpaper) is visible through the effect, rather than a flat, static overlay.

Effects

Pick from several independent visual styles in the menu bar:

iPhone Duo style — smooth, frosted-glass blur
Frost — scattered, six-branched ice crystals, growing denser
Brightness — simple, drastic dimming
Dust / Dew — a fine, grimy or dewy glass look
Condensation — randomly appearing moisture droplets
Glitch — RGB channel-shift digital breakup
Interference — live, flickering TV static
Pixel error — an ever-growing number of corrupted color blocks
More features
🔊 Alarm sound — a car-lock-style chirp when the effect starts
🔒 Lock at tilt angle — automatically lock your Mac at a chosen angle, without having to fully close the lid
🎚️ Manual control + Quick preview — manually set the effect strength, or preview it instantly with one click, no lid-closing required
🌐 Hungarian/English language switch
⚙️ Launch at login, adjustable start angle
Requirements
Apple Silicon MacBook with a built-in lid angle sensor (2021 MacBook Pro/Air or newer — not every model has one)
macOS 14 (Sonoma) or later
Permissions: Screen Recording (for the visual effects), Accessibility (for the lock feature, optional)
Important note

Reading the lid angle relies on an undocumented, unofficial Apple HID interface, since Apple doesn't publish a public API for this. As a result:

The app cannot be distributed via the Mac App Store and isn't signed with an official Apple Developer certificate — it must be built from source, and Gatekeeper needs a one-time approval.
A future macOS update could break it.
Not every Mac has this sensor — if yours doesn't, the app still runs, but the core feature won't be available.
Building from source
bash
git clone <repo-url>
cd LidFrost
chmod +x build.sh install.sh
./build.sh
./install.sh
Developer

-=ImrusMágus=-  
-------------------------------------------------------------------------------------------------------------------------------------------------
❄️ LidFrost

LidFrost egy macOS menüsori alkalmazás, amely a MacBook fedelének dőlésszögét figyeli, és valós időben, látványos vizuális effektekkel reagál arra, ahogy csukod a kijelzőt — mintha a képernyő ténylegesen "befagyna", bepárásodna vagy egyéb módon reagálna a becsukásra.

Hogyan működik?

A modernebb Apple Silicon MacBook-ok (2021-es vagy újabb MacBook Pro/Air modellek) beépített hardveres szenzorral rendelkeznek, ami méri a kijelző dőlésszögét. A LidFrost ezt olvassa ki valós időben, és a szög alapján fokozatosan felerősíti a kiválasztott vizuális hatást — minél jobban csukod a fedelet, annál erősebb az effekt.

A hatás egy élő képernyő-rögzítésen (ScreenCaptureKit) alapul, amit Core Image-dzsel dolgozunk fel — így a tényleges asztali tartalom (ikonok, ablakok, háttérkép) látszik a hatáson keresztül, nem egy egyszerű, statikus fedőréteg.

Effektek

Több, egymástól teljesen független vizuális stílus közül választhatsz a menüsorból:

iPhone Duo style — sima, füstüveg-szerű elmosódás
Jegesedés — szétszórt, hatágú jégkristályok, sűrűsödve
Fényerő — egyszerű, drasztikus elsötétülés
Porosodás / Harmat — finom, koszos/harmatos üveg-hatás
Párakicsapódás — véletlenszerűen megjelenő páracseppek
Glitch — RGB-csatorna-eltolásos digitális "szétesés"
Interferencia — élő, villódzó TV-statikus zaj
Pixelhiba — egyre szaporodó, hibás színes pixel-blokkok
További funkciók
🔊 Riasztó hang — autóbezáráshoz hasonló hangjelzés a hatás indulásakor
🔒 Zárolás dőlésszögnél — a Mac automatikusan zárolható egy beállított szögnél, anélkül hogy teljesen le kéne csukni a fedelet
🎚️ Kézi vezérlés + Gyorselőnézet — a hatás erőssége kézzel is állítható, illetve egy gombnyomással megnézhető, fedélcsukás nélkül
🌐 Magyar/angol nyelvváltás
⚙️ Automatikus indítás bejelentkezéskor, testreszabható kezdő szög
Rendszerkövetelmények
Apple Silicon MacBook, beépített dőlésszög-szenzorral (2021-es vagy újabb MacBook Pro/Air modellek — nem minden gép rendelkezik vele)
macOS 14 (Sonoma) vagy újabb
Engedélyek: Képernyőrögzítés (a vizuális hatásokhoz), Kisegítő lehetőségek (a zárolás funkcióhoz, opcionális)
Fontos tudnivaló

A dőlésszög kiolvasása egy nem hivatalos, dokumentálatlan Apple HID-interfészen keresztül történik, mivel Apple nem publikál erre hivatalos API-t. Emiatt:

Az app nem kerülhet fel a Mac App Store-ra, és nincs hivatalos Apple Developer aláírással ellátva — forrásból kell lefordítani, és a Gatekeeper egyszeri feloldására lesz szükség.
Előfordulhat, hogy egy jövőbeli macOS-frissítés után nem működik tovább.
Nem minden Mac rendelkezik ezzel a szenzorral — ha nincs meg, az app fut, de a fő funkció nem elérhető rajta.
Telepítés forrásból
bash
git clone <repo-url>
cd LidFrost
chmod +x build.sh install.sh
./build.sh
./install.sh
Fejlesztő

-=ImrusMágus=-
