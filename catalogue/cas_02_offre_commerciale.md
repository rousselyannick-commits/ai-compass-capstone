# CAS D'USAGE 02 — Préparation d'offre commerciale et devis technique

## Description courte
Construire une offre commerciale structurée et un devis technique
pour un client, à partir de l'expression de besoin reçue (cahier des
charges, demande de cotation) et des éléments techniques produits par
le bureau d'études.

## Profils métier cibles
Commercial Travaux, Commercial Maintenance, Chargé d'affaires Travaux

## Mots-clés de détection
"offre", "devis", "proposition commerciale", "chiffrage", "cotation",
"prix de vente", "réponse à demande client"

## Tâche actuelle (avant IA)
- Lecture du cahier des charges ou de la demande client
- Sollicitation du bureau d'études pour le chiffrage technique
- Rédaction des sections rédactionnelles de l'offre (contexte,
  compréhension du besoin, méthodologie, garanties, planning)
- Mise en forme dans le modèle Word DEF Ouest
- Relecture et validation hiérarchique

## Tâche avec IA encadrée
- L'utilisateur fournit à l'IA une synthèse du besoin (sans coller le
  cahier des charges brut)
- L'IA propose une trame d'offre adaptée au contexte décrit
- L'IA reformule et structure les paragraphes commerciaux
- L'utilisateur intègre les éléments techniques chiffrés (issus du BE)
- Relecture critique et validation humaine systématique

## Gain unitaire moyen estimé
- Temps actuel moyen : 180 à 300 minutes par offre (selon complexité)
- Temps avec IA encadrée : 80 à 130 minutes par offre
- Gain net moyen : 100 à 170 minutes par offre
- Hypothèse de calcul retenue : 55 % de gain moyen

## Source des estimations
Étude McKinsey 2024 sur les gains de productivité IA générative en
B2B : 50 à 60 % sur les tâches de rédaction structurée à partir
d'éléments existants. Hypothèse prudente compte tenu du caractère
contractuel de l'offre (relecture humaine systématique non
optimisable).

## Formule de calcul du ROI personnalisé
Variables collectées auprès de l'apprenant :
- temps_actuel = temps moyen actuel pour une offre (minutes)
- frequence = nombre d'offres rédigées par semaine

Calcul :
- gain_par_offre = temps_actuel × 0,55
- gain_hebdo_minutes = gain_par_offre × frequence
- gain_hebdo_heures = gain_hebdo_minutes / 60
- gain_annuel_heures = gain_hebdo_heures × 45 semaines
- gain_annuel_euros = gain_annuel_heures × 35 € (coût chargé moyen)

## Prérequis de formation
- Module 1 — Comprendre l'IA générative (obligatoire)
- Module 2 — Risques et confidentialité (obligatoire)
- Module 3 — RGPD et IA générative (obligatoire, CRITIQUE)
- Module 5 — Prompt engineering responsable (obligatoire)
- Module 6 — Cas pratiques métier (obligatoire)

## Points de vigilance RGPD et confidentialité
NIVEAU DE VIGILANCE : ÉLEVÉ

Un cahier des charges client contient quasi systématiquement des
données identifiantes (interlocuteurs, coordonnées, descriptions
détaillées de sites, parfois plans). Pour les clients industriels ou
infrastructures critiques, ces informations relèvent du secret des
affaires voire de la sécurité.

Pratiques sécurisées :
- NE JAMAIS coller le cahier des charges brut dans un LLM
- Extraire manuellement une synthèse anonymisée du besoin
  (type d'établissement, type de système, contraintes principales)
  AVANT toute interaction avec l'IA
- Utiliser uniquement un outil IA maîtrisé entreprise
- Conserver le brouillon généré dans un environnement maîtrisé
- Validation humaine obligatoire avant envoi au client

À ne pas faire :
- Coller le cahier des charges en pièce jointe ou en texte brut
- Mentionner le nom du client dans le prompt
- Demander à l'IA de "deviner" les attentes du client à partir
  d'éléments parcellaires

## Classification AI Act
Risque limité — Assistance à la rédaction.
Vigilance particulière : l'offre est un document contractuel qui
engage juridiquement DEF Ouest. La relecture humaine est obligatoire
et non optionnelle.

## Recommandation d'outil
Claude (interface entreprise) ou ChatGPT Enterprise UNIQUEMENT.
Refus catégorique : toute version grand public, gratuite ou
personnelle.

## Prompt type proposé à l'apprenant
"Tu es assistant à la rédaction d'offres commerciales pour DEF Ouest,
expert en systèmes de sécurité incendie. À partir de la synthèse de
besoin que je te fournis (anonymisée), propose-moi une trame d'offre
structurée avec : 1) Compréhension du besoin, 2) Solution proposée,
3) Méthodologie d'intervention, 4) Garanties et engagements,
5) Planning prévisionnel. Ton professionnel, orienté valeur pour le
client, sans inventer d'éléments techniques précis (je les ajouterai
moi-même).
Synthèse anonymisée du besoin : [ICI LA SYNTHÈSE]"
