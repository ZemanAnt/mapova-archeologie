# Mapová archeologie – 3D atlas českých hradišť

Web pro Cloudflare Pages, automatické publikování z větve `main` repozitáře `ZemanAnt/mapova-archeologie`.

## Katalog hradišť

| Lokalita | Stav | Vstup |
|---|---|---|
| Divoká Šárka | 3D LiDAR model | [Prohlížeč](lokality/divoka-sarka.html) |
| Stará Kouřim | 3D LiDAR model z `kourim_3d.html` | [Prohlížeč](lokality/stara-kourim.html) |
| Mařín | 3D model z exportu `oblast_3d.html` – **pracovní přiřazení lokality** | [Prohlížeč](lokality/marin.html) |
| Levý Hradec | 3D LiDAR model | [Prohlížeč](lokality/levy-hradec.html) |
| Oppidum Závist | Připravuje se | Karta v katalogu |

Fotografické náhledy katalogu jsou doplněny u Divoké Šárky, Staré Kouřimi, Závisti a Levého Hradce. U Mařína byla doplněna fotografie dřevěné zvonice v osadě (Jiří Komárek, Wikimedia Commons, CC BY-SA 4.0, [zdroj](https://commons.wikimedia.org/wiki/File:Ma%C5%99%C3%ADn_(02).jpg)). **Fotografie Mařína neukazuje samotné hradiště**, nýbrž obec v jeho blízkosti. V případě nedostupnosti vzdálené fotografie se zobrazí původní vizualizace reliéfu `assets/thumbnails/marin.svg`. Přiřazení exportu `oblast_3d.html` k hradišti u Mařína nadále není ověřeno.

## Princip publikování

Původní autonomní 3D HTML exporty jsou velké (přibližně 17–19 MB). Z důvodu snadnější správy jsou uložené po částech v `assets/<lokalita>/part-NN.txt`. Stránky příslušných lokalit tyto soubory stáhnou, spojí a vykreslí v iframe. V prohlížeči lze stáhnout původní HTML a GLB. Měřicí funkce pocházejí z dodaných exportů.

- Divoká Šárka: `divoka_sarka_3d.html`
- Stará Kouřim: `kourim_3d.html` (vložený skutečný export, použit také jako výchozí demo na hlavní straně)
- Mařín: `oblast_3d.html` (interní název „Oblast“, přiřazení k Mařínu není samotným souborem prokázáno)
- Levý Hradec: `levy_hradec_3d(1).html`

Zdrojové exporty uvádějí „LiDAR © ČÚZK“. Odborná metadata a licenční podmínky je nutné dále ověřovat. Levý Hradec již nabízí samostatný uzavřený STL model pro 3D tisk v archivu ZIP (7 753 985 B), složeném a ověřeném pomocí SHA-256 při stažení. Archiv je uložen po částech v `assets/downloads/levy-hradec/` a popsán souborem `manifest.json`. Další tiskové modely STL/3MF jsou zatím v přípravě.

## Cloudflare Pages

- Repository: `ZemanAnt/mapova-archeologie`
- Production branch: `main`
- Framework preset: `None`
- Build command: `exit 0`
- Build output directory: kořen repozitáře

Každý commit na `main` spustí nové nasazení v Cloudflare Pages, pokud je GitHub propojen s projektem.
