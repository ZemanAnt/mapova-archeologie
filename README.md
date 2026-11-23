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

U tří lokalit používá katalog náhledy skutečného reliéfu odvozené z dat přiložených GLB modelů: `assets/thumbnails/*.svg`. Stará Kouřim má zatím označený grafický náhled; skutečný model je v prohlížeči. Závist má zatím jen jasně označený dekorativní motiv.

## Princip publikování

Původní autonomní 3D HTML exporty jsou velké (přibližně 17–19 MB). Z důvodu snadnější správy jsou uložené po částech v `assets/<lokalita>/part-NN.txt`. Stránky příslušných lokalit tyto soubory stáhnou, spojí a vykreslí v iframe. V prohlížeči lze stáhnout původní HTML a GLB. Měřicí funkce pocházejí z dodaných exportů.

- Divoká Šárka: `divoka_sarka_3d.html`
- Stará Kouřim: `kourim_3d.html` (vložený skutečný export, použit také jako výchozí demo na hlavní straně)
- Mařín: `oblast_3d.html` (interní název „Oblast“, přiřazení k Mařínu není samotným souborem prokázáno)
- Levý Hradec: `levy_hradec_3d(1).html`

Zdrojové exporty uvádějí „LiDAR © ČÚZK“. Odborná metadata, licence a tisknutelné uzavřené modely STL/3MF je potřeba řešit samostatně. Web nenabízí dosud neexistující tiskové soubory.

## Cloudflare Pages

- Repository: `ZemanAnt/mapova-archeologie`
- Production branch: `main`
- Framework preset: `None`
- Build command: `exit 0`
- Build output directory: kořen repozitáře

Každý commit na `main` spustí nové nasazení v Cloudflare Pages, pokud je GitHub propojen s projektem.
