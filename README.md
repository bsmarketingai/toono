# toono – e-shop (prototyp)

Živý návrh e-shopu značky **toono** (ručně šitý kapsulový šatník). Návrh a prototyp zároveň: čisté HTML + CSS + JS bez závislostí, postavené na knihovně komponent BSSHOP. Struktura vychází z [roncato.cz](https://www.roncato.cz), vizuál z brand manuálu toono.

- Živý náhled: https://claude.ai/artifact/TV3uYtmUP54pbfVhD5MTA7
- Spuštění lokálně: otevřít `index.html` v prohlížeči (nebo `npx serve .`)

## Struktura

```
index.html          celý web (stránky řízené přes #hash)
img/                fotografie (ilustrační, viz img/zdroje.json)
assets/             logo a symbol „oo“ (SVG, vektorizováno z brand manuálu – nahradit master SVG)
docs/KOMPONENTY.md  mapování na knihovnu BSSHOP
docs/ZADANI.md      zadání, stav a chybějící podklady
```

## Stránky (hash routing)

| Stránka | URL |
|---|---|
| Úvod | `#home` |
| Kolekce / kategorie | `#kolekce`, `#topy`, `#spodni-dily`, `#saty`, `#vrstvy` |
| Detail produktu | `#produkt-top`, `#produkt-kalhoty`, `#produkt-sukne`, `#produkt-saty`, `#produkt-kardigan` |
| Košík (4 kroky, 1:1 podle roncato.cz) | `#kosik`, `#kosik-doprava`, `#kosik-udaje`, `#kosik-kontrola` |
| Příběh toono (O značce) | `#pribeh` |
| Inspirace | `#inspirace` |
| Dárkové poukazy | `#darkove-poukazy` |
| Deník | `#denik`, `#denik-kapsle-podzim`, `#denik-velikost`, `#denik-pece` |

## Tokeny

Barvy a písma jsou CSS proměnné na `:root` (`--c-*`, `--font-*`) podle knihovny BSSHOP. Hlavní barvy: Espresso `#3C2F28`, Ivory `#F6F2EB`, Terracotta `#C06F56` (text `#9A4F3A`), Wine `#6B2C3A`, Blush `#E9C1BC`. Písma: EB Garamond (nadpisy, místo Cormorant Garamond kvůli české diakritice), Montserrat (texty).

## Poznámky k implementaci

- Data produktů jsou v poli `P` v `index.html` – ceny a texty `[ ]` doplnit z Pohody.
- Tlačítko „▶ Přehrát intro“ vlevo dole je jen pro náhled – před spuštěním odstranit (`#devIntro`).
- SizeID: tlačítka připravena (`data-sizeid`), widget napojit po založení účtu na sizeid.com.
- Video: místa připravena (`data-video`), videa dodat po natáčení (konec listopadu 2026).
- Fotografie jsou ilustrační (AI), na ostrém webu musí věrně odpovídat skutečnému oblečení.
