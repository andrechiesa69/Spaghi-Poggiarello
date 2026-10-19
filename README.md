# Il Poggiarello – Realtà Aumentata (MindAR multitarget)

## Contenuto
```
index.html              pagina AR
targets.mind            3 target: 0 = bottiglie, 1 = logo, 2 = social
assets/gutturniofronte.png
assets/ortrugofronte.png
assets/logopoggiarello.png
assets/fb.png
assets/ig.png
```

## Cosa succede
| Inquadri…             | Appare in AR                   | Al tocco apre |
|-----------------------|--------------------------------|---------------|
| Pagina bottiglie      | Gutturnio + Ortrugo sopra quelle stampate | pagine dei due vini |
| Logo Il Poggiarello   | Logo fluttuante                | /vini/ |
| Striscia social       | Icone Facebook e Instagram     | pagine social |

## Pubblicare su GitHub Pages
1. Su github.com crea un repository pubblico (es. `poggiarello-ar`).
2. **Add file › Upload files**: trascina `index.html`, `targets.mind` e la cartella `assets` (struttura identica a sopra) → **Commit**.
3. **Settings › Pages** → Source: *Deploy from a branch*, Branch: `main` / `(root)` → **Save**.
4. Dopo 1–2 minuti il sito è su `https://TUONOME.github.io/poggiarello-ar/`.
5. Crea il QR code con quell'indirizzo (qualsiasi generatore di QR) e stampalo nel libro.

## Note
- Serve https (GitHub Pages lo fornisce già). iPhone: Safari, iOS 15+; Android: Chrome.
- Aprire il QR con la fotocamera di sistema. Se si apre dentro Instagram/Facebook, la pagina avvisa di passare a Safari/Chrome.
- I target logo e social sono stati compilati dalle foto fornite. Per il massimo aggancio puoi ricompilarli dai file di stampa originali
  (https://hiukim.github.io/mind-ar-js-doc/tools/compile) caricando le 3 immagini **in questo ordine**: bottiglie, logo, social.
- Per spostare/ingrandire gli oggetti AR modifica l'array `TARGETS` in `index.html` (x, y, z, w).
- Logo, bottiglie e social sono sulla stessa pagina: la pagina riconosce fino a 3 target insieme.
  Inquadrando tutta la pagina si aggancia subito la parte con le bottiglie; per il logo e i social
  avvicina il telefono alla parte bassa della pagina (sono stampati piccoli).
