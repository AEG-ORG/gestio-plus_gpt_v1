# Gestio+ — Prototype devis et factures

Code de la maquette Gestio+ : saisie clavier, catalogue, clients, devis et factures, trois présentations, TVA globale ou par ligne, impression et scanner de documents avec export PDF.

## Démarrer

Aucune compilation ni dépendance à installer. Ouvrez `index.html`, ou servez ce dossier avec `python -m http.server 8000`, puis ouvrez http://localhost:8000. La caméra et le partage dépendent des fonctions du navigateur ; utilisez HTTPS en ligne.

## Déposer sur GitHub

1. Créez un dépôt, par exemple `gestio-plus` (privé conseillé pendant le développement).
2. Décompressez l'archive sur votre ordinateur.
3. Dans le dépôt, choisissez **Add file → Upload files**.
4. Ajoutez les fichiers du dossier, avec `index.html` à la racine du dépôt, et validez le commit.

Ne téléversez pas simplement l'archive ZIP : GitHub doit recevoir les fichiers décompressés.

## Déployer sur Vercel

Importez le dépôt GitHub dans Vercel. Ce projet est un site statique : preset **Other**, pas de commande de build, répertoire de sortie `.`. Le fichier `vercel.json` contient également cette configuration. Les prochains commits de la branche de production pourront déclencher les déploiements Vercel.

## Variante GitHub Pages

Le workflow `.github/workflows/pages.yml` déploie ce dossier sur GitHub Pages. S'il a été ajouté au dépôt, sélectionnez **GitHub Actions** dans **Settings → Pages → Source**. Il fonctionne sur la branche `main` ou par lancement manuel. La disponibilité de Pages pour un dépôt privé dépend de votre offre GitHub. Si vous utilisez Vercel uniquement, ce workflow est facultatif.

## Données et limites

- Les données sont conservées localement dans le navigateur, pas dans Supabase.
- Le stockage n'est pas partagé entre téléphone, ordinateur ou navigateurs. Changer de domaine ne transfère pas les données existantes.
- Aucun compte utilisateur, serveur, secret ni clé API n'est inclus.
- Les coordonnées préremplies sont des exemples de démonstration.
- Le scanner travaille localement ; caméra, partage et téléchargement doivent être testés sur les appareils cibles.
- Cette archive reprend le prototype ; elle ne constitue pas une validation comptable ou réglementaire des factures.
- L'impression utilise la fenêtre du navigateur (choisir « Enregistrer au format PDF »).

## Vérifications conseillées après déploiement

Créer un devis, ajouter un article, changer de mode de TVA, enregistrer, recharger, imprimer en PDF et tester un scan. Les calculs et la numérotation doivent être validés avant utilisation réelle. Le raccordement sécurisé aux tables Supabase existantes sera une étape distincte.
