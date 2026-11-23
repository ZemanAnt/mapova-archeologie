# Mapová archeologie – 3D atlas českých hradišť

První pracovní verze statického webu pro Cloudflare Pages. Česká úvodní stránka, přehled připravovaných lokalit a interaktivní 3D prohlížeč.

## Cloudflare Pages – nastavení

- Repository: `ZemanAnt/mapova-archeologie`
- Production branch: `main`
- Framework preset: `None`
- Build command: `exit 0`
- Build output directory: kořen repozitáře (`/`, bez názvu podsložky)
- Root directory (advanced): ponechat výchozí
- Název projektu: `mapova-archeologie`

Tato verze nevyžaduje npm ani sestavování. Vstupní stránkou je `index.html`.

## Co web nyní opravdu umí

- Interaktivní 3D ukázka **syntetického** terénu (není to vědecký model žádné lokality).
- Otáčení, zoom a základní pohled.
- Lokální otevření souboru `.glb` v prohlížeči (data se nikam neodesílají).
- Přehled čtyř plánovaných lokalit (Divoká Šárka, Závist, Mařín, Levý Hradec).
- Responzivní zobrazení na mobilu.

## Co zatím neumí

- Nahrát soubory přes veřejný web na server (statické Pages nemají úložiště ani administrační backend).
- Zveřejňovat nebo poskytovat skutečné tiskové soubory STL/3MF (zatím žádné nejsou dodány).
- Předkládat syntetickou ukázku jako skutečná geodetická data.

## Další rozvoj

1. Převzít odborně doložené GLB modely a doplnit uvedení původu dat a jejich licence.
2. Pro každou lokalitu vytvořit kartu s metadaty, článek a prameny.
3. Zajistit přímé odkazy na STL/3MF soubory, pokud budou výslovně uvolněny ke stažení.
4. Pro větší modely použít externí objektové úložiště (např. Cloudflare R2).

3D prohlížeč používá Three.js z veřejného CDN, proto je pro jeho plnou funkčnost zapotřebí internetové připojení.
