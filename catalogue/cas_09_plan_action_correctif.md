# CAS D'USAGE 09 — Plan d'action correctif post non-conformité

## Description courte
Construire un plan d'action correctif structuré suite à une
non-conformité identifiée chez un client (audit, contrôle commission
de sécurité, incident), à proposer au client pour mise en conformité.

## Profils métier cibles
Commercial Maintenance, Chargé d'affaires Travaux, Responsables
techniques

## Mots-clés de détection
"plan d'action", "plan correctif", "mise en conformité", "remise à
niveau", "actions correctives", "non-conformité", "préconisations"

## Tâche actuelle (avant IA)
- Identification des non-conformités à traiter (issues de l'audit
  ou du contrôle)
- Définition des actions correctives techniques (par type de
  non-conformité)
- Estimation des délais et coûts pour chaque action
- Hiérarchisation (urgences réglementaires vs améliorations)
- Mise en forme dans un document client professionnel

## Tâche avec IA encadrée
- L'utilisateur fournit la liste anonymisée des non-conformités
- L'IA propose une structure de plan d'action standard
- L'IA suggère des actions correctives types pour chaque catégorie
- L'utilisateur ajuste avec les contraintes réelles du client
  (délais, accès, coûts) et fait valider techniquement

## Gain unitaire moyen estimé
- Temps actuel moyen : 90 à 180 minutes par plan d'action
- Temps avec IA encadrée : 40 à 85 minutes par plan
- Gain net moyen : 50 à 95 minutes par plan
- Hypothèse de calcul retenue : 50 % de gain moyen (prudence
  renforcée vu la responsabilité juridique engagée)

## Source des estimations
Études sectorielles 2024 sur l'IA générative dans les services de
conformité : gains de 45 à 60 % sur la structuration des plans
d'action, limités par la nécessité de validation humaine
systématique.

## Formule de calcul du ROI personnalisé
Variables collectées auprès de l'apprenant :
- temps_actuel = temps moyen actuel pour un plan d'action (minutes)
- frequence = nombre de plans d'action par mois (puis converti
  en hebdo)

Calcul :
- gain_par_plan = temps_actuel × 0,50
- gain_hebdo_minutes = (gain_par_plan × frequence) / 4,33
- gain_hebdo_heures = gain_hebdo_minutes / 60
- gain_annuel_heures = gain_hebdo_heures × 45 semaines
- gain_annuel_euros = gain_annuel_heures × 35 €

## Prérequis de formation
- Module 1 — Comprendre l'IA générative (obligatoire)
- Module 2 — Risques et confidentialité (obligatoire)
- Module 3 — RGPD et IA générative (obligatoire)
- Module 4 — Cadre AI Act (obligatoire)
- Module 5 — Prompt engineering responsable (obligatoire)
- Module 6 — Cas pratiques métier (obligatoire)

## Points de vigilance RGPD et confidentialité
NIVEAU DE VIGILANCE : ÉLEVÉ

Un plan d'action correctif est un document qui engage la
responsabilité technique et juridique de DEF Ouest vis-à-vis du
client. En cas d'incident postérieur, le plan peut être produit en
justice ou utilisé par l'assureur.

Pratiques sécurisées :
- Anonymiser les références au site et au client dans le prompt
- L'IA propose une trame et des actions types — la décision technique
  finale appartient au responsable technique
- Validation hiérarchique systématique avant transmission au client
- Conservation du brouillon généré dans un environnement maîtrisé

À ne pas faire :
- Considérer le plan généré par l'IA comme un document définitif
- Diffuser au client sans validation technique formelle
- Faire produire par l'IA des engagements de moyens ou de résultats
  précis (délais, coûts, garanties)
- Coller des éléments d'audit ou de rapport d'incident bruts

## Classification AI Act
Risque limité au sens de l'outil (assistance à la rédaction).
Vigilance : le plan d'action est un document à valeur d'engagement
contractuel et potentiellement à valeur juridique en cas d'incident.
Validation humaine non négociable.

## Recommandation d'outil
Claude (interface entreprise) ou ChatGPT Enterprise UNIQUEMENT.

## Prompt type proposé à l'apprenant
"Tu es assistant à la rédaction de plans d'action correctifs pour
mise en conformité incendie. À partir de la liste anonymisée des
non-conformités que je te fournis, structure un plan d'action
professionnel selon les sections : 1) Contexte et objectif, 2) Liste
des non-conformités par catégorie, 3) Pour chaque non-conformité :
action corrective proposée, type d'intervention, niveau d'urgence
(immédiat / court terme / moyen terme), 4) Synthèse et prochaines
étapes. Ne propose aucun délai précis ni aucun coût (sera complété
par moi). Reste générique sur les actions, n'invente aucun élément
absent de ma liste.
Liste anonymisée de non-conformités : [ICI LA LISTE]"
