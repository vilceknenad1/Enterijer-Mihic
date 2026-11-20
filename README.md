# Enterijer Mihić — sajt

Sajt: https://vilceknenad1.github.io/Enterijer-Mihic/

Jedna stranica, bez build koraka. Sve što je potrebno za sajt je `index.html` i folder `assets`. Posle svakog push-a na `main` GitHub Pages osveži sajt za minut-dva.

## Gde je šta

| Fajl | Šta je u njemu |
|---|---|
| `index.html` | Sav tekst i raspored stranice |
| `assets/js/config.js` | Telefon, Instagram, adresa za prijem upita |
| `assets/css/main.css` | Boje, fontovi, raspored |
| `assets/js/main.js` | Meni, galerija, uvećavanje slika, obrazac |
| `assets/js/fx.js` | Animacije (GSAP i Lenis, učitavaju se sa cdnjs i jsDelivr) |
| `assets/img/` | Fotografije u tri veličine (800, 1200, 1600 px) |
| `tools/` | Skripte za pripremu slika i spisak izvora fotografija. Sajtu nisu potrebne. |

## Šta još nedostaje

**Prijem upita.** Obrazac proverava unos, ali poruke još nigde ne stižu. Dok se to ne podesi, posetilac dobije poruku da slanje nije aktivno i da pozove +381 65 911 4646. Najlakše je preko besplatnog naloga na formspree.io: napravite formu, a dobijeni link (`https://formspree.io/f/...`) upišite u `config.js` kao `formEndpoint`. Formspree na besplatnom paketu ne prima priložene fotografije, pa tada postavite `acceptsFiles: false`.

**E-mail i politika privatnosti.** Upisuju se u `config.js` (`email`, `privacyPolicyUrl`). Dok su prazni, ne prikazuju se.

## Fotografije

Fotografije su sa Instagram profila @enterijer_mihic, sa blago ujednačenom bojom i isečenim ivicama. Spisak objava je u `tools/IZVOR-FOTOGRAFIJA.md`.

Nova fotografija u galeriji:

1. Napravite tri verzije u WebP formatu, široke 800, 1200 i 1600 px, i nazovite ih npr. `rnovakuhinja-800.webp`, `rnovakuhinja-1200.webp` i `rnovakuhinja-1600.webp`. Stavite ih u `assets/img/`.
2. U `index.html`, u sekciji `#nasi-radovi`, kopirajte jedan blok `<figure class="g-item">`.
3. Promenite naziv slike, `alt` tekst, `data-title` i `data-cat` (`kuhinje`, `plakari`, `dnevne`, `spavace` ili `ostalo`).

Galerija je mreža od 4 kolone, pa izgleda najurednije kada je broj fotografija deljiv sa 4. Brojači u filterima se ažuriraju sami.

## Animacije

Ako posetilac u sistemu ima uključeno smanjenje pokreta, ili se biblioteke za animacije ne učitaju, sajt se prikazuje bez animacija i sav sadržaj ostaje vidljiv. Uvodna animacija se prikazuje samo pri prvoj poseti u toku jedne sesije.
