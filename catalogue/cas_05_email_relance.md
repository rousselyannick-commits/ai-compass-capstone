# CAS D'USAGE 05 — Email de relance et suivi d'affaires

## Description courte
Rédiger des emails de relance commerciale, de suivi d'offres, de
prise de nouvelles ou de réactivation de comptes, adaptés au stade
de la relation client et au niveau d'interlocuteur.

## Profils métier cibles
Commercial Travaux, Commercial Maintenance, Chargé d'affaires

## Mots-clés de détection
"relance", "email de suivi", "follow-up", "réactivation",
"prise de nouvelles", "courriel client", "mail commercial"

## Tâche actuelle (avant IA)
- Identification de l'objectif de la relance (information, échéance,
  proposition de RDV...)
- Rédaction d'un email court, professionnel et engageant
- Adaptation du ton au niveau d'interlocuteur et à l'historique
  relationnel
- Relecture et envoi

## Tâche avec IA encadrée
- L'utilisateur fournit le contexte minimal (étape, objectif, ton
  attendu)
- L'IA propose 2-3 variantes adaptées
- L'utilisateur choisit, ajuste, envoie

## Gain unitaire moyen estimé
- Temps actuel moyen : 10 à 20 minutes par email rédigé
- Temps avec IA encadrée : 3 à 7 minutes par email
- Gain net moyen : 7 à 13 minutes par email
- Hypothèse de calcul retenue : 65 % de gain moyen
- À noter : le gain unitaire est modeste, mais la FRÉQUENCE est très
  élevée (plusieurs emails par jour), donc l'impact cumulé est fort

## Source des estimations
Étude HubSpot 2024 sur l'IA générative dans les outils de vente :
gains de 60 à 70 % sur la rédaction d'emails commerciaux de relance.

## Formule de calcul du ROI personnalisé
Variables collectées auprès de l'apprenant :
- temps_actuel = temps moyen actuel pour un email de relance (minutes)
- frequence = nombre d'emails de relance par semaine

Calcul :
- gain_par_email = temps_actuel × 0,65
- gain_hebdo_minutes = gain_par_email × frequence
- gain_hebdo_heures = gain_hebdo_minutes / 60
- gain_annuel_heures = gain_hebdo_heures × 45 semaines
- gain_annuel_euros = gain_annuel_heures × 35 €

## Prérequis de formation
- Module 1 — Comprendre l'IA générative (obligatoire)
- Module 3 — RGPD et IA générative (obligatoire)
- Module 5 — Prompt engineering responsable (obligatoire)

## Points de vigilance RGPD et confidentialité
NIVEAU DE VIGILANCE : MODÉRÉ

L'email de relance contient typiquement nom de l'interlocuteur,
contexte de l'affaire, parfois éléments commerciaux (prix, délais).

Pratiques sécurisées :
- Anonymiser le nom du destinataire dans le prompt ("M. X",
  "responsable Y")
- Limiter le contexte commercial transmis au strict nécessaire
- Ne pas coller d'historique d'échanges complets
- Conserver la signature et les éléments DEF Ouest dans l'email
  final, hors prompt

À ne pas faire :
- Coller l'historique complet d'échanges avec le client
- Mentionner des montants précis d'offres dans le prompt
- Utiliser l'IA pour des emails à forte sensibilité relationnelle
  (litige, réclamation) sans relecture très critique

## Classification AI Act
Risque limité — Assistance à la rédaction.

## Recommandation d'outil
Claude (interface entreprise) ou ChatGPT Enterprise.

## Prompt type proposé à l'apprenant
"Tu es assistant à la rédaction d'emails commerciaux pour DEF Ouest.
Rédige-moi un email de relance court (8 à 12 lignes), professionnel
et engageant, avec un objet pertinent.
Contexte : [étape de la relation, dernier échange, objectif de la
relance]. Ton souhaité : [formel / chaleureux / direct]. Pas de
formulation excessive, va à l'essentiel. Termine par une question
ouverte ou une proposition d'action claire."
