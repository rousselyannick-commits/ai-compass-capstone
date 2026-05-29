# CAS D'USAGE 07 — Présentation pour décideurs client

## Description courte
Construire une présentation (slides PowerPoint ou support de pitch)
destinée à des décideurs côté client (CODIR, responsables sécurité,
RSSI, direction technique) pour présenter une solution, faire un
point d'avancement ou défendre une recommandation.

## Profils métier cibles
Commercial Travaux, Chargé d'affaires Travaux, Responsables
techniques

## Mots-clés de détection
"présentation", "slides", "deck", "PowerPoint", "pitch décideurs",
"présenter au CODIR", "support de réunion", "réunion direction"

## Tâche actuelle (avant IA)
- Identification de l'enjeu et du message clé pour les décideurs
- Construction du plan de présentation (5 à 12 slides)
- Rédaction des titres, bullets et messages clés
- Mise en forme dans le modèle PowerPoint DEF Ouest
- Préparation du discours de présentation

## Tâche avec IA encadrée
- Description à l'IA du contexte (audience, objectif, message clé,
  durée prévue)
- L'IA propose un plan structuré adapté à un format décideurs
- L'IA rédige les titres et bullets clés pour chaque slide
- L'utilisateur met en forme dans le modèle PowerPoint
- L'utilisateur prépare et répète le discours associé

## Gain unitaire moyen estimé
- Temps actuel moyen : 120 à 240 minutes par présentation
- Temps avec IA encadrée : 40 à 90 minutes par présentation
- Gain net moyen : 80 à 150 minutes par présentation
- Hypothèse de calcul retenue : 60 % de gain moyen

## Source des estimations
Étude McKinsey 2024 et études Microsoft 365 Copilot 2024 : gains de
55 à 70 % sur la préparation de présentations à partir d'éléments
existants.

## Formule de calcul du ROI personnalisé
Variables collectées auprès de l'apprenant :
- temps_actuel = temps moyen actuel pour une présentation (minutes)
- frequence = nombre de présentations préparées par mois (puis
  converti en hebdo)

Calcul :
- gain_par_presentation = temps_actuel × 0,60
- gain_hebdo_minutes = (gain_par_presentation × frequence) / 4,33
- gain_hebdo_heures = gain_hebdo_minutes / 60
- gain_annuel_heures = gain_hebdo_heures × 45 semaines
- gain_annuel_euros = gain_annuel_heures × 35 €

## Prérequis de formation
- Module 1 — Comprendre l'IA générative (obligatoire)
- Module 5 — Prompt engineering responsable (obligatoire)
- Module 3 — RGPD et IA générative (recommandé)

## Points de vigilance RGPD et confidentialité
NIVEAU DE VIGILANCE : FAIBLE

La présentation est par nature un contenu structurant et synthétique,
adapté à un message à porter. Sauf cas particulier (présentation
ultra-personnalisée pour un décideur identifié), le risque RGPD est
limité.

Pratiques sécurisées :
- Décrire le contexte audience en restant générique (fonction, enjeu)
- Si la présentation porte sur un site client précis, anonymiser les
  éléments transmis à l'IA
- Vérifier la véracité de toute statistique, chiffre ou référence
  produite par l'IA

À ne pas faire :
- Demander à l'IA d'inventer des chiffres ou des statistiques
  "vraisemblables"
- Reproduire des éléments graphiques ou textuels concurrents
- Présenter des chiffres ou références sans avoir vérifié leur
  exactitude

## Classification AI Act
Risque limité — Assistance à la création de contenu.

## Recommandation d'outil
Claude (interface entreprise) ou ChatGPT Enterprise pour la structure
et le texte.
Pour la mise en forme graphique : conserver le modèle PowerPoint
DEF Ouest, ne pas générer de visuels par IA sans contrôle.

## Prompt type proposé à l'apprenant
"Tu es assistant à la préparation de présentations pour décideurs
clients dans le secteur de la sécurité incendie. Je dois présenter
[sujet de la présentation] à [type d'audience] pendant [durée].
L'objectif est de [objectif clair]. Propose-moi : 1) Un plan de
présentation en 7 à 10 slides, 2) Pour chaque slide : un titre fort
et 3 bullets de contenu, 3) Une slide de conclusion orientée action.
Ton orienté décideur (focus enjeu, ROI, risques, décision attendue).
Pas de jargon technique inutile. Reste factuel, n'invente pas de
chiffres."
