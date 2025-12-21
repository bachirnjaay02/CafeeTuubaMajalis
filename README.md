# Café Touba Majalis — Site de démonstration

Petit site statique (HTML + CSS + Bootstrap) pour commercialiser du café Touba moulu.

## Structure du projet

- `index.html` — page d'accueil (navbar, hero, produits, à propos, footer). Les boutons "Commander" ouvrent WhatsApp avec un message pré-rempli.
- `style.css` — styles personnalisés (palette blanc / marron, dégradé navbar, boutons, vidéos).
- `videoframe_cafee.mp4` (optionnel) — place ta vidéo ici ou modifie la balise `<source>` dans `index.html` pour pointer vers une URL publique.

## Modifier le numéro WhatsApp

Les boutons "Commander (WhatsApp)" utilisent le lien `https://wa.me/<numero>?text=...`.
Si tu veux changer le numéro, ouvre `index.html` et remplace `221778401904` par ton numéro (format international sans le `+`, par ex. `22177XXXXXXX`).

Exemple de lien formaté :
```
https://wa.me/221778401904?text=Bonjour%2C%20je%20souhaite%20commander%20... 
```

## Ajouter une vidéo pour `.videoframe`

1. Crée un fichier vidéo MP4 (optimisé web) et nomme-le `videoframe_cafee.mp4`, ou modifie le chemin dans la balise `<video>` de `index.html`.
2. Place le fichier à la racine du projet (même dossier que `index.html`) ou dans un sous-dossier (p. ex. `video/`) et mets à jour le chemin dans `<source src="...">`.

Remarque : les navigateurs autorisent l'autoplay seulement si la vidéo est muette. Le code actuel utilise `muted` et un petit script JS qui tente de lancer la lecture automatiquement.

## Ouvrir la page localement

Tu peux simplement double-cliquer sur `index.html` pour l'ouvrir dans ton navigateur. Pour un test plus fiable (et pour éviter certaines restrictions d'accès aux fichiers), tu peux lancer un petit serveur local.

Si tu as Python installé (recommandé), dans PowerShell va au dossier du projet et exécute :

```powershell
# depuis le dossier contenant index.html
python -m http.server 8000
# puis ouvre http://localhost:8000 dans ton navigateur
```

Ou, si tu as VS Code, installe l'extension "Live Server" et clique sur "Go Live".

## Test rapide après modifications

- Vidéo : assure-toi que la vidéo est nommée et placée correctement, puis recharge la page. Elle doit démarrer automatiquement (muette) et boucler.
- WhatsApp : clique sur un bouton "Commander (WhatsApp)" ; le lien doit ouvrir WhatsApp Web ou l'application mobile si utilisé depuis smartphone.

## Suggestions d'améliorations

- Ajouter un panier réel (stockage dans localStorage) et une page de commande.
- Intégrer un formulaire de contact côté serveur ou un service tierce pour recevoir les commandes par email.
- Ajouter des pages produit individuelles et des photos réelles des sachets.
- Ajouter des métadonnées SEO, favicon et optimisation des images/vidéos pour la performance.

## Licence

Contenu et code fournis sans licence explicite — tu peux les utiliser et modifier pour ton usage personnel. Si tu prévois une publication publique, pense à ajouter une licence formelle (MIT, CC-BY, ...).

---

Si tu veux, je peux :
- créer le dossier `video/` et y ajouter un exemple de source (URL publique commentée),
- automatiser la mise à jour du numéro WhatsApp en un seul endroit (variable JS) pour éviter modifications multiples,
- ou ajouter un petit script qui montre une notification (toast) avant d'ouvrir WhatsApp.

Dis-moi ce que tu préfères !