# Levý Hradec — model pro 3D tisk

Originální ZIP archiv `levy_hradec_tisk_pro_web.zip` (7753985 B) obsahuje `levy_hradec_tisk.stl` a `INFO_TISK.txt`.

Velikost archivu umožňuje ukládání přímo v repozitáři, ale kvůli limitům přenosu přes konektor GitHub byl rozdělen na 11 binárních částí: `part-00.bin` až `part-10.bin`.

Webový prohlížeč na `/lokality/levy-hradec.html` soubory stáhne, spojí v původním pořadí a prověří jejich kontrolní součet SHA-256 podle souboru `manifest.json`. Poté nabídne jediný ZIP ke stažení.

SHA-256 úplného ZIPu: `a20909b68f2688912bf6d61e46a4cb73aa457bedb2a627d877d876256440f14c`

**Pozor:** STL neobsahuje jednotky. Před tiskem ověřte předpokládané milimetry, velikost modelu, kvalitu vrstev a podmínky dalšího užití původních LiDAR dat.
