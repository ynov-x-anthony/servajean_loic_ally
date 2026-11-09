# AUDIT.md : à compléter

## 1. Audits outillés

Lance les 3 audits sur la page (`npm run dev`, puis ouvre-la dans Chrome) et
colle ici un résumé de ce que chacun remonte :

- **Lighthouse** (DevTools → onglet Lighthouse → catégorie Accessibility) :
- **axe DevTools** (extension Chrome) :
- **WAVE** (https://wave.webaim.org/, ou l'extension) :

## 2. Les éléments à corriger

| Élément | Couleur texte | Couleur fond | Ratio mesuré | Ratio AA requis | Conforme ? |
|---------|---------------|--------------|--------------|------------------|------------|
| `.subtitle` | `#aaaaaa` → `#5c5c5c` | `#ffffff` | 2.3:1 → 6.7:1 | 4.5:1 | Oui (après) |
| `.label` | `#999999` → `#595959` | `#ffffff` | 2.9:1 → 7.0:1 | 4.5:1 | Oui (après) |
| `.hint` | `#bbbbbb` → `#595959` | `#ffffff` | 1.9:1 → 7.0:1 | 4.5:1 | Oui (après) |
| `.btn-primary` | `#ffffff` | `#6fa8dc` → `#1a5fa8` | 2.5:1 → 6.5:1 | 4.5:1 (texte) | Oui (après) |

> Utilise un vérificateur de contraste (ex. le picker de couleur de Chrome
> DevTools affiche déjà le ratio AA/AAA quand tu modifies une couleur).

## 3. Priorisation

Classe les 4 corrections par ordre d'impact (1 = le plus urgent) et explique pourquoi.

1. `.btn-primary` : c'est l'action principale, et le seul élément interactif.
2. `.hint` : ratio le plus bas (1.9:1), et c'est un conseil lié à la facturation.
3. `.label` : sert à identifier les valeurs (statut), à 2.9:1.
4. `.subtitle` : texte d'introduction, le moins critique (2.3:1), mais à corriger aussi.