# CAS D'USAGE 10 — Rapport d'activité commerciale périodique

## Description courte
Produire un rapport d'activité commerciale hebdomadaire ou mensuel à
destination de la hiérarchie (responsable commerce, DG), synthétisant
les actions menées, les résultats obtenus et les perspectives.

## Profils métier cibles
Commercial Travaux, Commercial Maintenance, Chargé d'affaires

## Mots-clés de détection
"rapport d'activité", "reporting commercial", "rapport hebdo",
"rapport mensuel", "bilan d'activité", "compte rendu d'activité"

## Tâche actuelle (avant IA)
- Compilation des données d'activité (visites, offres envoyées,
  affaires gagnées/perdues, pipeline)
- Identification des faits marquants de la période
- Rédaction du commentaire de gestion
- Mise en forme dans le modèle de reporting DEF Ouest
- Diffusion à la hiérarchie

## Tâche avec IA encadrée
- L'utilisateur fournit les données brutes anonymisées de la période
- L'IA structure le rapport selon le format attendu
- L'IA rédige le commentaire de gestion à partir des données
- L'utilisateur ajoute son analyse qualitative et son ressenti
  terrain

## Gain unitaire moyen estimé
- Temps actuel moyen : 30 à 75 minutes par rapport (selon
  périodicité)
- Temps avec IA encadrée : 10 à 25 minutes par rapport
- Gain net moyen : 20 à 50 minutes par rapport
- Hypothèse de calcul retenue : 65 % de gain moyen
- Effet cumulé important : rapports hebdomadaires = 45 fois par an

## Source des estimations
Étude HubSpot 2024 sur l'IA dans les outils de reporting commercial :
gains de 60 à 75 % sur la production de rapports périodiques à
partir de données structurées.

## Formule de calcul du ROI personnalisé
Variables collectées auprès de l'apprenant :
- temps_actuel = temps moyen actuel pour un rapport (minutes)
- frequence = nombre de rapports par mois (4 si hebdo, 1 si mensuel)
- frequence_hebdo = frequence / 4,33

Calcul :
- gain_par_rapport = temps_actuel × 0,65
- gain_hebdo_minutes = gain_par_rapport × frequence_hebdo
- gain_hebdo_heures = gain_hebdo_minutes / 60
- gain_annuel_heures = gain_hebdo_heures × 45 semaines
- gain_annuel_euros = gain_annuel_heures × 35 €

## Prérequis de formation
- Module 1 — Comprendre l'IA générative (obligatoire)
- Module 3 — RGPD et IA générative (obligatoire)
- Module 5 — Prompt engineering responsable (obligatoire)

## Points de vigilance RGPD et confidentialité
NIVEAU DE VIGILANCE : MODÉRÉ

Un rapport d'activité commerciale contient des données clients
agrégées et des informations sur l'activité commerciale interne
(chiffres, prospects, pipeline).

Pratiques sécurisées :
- Anonymiser les noms de clients et prospects dans le prompt
  (utiliser des codes ou "Client A", "Prospect B")
- Limiter le détail des informations financières transmises
  (utiliser des fourchettes plutôt que des montants précis)
- Validation hiérarchique du contenu avant diffusion élargie
- Utiliser uniquement un outil IA maîtrisé entreprise

À ne pas faire :
- Coller des extracts CRM bruts ou des listes nominatives de
  prospects/clients
- Mentionner des montants d'affaires précis liés à des clients
  identifiables
- Faire produire par l'IA des prévisions commerciales engageantes
  sans validation

## Classification AI Act
Risque limité — Assistance à la rédaction et au reporting.
Note : pas d'usage RH des contenus produits (pas d'évaluation
individuelle automatisée des commerciaux par l'IA).

## Recommandation d'outil
Claude (interface entreprise) ou ChatGPT Enterprise.

## Prompt type proposé à l'apprenant
"Tu es assistant à la rédaction de rapports d'activité commerciale
pour un commercial en sécurité incendie. À partir des données
anonymisées que je te fournis, structure un rapport selon les
sections : 1) Synthèse de la période (3 lignes), 2) Activité
réalisée (visites, offres, affaires), 3) Résultats vs objectifs,
4) Faits marquants, 5) Perspectives et plan d'action pour la
prochaine période. Ton factuel et synthétique, orienté
hiérarchie. Reste sur les chiffres fournis, n'invente aucune donnée.
Données anonymisées : [ICI LES DONNÉES]"
