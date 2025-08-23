---

title: "Notre Magasin de fichiers + audit critique"
author: ouaisfi.eu
date: 2025-08-22
description: "Retour d’expérience sur le projet « Magasin de fichiers » : points forts, limites et recommandations concrètes pour une diffusion publique propre via Hugo/FixIt."
categories: ["Outils"]
tags: []
type: posts
images:
  - "https://dl.ouaisfi.eu/1160/images/jason-manifest-json.jpg"
---



> Un **catalogue 100 % statique** qui s’appuie uniquement sur `index.html` + `manifest.json` : aucune base de données, déploiement instantané sur GitHub Pages.&#x20;


<div style="text-align: center;">
  <img src="/1160/images/magasin.jpg" alt="Performances PageSpeed Insights" style="max-width: 80%; height: auto; border-radius: 12px;"  />
</div>

<p>
<a class="btn primary" href="https://ouaisfieu.github.io/magasin/" target="_blank" rel="noopener">▶️ Démo en ligne</a>
&nbsp; &nbsp;
<a class="btn" href="https://github.com/ouaisfieu/magasin" target="_blank" rel="noopener">🛠️ Dépôt GitHub</a>
</p>

---

## Pourquoi ce projet ?

* **Mettre en valeur notre corpus** de textes, kits et visuels — consultables en un clic, avec recherche, tags, tri et aperçus.
* **Donner envie de faire pareil** : forker, remplacer le manifeste par ses propres ressources, publier.

---

## Le cœur : des contenus qui donnent envie de creuser

### 1) Citoyenneté & veille (pour comprendre et agir)

* **Kit Citoyen – Volet « Comprendre »** — remettre l’individu dans le collectif et ouvrir le champ de l’action.&#x20;
* **De l’Auftragstaktik à la participation consciente** — passer d’une culture du commandement à la décision distribuée.&#x20;
* **La citoyenneté, c’est le brol** — complexité, règles, papiers… et comment s’y retrouver.&#x20;
* **Veille citoyenne en FWB : enjeux & inclusion** — pourquoi « le regard citoyen » sur l’action publique compte.&#x20;

> Un ensemble cohérent pour lancer un **atelier de veille** : cadrage, outils et posture.&#x20;

### 2) Outillage & méthode (pour s’organiser)

* **Tutoriel Obsidian (débutant·e)** + **Guide Obsidian pas à pas** — bases PKM, workflow fichiers Markdown.&#x20;
* **Créer sa bibliothèque (tutoriel complet)** — structure, `manifest.json`, vignettes, déploiement.&#x20;
* **Légende des badges / Effets CSS (fx.css)** — micro-UI lisible (badges, surlignages) pour hiérarchiser les items.&#x20;

> Résultat : on passe **du stock dispersé** à une **bibliothèque navigable** et esthétique, sans framework lourd.&#x20;

### 3) Kits thématiques « ☯ » (à structurer pour le public)

* **☯ ASTRO – Kit Markdown** — 24 signes, planètes, éléments… un coffret pédagogique en .zip. *(À ouvrir/éditer avant diffusion publique.)*&#x20;
* **Autres kits (Émotions, Équipe, Introspection, Valeurs… )** — actuellement notés avec un **mot de passe en clair** dans le manifest → à retirer avant mise en avant publique.

### 4) Culture & société (pour alimenter le débat)

* **Échanges : de l’« intelligence » à la « stupidité » économique** — 5 ruptures pour comprendre nos dépendances.&#x20;
* **Pouvoir d’agir vs hégémonie** — l’information comme levier d’empouvoirement.&#x20;
* **Guerre économique & société civile** — dommages collatéraux des sanctions.&#x20;
* **Visuel « Smoke — Parce que fumer tue »** — message de santé publique percutant, à alléger côté poids d’image.&#x20;

---

## Ce que la démo montre bien

