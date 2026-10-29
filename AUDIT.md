# AUDIT.md : à compléter

Pour chaque ligne, retrouve le problème correspondant dans `src/App.tsx` / `src/App.css`
et remplis les 3 colonnes. Il y a **6 problèmes volontaires** dans ce starter.

| # | Problème trouvé (où, quoi) | Principe WCAG (P / O / U / R) | Pourquoi c'est bloquant, et pour qui |
|---|------------------------------|-------------------------------|----------------------------------------|
| 1 | `src/App.tsx` : `<img src="/hero.jpg" />` n'a pas d'attribut `alt`. | Perceptible (P) | Un lecteur d'écran ne peut pas décrire l'image ; elle est invisible pour une personne aveugle. |
| 2 | `src/App.tsx` : le `h1` est suivi directement d'un `h3`, sans `h2`. | Robuste (R) | La hiérarchie des titres sert à naviguer rapidement dans la page ; un saut de niveau perturbe cette navigation. |
| 3 | `src/App.tsx` : `<div className="see-more" onClick>` est utilisé au lieu d'un bouton. | Opérable (O) | Le contrôle est inaccessible au clavier (pas de `tabIndex` ni de gestion d'Entrée/Espace) et est annoncé comme du texte brut, pas comme un contrôle. |
| 4 | `src/App.tsx` / `src/App.css` : le bandeau `.carousel` s'affiche sans moyen de le fermer ou de le mettre en pause. | Opérable (O) | Selon WCAG 2.2.2, l'utilisateur doit pouvoir maîtriser le contenu qui apparaît. |
| 5 | `src/App.tsx` : les trois liens utilisent le même texte « cliquez ici ». | Compréhensible (U) | Le texte d'un lien doit avoir du sens hors contexte ; les personnes qui naviguent par liste de liens avec un lecteur d'écran ne peuvent pas les distinguer. |
| 6 | `src/App.tsx` / `src/App.css` : le statut « annulé » ou « publié » est indiqué uniquement par la couleur du point (`dot-red` / `dot-green`). | Perceptible (P) | L'information ne doit pas reposer uniquement sur la couleur ; elle peut être inaccessible aux personnes daltoniennes ou sur un écran en noir et blanc. |

> Rappel : P = Perceptible, O = Opérable, U = Utilisable (Compréhensible), R = Robuste.
