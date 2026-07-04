# Landing page

Landing page produit pour Flux, une application de gestion de tâches pour équipes. Le projet est livré en un seul fichier HTML autonome (index.html), avec CSS intégré, sans dépendance externe hors polices Google Fonts.

Structure des sections


En-tête / Navigation — logo, liens d'ancrage, actions de connexion et d'essai
Hero — titre principal, accroche, boutons d'action, visuel de pile de cartes de tâches
Fonctionnalités — 3 colonnes illustrées d'une icône (Organiser, Collaborer, Suivre)
Témoignages — 3 avis clients sur fond sombre contrasté
Tarifs — 3 plans comparés (Essentiel, Équipe, Entreprise), plan du milieu mis en avant
Appel à l'action (CTA) — bandeau de conversion final
Pied de page — colonnes de liens, mentions légales


Système de design

Variables CSS (:root)

Toutes les valeurs de couleur, typographie, espacement et rayon de bordure sont centralisées en variables CSS, ce qui permet de changer l'identité visuelle du site en un seul endroit :

css--color-bg          /* fond général */
--color-surface      /* cartes et surfaces élevées */
--color-ink          /* texte principal */
--color-muted        /* texte secondaire */
--color-primary      /* couleur d'action (bleu électrique) */
--color-accent        /* couleur de mise en avant (chartreuse) */
--font-display        /* Space Grotesk — titres */
--font-body            /* Inter — texte courant */
--font-mono             /* JetBrains Mono — étiquettes/utilitaires */
--space-xs … --space-2xl  /* échelle d'espacement */
--radius-sm … --radius-lg /* échelle de rayons */

Typographie


Space Grotesk — titres et éléments de marque, pour une identité technique et affirmée
Inter — texte courant, optimisé pour la lisibilité



Techniques CSS avancées mises en œuvre

Reset personnalisé

Un reset minimal et ciblé (box-sizing, marges par défaut, listes, images, boutons, focus) plutôt qu'un reset générique complet, pour garder le contrôle sur la cascade.

Pseudo-classes


:nth-child() — pivote et décale chaque carte de la pile du hero, alterne le style des témoignages, met en avant le plan tarifaire du milieu
:first-of-type — distingue la première carte de fonctionnalité et le premier élément d'une liste de tarifs
:hover, :active, :focus-visible — états interactifs cohérents sur tous les boutons et liens


Maîtrise de la spécificité


Une seule classe de base par composant (.btn, .feature-card, .plan-card…) avec des modificateurs (.btn--primary, .btn--ghost) plutôt que des sélecteurs imbriqués profonds
Aucun sélecteur d'ID utilisé pour le style
Aucune déclaration !important
Les variantes de contexte (plan tarifaire mis en avant, témoignage alterné) sont gérées par pseudo-classes plutôt que par des classes supplémentaires, pour éviter les conflits de cascade


Utilisation

Ouvrir directement index.html dans un navigateur.

Personnalisation rapide

Pour adapter le design à un autre produit :


Modifier les valeurs dans :root (couleurs, polices, espacements)
Remplacer les textes des sections (hero, fonctionnalités, témoignages, tarifs)
Ajuster les icônes SVG des fonctionnalités si nécessaire


Structure du fichier

flux-landing.html
├── <style>
│   ├── 1. Reset personnalisé
│   ├── 2. Variables CSS
│   ├── 3. Base (typographie, boutons, conteneur)
│   ├── 4. En-tête / Navigation
│   ├── 5. Hero
│   ├── 6. Fonctionnalités
│   ├── 7. Témoignages
│   ├── 8. Tarifs
│   ├── 9. Appel à l'action
│   └── 10. Pied de page
└── <body>
    ├── <header>
    ├── <main>
    │   ├── <section class="hero">
    │   ├── <section class="features">
    │   ├── <section class="testimonials">
    │   ├── <section class="pricing">
    │   └── <section class="cta-banner">
    └── <footer>