* **Simplicité** : le site charge le `manifest.json`, construit les cartes, applique recherche et tri (pertinence/récence).&#x20;
* **Aperçus confortables** : PDF/MD/vidéo/image en modal, avec fallback « Ouvrir/Télécharger ».&#x20;
* **Lisibilité** : badges, chips de tags, thème clair/sombre, clavier `/` pour chercher.&#x20;

---

## Répliquer en 3 étapes

1. **Forker** le dépôt → [github.com/ouaisfieu/magasin](https://github.com/ouaisfieu/magasin).
2. **Remplacer** les fichiers et **éditer** `manifest.json` (un item = `title`, `description`, `url`, `type`, `tags`, `created`, `thumb` …). Utilise les docs du dépôt (*guide bibliothèque, légende des badges, FAQ*).&#x20;
3. **Publier** avec GitHub Pages (branche `main` → `gh-pages` ou Pages projet). C’est tout.

> Astuce : garde des **chemins relatifs** dans le manifest pour rester portable sur GitHub Pages et sites en sous-répertoire.&#x20;

---

## Quelques conseils éditoriaux (avant diffusion large)

* **Retirer du manifest** toute mention de **mot de passe** ou d’information sensible.
* **Harmoniser les dates & titres** (ISO 8601, style clair), éviter les chemins absolus et les noms de fichiers avec espaces/emoji.&#x20;
* **Compresser les vignettes** (WebP/AVIF, ≤ 120 Ko) pour garder l’expérience fluide, surtout mobile.&#x20;
* **Corriger les métadonnées sociales** (`og:url` doit pointer vers la bonne URL de la démo).&#x20;

---

## En deux mots

Le **Magasin** est un **excellent gabarit** pour rendre des contenus **trouvables** et **désirables** en quelques minutes. La démonstration prouve que **performance, accessibilité et sobriété** peuvent rimer avec **plaisir de lecture**.
➡️ **Testez la démo**, piochez dans les **ressources citoyennes**, puis **réappropriez-vous** l’outil pour votre propre corpus.

<p>
<a class="btn primary" href="https://ouaisfieu.github.io/magasin/" target="_blank" rel="noopener">▶️ Ouvrir la démo</a>
&nbsp; &nbsp;
<a class="btn" href="https://github.com/ouaisfieu/magasin" target="_blank" rel="noopener">🛠️ Cloner le dépôt</a>
</p>


# Pourquoi cet audit ?

Le **Magasin de fichiers** est une bibliothèque 100 % statique alimentée par un `manifest.json` et un unique `index.html`. L’interface offre recherche, filtres, aperçus et un basculement clair/sombre. L’objectif de cet article est de passer en revue **ce qui marche très bien**, **ce qui doit être corrigé en priorité**, et **les améliorations utiles à court terme**.

> Base d’analyse : le code fourni (`index.html`, `manifest.json`) et la version live. L’appli est pensée pour fonctionner *sans base de données* et charge le manifeste au runtime. &#x20;

---

## Ce qui fonctionne vraiment bien

* **Architecture minimaliste et portable.** Le couple `index.html` + `manifest.json` suffit ; l’index précharge le manifeste et construit l’UI en mémoire. C’est simple à déployer (GitHub Pages, dossier statique, etc.).&#x20;

* **Excellente performance perçue.**
  Le gabarit utilise `content-visibility:auto` + `contain-intrinsic-size` pour réduire le **CLS** sur les cartes, des vignettes `loading="lazy"`, et une grille responsive — de bons choix pour atteindre 100/100 en perf mobile.&#x20;

* **Recherche et tri utiles.**
  Normalisation des accents (NFD + strip diacritics) pour des recherches « à la française » plus tolérantes ; tri par pertinence, date, taille et titre.&#x20;

* **Accessibilité soignée pour un projet front léger.**
  Libellés ARIA sur les blocs, puces *chips* accessibles au clavier (`role="button"`, `aria-pressed`) et modal fermable au clic hors contenu.&#x20;

* **Design cohérent dark/light.**
  Variables CSS, `meta color-scheme`, bascule de thème persistée en `localStorage`.&#x20;

---

## Limites et risques (priorité haute)

1. **Chemins incohérents dans le manifeste.**
   Mélange d’URLs **absolues** (`/pdfs/...`, `/☯ VALEURS.zip`) et **relatives** (`pdfs/Article-PKM.pdf`, `images/smoke.png`). Sur GitHub Pages (projet), les chemins commençant par `/` pointent vers la racine du domaine et risquent de **casser** en production. Standardiser **en relatif** ou calculer une base dynamique.&#x20;

2. **Caractères spéciaux et espaces dans les noms de fichiers.**
   Exemples : `Guide Obsidian pas à pas.pdf`, `☯ ASTRO.zip`. Ça rend les liens fragiles (encodage `%20`, UTF-8), surtout combiné à des chemins absolus. Renommer en *kebab-case* ASCII côté fichiers ou **URL-encoder systématiquement** côté manifeste.&#x20;

3. **Mot de passe exposé publiquement dans le manifeste.**
   Plusieurs items affichent *« Mot de passe : batman1234 »* dans `note`. C’est indexable et archivable ; si ce mot de passe protège vraiment une archive, il est **compromis**. À minima : supprimer la mention publique et placer l’info derrière une page interne authentifiée.&#x20;

4. **Métadonnées sociales incohérentes.**
   `og:url` pointe vers `https://dl.ouaisfi.eu/` alors que la démo est servie depuis un autre chemin (`…/magasin/`). Ça **désaligne** l’aperçu de partage et la canonicalité. Corriger `og:url` et ajouter `<link rel="canonical">`.&#x20;

5. **Dates farfelues qui biaisent le tri.**
   Des `created` en **1957** et **1980** faussent les tris par récence et jettent un doute éditorial. Garder des dates ISO réalistes ou laisser vide si inconnu.&#x20;

6. **Tonalité éditoriale hétérogène.**
   Mélange d’intitulés sérieux et de notes *private jokes* (tags « enfer », « damnation », *« Ça vaut pour toux et tousse ! »*). Pour un site public, créer des **collections** (public / labo) ou normaliser le ton.

---

## Points à améliorer (court terme)

### a) Robustesse des liens & encodage

* **Uniformiser les URLs** en relatif (recommandé pour GitHub Pages) :
  `"/pdfs/..."` → `"./pdfs/..."`, `"/☯ VALEURS.zip"` → `"./zips/valeurs.zip"`, etc.&#x20;

* **Éviter espaces/emoji dans les noms physiques** et les *thumbs* (ex. `thumbs/Hans Fritz.jpg`). Renommer côté dépôt et **réécrire** le manifeste.

* **Option code** : calculer une base automatiquement dans `index.html` et préfixer les URLs du manifeste si besoin.

### b) Accessibilité & UX

* Ajouter `aria-live="polite"` sur le compteur d’items pour annoncer les résultats filtrés. (La zone « Aucun élément… » utilise déjà `aria-live` : bien vu.)&#x20;
* Prévoir un **fallback** d’aperçu PDF (certains mobiles bloquent l’embed) : lien « Ouvrir » mis en avant quand l’iframe échoue.&#x20;
* Limiter la **taille des vignettes** (ex. image > 1,6 Mo) : viser ≤ 120 Ko, WebP/AVIF, largeur 960–1280 px.&#x20;

### c) SEO & partage

* Corriger `og:url`, ajouter `og:image` (vignette générique du Magasin), `twitter:card`, `<meta name="theme-color">`.&#x20;
* Si l’objectif est la **découvrabilité** des *items* par moteur de recherche, envisager un **générateur** de pages HTML statiques (une page par item) en plus de l’index JS (le manifeste contient déjà titre/desc/tags).&#x20;

### d) Gouvernance éditoriale

* Définir un **schéma de nommage** (titre, tags, badges, dates) et s’y tenir ; c’est déjà amorcé avec un *schema JSON* présent dans la bibliothèque — excellent réflexe.&#x20;
* Séparer **public** (contenus finalisés) et **interne/bêta** (scripts, docs de travail) via un tag *collection* ou deux manifestes distincts.

---

## Recommandations concrètes

### 1) Front-matter social propre (dans `index.html` ou layout Hugo)

```html
<link rel="canonical" href="https://ouaisfieu.github.io/magasin/">
<meta property="og:url" content="https://ouaisfieu.github.io/magasin/">
<meta property="og:title" content="Magasin de fichiers – ouaisfi·eu">
<meta property="og:description" content="Catalogue statique : recherche, tags, aperçus, téléchargements.">
<meta property="og:type" content="website">
<meta name="theme-color" content="#0b0c0f">
```

> Remplacez les URLs par le domaine définitif dès que fixé. L’`og:url` actuel pointe vers un autre hôte.&#x20;

### 2) Exemple d’item **robuste** à utiliser comme modèle

```json
{
  "id": "guide-obsidian-debutant",
  "title": "Guide Obsidian pour débutant·e",
  "description": "Pas à pas : prise de notes, graph view, organisation.",
  "url": "./pdfs/guide-obsidian-debutant.pdf",
  "type": "pdf",
  "size": 71650,
  "tags": ["guide", "obsidian"],
  "created": "2025-07-29",
  "thumb": "./thumbs/obsidian-guide.webp",
  "badges": ["star"]
}
```

**Règles appliquées** : chemins relatifs, noms ASCII en *kebab-case*, date réaliste (ISO 8601), vignette optimisée, badges sobres. (Les exemples actuels montrent l’intérêt des badges mais cumulent caractères spéciaux et chemins absolus.)&#x20;

### 3) Nettoyage « grand public »

* Retirer les mots de passe du manifeste et des notes.&#x20;
* Retirer ou déplacer les entrées « labo/privées » (`enfer`, `damnation`, dates 1957/1980) vers un manifeste séparé.&#x20;
* Harmoniser les descriptions (80–160 car.) et les *tags* (liste fermée).

---

## Verdict

Un **très bon socle** : interface claire, performances exemplaires, recherche utile, design propre. Les principaux écueils tiennent **au manifeste** (chemins, encodage, mots de passe, dates) et à quelques **métadonnées sociales**. En corrigeant ces points, le Magasin devient un **template solide** pour publier des bibliothèques de ressources versionnées et partageables.

---

## Check-list rapide pour la prochaine release

* [ ] Tous les `url`/`thumb` en **relatif** et sans espace/emoji.&#x20;
* [ ] Suppression des **mots de passe** du manifeste.&#x20;
* [ ] Dates `created` réalistes (ISO).&#x20;
* [ ] `og:url` corrigé (+ canonical, twitter card).&#x20;
* [ ] Vignettes compressées (≤ 120 Ko, WebP/AVIF).&#x20;
* [ ] `aria-live` sur le compteur de résultats.&#x20;

---

### Notes techniques repérées dans le code

* Anti-CLS sur les cartes : `content-visibility:auto; contain-intrinsic-size:320px 300px;` ✔︎&#x20;
* Recherche tolérante aux accents : normalisation NFD + strip diacritics ✔︎&#x20;
* Tri par pertinence puis récence par défaut ✔︎&#x20;
* Aperçu modal : image/vidéo/audio/PDF/MD, fallback sur « ouvrir/télécharger » ✔︎&#x20;
* Limitation des **chips de tags** aux 24 plus fréquents (évite le bruit) ✔︎&#x20;

---




{{< link "https://dl.ouaisfi.eu/" "Magasin de fichiers en action" "Notre corpus" true "fa-solid fa-newspaper" >}}
