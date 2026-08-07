# WG Valeurs — Live

Page statique de suivi du fonds WG Valeurs (GitHub Pages).

- `index.html` — page autonome ; « Actualiser » recharge les cours BVC en direct
  (API BMCE Capital, CORS ouvert) dans le navigateur, même si la machine source
  est éteinte.
- `data/payload.enc` — snapshot + listings chiffrés AES-256-GCM (clé dérivée user:pass, PBKDF2 600k) publiés par
  `FamilyAgent/quant/wg_valeurs/publish_wg_live.sh` (launchd, toutes les 30 min
  en heures de bourse).
Aucune donnée en clair dans ce repo. Identifiants : `~/.config/wgvaleurs/credentials` sur la machine source.

Ne pas éditer `data/` à la main — régénéré à chaque publication.
