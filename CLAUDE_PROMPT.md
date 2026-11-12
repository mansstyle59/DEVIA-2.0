# PROMPT — TERMINER DEVIA 2.0

Agis comme architecte logiciel senior, développeur full-stack, expert UX mobile, sécurité et performance. Audite puis fais évoluer ce starter vers une application SaaS professionnelle de devis pour artisans.

## Design
- Parcours : tableau de bord, devis vocal, analyse IA, détail et chiffrage, PDF, signature, clients, catalogue, factures, suivi chantier et rentabilité.
- Logo SVG fourni dans assets/mark.svg. Fond #0F0C1D, surfaces #17142B et #211B3B, violet #6A56F5 / #3D2BC4, texte blanc et accents mauves.
- Layout mobile et desktop réellement distincts. Respect strict iPhone : viewport-fit=cover, env(safe-area-inset-*), navigation basse opaque, aucun header translucide.
- Dépôt DEVIA indépendant : ne touche à aucun autre projet GitHub.

## Méthode
1. Audite les fichiers et liste les problèmes avant modification.
2. Décris l'architecture cible (pages, composants, modèles, services, stockage) avant refonte.
3. Préserve ce qui fonctionne et avance par étapes avec tests.
4. N'invente ni prix, ni règles fiscales, ni mentions légales. Affiche les hypothèses et demande validation.
5. Aucune clé API, aucun secret ni jeton dans le frontend ou Git.
6. Sans clé IA ou si quota dépassé, l'application reste utilisable en mode manuel.
7. Validation humaine obligatoire pour quantités, prix, TVA et devis avant envoi.

## Fonctionnalités
P0 : authentification, profil entreprise, clients, devis, numérotation, lignes et TVA configurables, catalogue personnalisable, PDF, sauvegarde persistante, contrôle d'accès.
P1 : dictée vocale française, IA qui propose prestations/unités/quantités, questions de clarification, validation des prix, analyse photo après consentement, signature, factures et acomptes.
P2 : chantiers, marge, rentabilité, prix régionaux sourcés et datés, relances, partage sécurisé, mode hors ligne et synchronisation.

## Architecture cible
Frontend TypeScript, Cloudflare Pages, API côté serveur / Cloudflare Workers, Supabase Auth/PostgreSQL/Storage avec RLS vérifié, documents privés par URL temporaire, fournisseur IA interchangeable côté serveur. Explique les coûts avant toute architecture lourde.

## Qualité
JavaScript initial léger, dépendances limitées, validation client et serveur, protections XSS/CSRF adaptées, contrôle d'accès, accessibilité, pas de débordement horizontal iPhone, tests unitaires des calculs et tests de parcours, contrôle console. Pas de secrets côté navigateur.

Ordre : audit/corrections, modèles et tests, devis/PDF, auth/base, dictée/IA, signature/facturation, sécurité/conformité/tests/déploiement. À chaque étape, liste fichiers modifiés, tests exécutés, résultats, limites et instructions de déploiement.