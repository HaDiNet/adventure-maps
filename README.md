# HaDiKo-WorkAdventure-Maps

Hier werden die Maps für das HaDiKo [WorkAdventure](https://workadventu.re) gehosted,
zu erreichen unter https://play.adventure.hadiko.de.

Geforked von [DigitaleGesellschaft](https://github.com/DigitaleGesellschaft/workadventure-map-bitwaescherei),
was wiederrum eine Kopie des offiziellen [starter kit](https://github.com/thecodingmachine/workadventure-map-starter-kit) ist.

In der [index.html](https://maps.adventure.hadiko.de/hadiko/index.html) gibt es weitere Informationen zu Lizenzen und Urhebererecht.

## Eigene Maps beisteuern

Um das HaDiKo vollständig digital nachzubauen,
sind wir auf deine Hilfe angewiesen.
Hier ist erklärt, wie du helfen kannst.

Die Maps bestehen aus meherern Layern von 32x32 pixel "Tiles".

### Tools die du brauchst

Um Maps zu erstellen oder zu bearbeiten benötigst du:

- Den [Tiled editor](https://www.mapeditor.org/)
- "Tiles", also 32x32-Pixel-Bilder aus denen die Map zusammengebaut wird.
  Ein paar gute Tilesets sind in den [pngs](pngs/)- und [tiles](tiles/)-Ordnern zufinden.
  Weiter findest du im Internet, z.B. auf:
  - [itch.io](https://itch.io)
  - [opengameart.org](https://opengameart.org)
  - [deviantart.com](https://deviantart.com)
- [npm](https://www.npmjs.com/) um deine Map zu testen.

### Repository forken

Zuerst musst du dieses Repository forken.
In dem geforkten Repository führst du deine Änderungen durch und machst danach einen Pull Request auf.

### Die Map in Tiled öffnen und bearbeiten

Unsere Maps liegen im [world](world/)-Ordner, z.B. [world/k1.json](world/k1.json)
Ein paar Beispiel-/Testmaps findest du in [test](test/), oder [maps](maps/).

Du kannst die JSON-Datein in [Tiled](https://www.mapeditor.org/) öffnen.
Um eine neue Map zu erstellen, lege mit Tiled eine Map in JSON-Format im [world](world/)-Ordner an.

Nun kannst du die Maps bearbeiten.

Die Tiled software ist relativ intuitiv. Nichtdestotrotz hier ein paar Resourcen, falls du Anleitung brauchst:

- [Tiled documentation](https://doc.mapeditor.org/en/stable/manual/introduction/)
- [Tiled video tutorials](https://www.gamefromscratch.com/post/2015/10/14/Tiled-Map-Editor-Tutorial-Series.aspx)

### Wie WorkAdventure-Maps funktionieren

Damit deine Map von WorkAdventure geladen werden kann, musst du einige regeln beachten.
Am besten liest du den offiziellen [WorkAdventure Map Building Guide](https://workadventu.re/map-building/wa-maps),
der ist nicht so lang, man kann sich innerhalb von 20 Minuten durch alle Seiten durchklicken.

### Die Map ausprobieren

Bevor du einen Pull Request erstellst, willst du deine Änderungen oder neuen Maps bestimmt ausprobieren.
Hierzu kannst du einen lokalen Mapsserver starten, der deine Maps deinem Browser zur Verfügung stellst.
Führe dazu im Repository die folgenden Commands aus:
```
npm install
npm run start
```

Danach kannst du die Maps mit einer beliebigen WorkAdventure Instanz ausprobieren, am besten der vom HadiKo:

http://play.adventure.hadiko.de/_/global/localhost:8080/pfad/zur/map.json

Also zum Beispiel:

http://play.adventure.hadiko.de/_/global/localhost:8080/world/k1.json

### Urheberrecht und Lizenzen

Damit wir deine Map verwenden können, musst du damit einverstanden sein,
sie unter einer [CC-BY-SA](http://creativecommons.org/licenses/by-sa/4.0/) Lizenz zu veröffentlichen.

Füge hierzu in der [index.html](index.html) einen Vermerk unter "Original Contributions" hinzu.
Entweder als zusätzlicher Name bei einer existierenden Map, oder als komplett neue Zeile.
Diese hat das Format:
```html
<li><a href="$PFAD_ZUR_MAP.json"</a>: $NAME, $JAHR</li>
```

Wenn du zusätzliche Tilesets oder sonstige Resourcen einbindest,
musst du je nach Lizenz des Quellmaterials diese vermutlich nennen.
Füge dazu, ebenfalls in der [index.html](index.html) einen Vermerk der folgenden Form hinzu:

```html
<li>
  <a href="$PFAD_ZUR_DATEI">$NAME_DES_WERKS</a>:
  $URHEBER;
  $LIZENZINFORMATION;
  <a href="$LINK_ZUR_ORIGINALQUELLE">$LINK_ZUR_ORIGINALQUELLE</a>
</li>
```

Die [index.html](index.html) kann unter https://maps.adventure.hadiko.de abgerufen werden
und wird beim joinen auf der Start-Map von https://play.adventure.hadiko.de angezeigt.
