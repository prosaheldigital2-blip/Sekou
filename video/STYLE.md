# Charte vidéo — format vertical

Base commune à toutes les vidéos HyperFrames du projet. Chaque vidéo a ensuite son propre `SPEC.md` (sujet, plans, texte) qui reprend ces valeurs.

## Format

- 1080 × 1920, 30 fps.
- Durée : 30 à 45 s, soit 900 à 1350 images.
- Image 0 = miniature et accroche : une phrase forte déjà à l'écran, jamais un écran noir ni un logo.

## Couleurs

| Rôle | Hex | Usage |
|---|---|---|
| Fond | `#0A0A0A` | Fond plein, sans dégradé, sans halo. |
| Texte | `#FFFFFF` | Tout texte à lire. |
| Accent | `#D97757` | **Un seul élément par plan** : le mot surligné du sous-titre, un chiffre, un trait. Jamais en fond de grande surface. |

Le fond sombre ne doit jamais rester vide : l'élément principal de chaque plan occupe au moins 40 % de la largeur ou de la hauteur.

## Polices (incluses dans HyperFrames)

- **Titres : Archivo Black**, 400. Taille 120–160 px, interlettrage −2 %, au plus 5 mots par ligne. Si ça ne rentre pas : on coupe des mots, on ne réduit jamais la taille.
- **Texte courant : Inter**, 700 pour les sous-titres, 400 pour le reste. Jamais sous 40 px.

## Zones de sécurité (TikTok, Reels, Shorts)

- Tout texte et tout élément important dans la zone **x 120 → 888 px, y 288 → 1248 px**. En dessous de y 840, le bord droit recule à x 780 (barre d'actions de TikTok) : zone x 120 → 780.
- Marge minimale de 120 px avec les bords : rien n'est collé au bord.
- Hors de cette zone : uniquement de la texture ou de la décoration, jamais du texte.

## Sous-titres

- Position : en bas de la zone de sécurité, **bord bas du sous-titre à y = 1248 px**. Plus bas, la légende et les boutons de l'application les recouvrent.
- Inter 700, taille de base 78 px (minimum 56 px), ajustée par groupe avec `fitTextFontSize`, largeur max 660 px (zone x 120 → 780 à cette hauteur).
- Groupes de 2 à 3 mots, un seul groupe visible à la fois. Premier groupe à 0,2 s, pas à 0.
- Le mot important de chaque groupe : couleur `#D97757` et échelle 1,12. Un seul mot surligné par groupe.
- Entrée du groupe : 0,15 s, `power3.out`, montée de 24 px. Sortie : 0,12 s, `power2.in`, puis masquage net.

## Rythme

- Un nouvel élément toutes les 0,5 à 1 s (15 à 30 images).
- Aucune image fixe plus de 2 s (60 images) : à 2 s au plus, un élément entre, sort ou change.
- Changement de mise en page toutes les 2 à 4 s.

## Animations

- Entrées : 0,25–0,35 s (8–10 images), `power3.out`, déplacement de 40–60 px ou échelle 0,92 → 1.
- Sorties : 0,15–0,2 s, `power2.in`, plus courtes que les entrées.
- Décalage entre éléments d'un même plan : 0,08–0,12 s.
- Un seul mouvement principal par plan ; les mouvements secondaires font 50–70 % de la distance et partent 0,1–0,2 s après.
- Un texte ne bouge plus une fois posé, pendant qu'on le lit.

## Interdits

- Effets gadgets : rebonds exagérés, rotations, tremblements, effets glitch, machine à écrire lettre par lettre.
- Halos, néons, lueurs, particules, dégradés violets ou bleus, cartes en verre.
- Tout qui entre en même temps ; tout qui entre en fondu vers le haut de la même façon.
- Texte sous 40 px ; texte hors de la zone de sécurité ; éléments à moins de 120 px d'un bord.
- Logo calé dans un coin ; cadres, crochets d'angle ou étiquettes décoratives.
