# Mapová archeologie – 3D atlas českých hradišť

Web publikovaný pomocí Cloudflare Pages z větve `main`.

## Aktivní modely
- [Divoká Šárka](lokality/divoka-sarka.html) – skutečný vložený 3D reliéf, původní rozšířený prohlížeč a měřicí nástroje.
- [Mařín](lokality/marin.html) – 3D reliéf z uživatelem dodaného exportu `oblast_3d.html`, lokalita přiřazena podle zadání.

Modely jsou bezeztrátově uložené po menších UTF-8 blocích v `assets/<slug>/part-NN.txt`. Stránky je v prohlížeči spojí do originálního autonomního HTML a vykreslí v iframe. Z výsledku lze stáhnout zdrojový model GLB a offline HTML.

Zdrojová data jsou dodaná uživatelem. Původní prohlížeče uvádějí „LiDAR © ČÚZK“. Odborná metadata, licenční režim a tisknutelné uzavřené modely STL/3MF vyžadují samostatnou kontrolu.

## Cloudflare Pages
- Repository: `ZemanAnt/mapova-archeologie`
- Production branch: `main`
- Framework preset: None
- Build command: `exit 0`
- Build output directory: kořen repozitáře
