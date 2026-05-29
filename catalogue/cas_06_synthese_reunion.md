# CAS D'USAGE 06 — Synthèse de réunion technique avec client

## Description courte
Produire une synthèse exploitable d'une réunion technique avec un
client (réunion de chantier, point d'avancement, comité de pilotage
client, réunion de cadrage technique) à partir de notes prises
pendant l'échange.

## Profils métier cibles
Commercial Travaux, Chargé d'affaires Travaux, Commercial Maintenance

## Mots-clés de détection
"compte rendu de réunion", "CR réunion", "synthèse de réunion",
"réunion technique", "réunion de chantier", "point d'avancement"

## Tâche actuelle (avant IA)
- Reprise des notes prises en réunion (manuscrites ou tapées)
- Structuration en sections (participants, ordre du jour, points
  abordés, décisions, actions)
- Identification claire des actions, responsables et échéances
- Mise au propre dans le modèle DEF Ouest
- Diffusion aux participants pour validation

## Tâche avec IA encadrée
- L'utilisateur fournit ses notes brutes
- L'IA structure en sections standards
- L'IA extrait explicitement les actions, responsables, échéances
- L'utilisateur vérifie l'exactitude, ajuste, diffuse

## Gain unitaire moyen estimé
- Temps actuel moyen : 45 à 75 minutes par CR
- Temps avec IA encadrée : 15 à 25 minutes par CR
- Gain net moyen : 30 à 50 minutes par CR
- Hypothèse de calcul retenue : 60 % de gain moyen

## Source des estimations
Étude McKinsey 2024 et études sectorielles Notion 2024 sur la
production de comptes rendus assistée par IA : gains de 55 à 70 %
sur structuration et mise en forme.

## Formule de calcul du ROI personnalisé
Variables collectées auprès de l'apprenant :
- temps_actuel = temps moyen actuel pour un CR de réunion (minutes)
- frequence = nombre de CR de réunion par semaine

Calcul :
- gain_par_cr = temps_actuel × 0,60
- gain_hebdo_minutes = gain_par_cr × frequence
- gain_hebdo_heures = gain_hebdo_minutes / 60
- gain_annuel_heures = gain_hebdo_heures × 45 semaines
- gain_annuel_euros = gain_annuel_heures × 35 €

## Prérequis de formation
- Module 1 — Comprendre l'IA générative (obligatoire)
- Module 3 — RGPD et IA générative (obligatoire)
- Module 5 — Prompt engineering responsable (obligatoire)

## Points de vigilance RGPD et confidentialité
NIVEAU DE VIGILANCE : MODÉRÉ

Une réunion technique contient les noms et fonctions des
participants, parfois des informations techniques sur les
installations du client, occasionnellement des éléments financiers
ou stratégiques.

Pratiques sécurisées :
- Utiliser un outil IA maîtrisé entreprise
- Limiter les détails techniques sensibles dans les notes transmises
  (configuration précise d'installations, vulnérabilités identifiées)
- Anonymiser ou abréger les noms si la réunion porte sur un site
  particulièrement sensible
- Validation humaine systématique avant diffusion

À ne pas faire :
- Enregistrer la réunion sans accord explicite des participants
  (RGPD + droit à l'image et à la voix)
- Coller des informations techniques détaillées sur des
  vulnérabilités ou des configurations sécuritaires d'un site client
- Diffuser le CR généré sans relecture humaine

## Classification AI Act
Risque limité — Assistance à la rédaction.

## Recommandation d'outil
Claude (interface entreprise) ou ChatGPT Enterprise.

## Prompt type proposé à l'apprenant
"Tu es assistant à la rédaction de comptes rendus de réunion
technique pour un commercial en sécurité incendie. À partir de mes
notes brutes, structure un compte rendu professionnel selon les
sections : 1) Date et participants, 2) Objectif de la réunion,
3) Points abordés (avec décisions prises), 4) Plan d'action (avec
responsable et échéance pour chaque action), 5) Prochaine étape.
Reste factuel, n'invente aucune décision ou action non mentionnée
dans les notes.
Notes brutes : [ICI LES NOTES]"
