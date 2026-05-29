# CAS D'USAGE 01 — Compte rendu de visite prospect ou client

## Description courte
Rédiger un compte rendu structuré et exploitable après une visite
commerciale ou technique chez un prospect ou un client, à partir de
notes brutes prises pendant l'échange.

## Profils métier cibles
Commercial Travaux, Commercial Maintenance, Chargé d'affaires

## Mots-clés de détection
"compte rendu", "CR de visite", "visite client", "visite prospect",
"rendez-vous", "rendre compte d'une visite", "synthèse d'entretien"

## Tâche actuelle (avant IA)
- Reprise des notes manuscrites ou des notes prises sur smartphone
  pendant ou juste après la visite
- Mise au propre dans le modèle Word DEF Ouest
- Structuration en sections (contexte, interlocuteurs, besoins identifiés,
  prochaines étapes)
- Relecture et envoi à la hiérarchie / mise en GED

## Tâche avec IA encadrée
- L'utilisateur dicte ou saisit ses notes brutes dans un format libre
- L'IA structure automatiquement en sections standard DEF Ouest
- L'IA propose une formulation professionnelle, neutre, exploitable
- L'utilisateur relit, ajuste, valide et envoie

## Gain unitaire moyen estimé
- Temps actuel moyen : 30 à 45 minutes par compte rendu
- Temps avec IA encadrée : 10 à 15 minutes par compte rendu
- Gain net moyen : 20 à 30 minutes par compte rendu
- Hypothèse de calcul retenue : 60 % de gain en moyenne sur cette tâche

## Source des estimations
Étude McKinsey 2024 "The economic potential of generative AI" :
gains de 50 à 70 % observés sur les tâches de mise en forme et de
structuration de texte court à partir de matière première brute.
Ajustement DEF Ouest : -10 % de prudence pour tenir compte du contexte
PME et de la courbe d'apprentissage initiale.

## Formule de calcul du ROI personnalisé
Variables collectées auprès de l'apprenant :
- temps_actuel = temps moyen actuel pour un compte rendu (minutes)
- frequence = nombre de comptes rendus par semaine

Calcul :
- gain_par_cr = temps_actuel × 0,60
- gain_hebdo_minutes = gain_par_cr × frequence
- gain_hebdo_heures = gain_hebdo_minutes / 60
- gain_annuel_heures = gain_hebdo_heures × 45 semaines
- gain_annuel_euros = gain_annuel_heures × 35 € (coût chargé moyen)

## Prérequis de formation
- Module 1 — Comprendre l'IA générative (obligatoire)
- Module 3 — RGPD et IA générative (obligatoire, données contact client)
- Module 5 — Prompt engineering responsable (recommandé)

## Points de vigilance RGPD et confidentialité
NIVEAU DE VIGILANCE : MODÉRÉ

Le compte rendu contient des données personnelles professionnelles
(noms, fonctions, coordonnées des interlocuteurs rencontrés). Ces
données entrent dans le champ du RGPD même en contexte professionnel.

Pratiques sécurisées :
- Utiliser un outil IA maîtrisé par l'entreprise (Claude entreprise,
  ChatGPT Enterprise) — JAMAIS la version grand public
- Limiter les données saisies aux strictes nécessaires à la structuration
- Éviter de mentionner des informations sensibles non utiles au compte
  rendu (santé, situation familiale, opinions personnelles)
- Stocker le compte rendu final dans la GED DEF Ouest, pas dans
  l'historique de conversation de l'IA

À ne pas faire :
- Coller des fichiers entiers (cartes de visite scannées, fiches client
  complètes) dans un LLM
- Demander à l'IA de "deviner" des informations manquantes sur
  l'interlocuteur

## Classification AI Act
Risque limité — Assistance à la rédaction, non décisionnel.
Obligation de transparence : le compte rendu doit pouvoir être identifié
comme rédigé avec assistance IA si une question se pose en interne.

## Recommandation d'outil
Claude (interface entreprise) ou ChatGPT Enterprise.
Refus : ChatGPT version gratuite, Gemini grand public, Copilot personnel.

## Prompt type proposé à l'apprenant
"Tu es assistant à la rédaction de comptes rendus de visite pour un
commercial en sécurité incendie. À partir des notes brutes que je te
fournis, rédige un compte rendu structuré selon les sections :
1) Contexte de la visite, 2) Interlocuteurs, 3) Besoins identifiés,
4) Solutions évoquées, 5) Prochaines étapes. Ton professionnel, neutre,
sans interprétation. Conserve uniquement les informations utiles.
Notes brutes : [ICI LES NOTES]"
