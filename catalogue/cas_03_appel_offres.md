# CAS D'USAGE 03 — Réponse à un appel d'offres

## Description courte
Construire une réponse formelle à un appel d'offres public ou privé,
en respectant le formalisme imposé par le règlement de consultation
et en valorisant les atouts de DEF Ouest.

## Profils métier cibles
Commercial Travaux, Chargé d'affaires Travaux

## Mots-clés de détection
"appel d'offres", "AO", "consultation", "règlement de consultation",
"DCE", "mémoire technique", "réponse marché public"

## Tâche actuelle (avant IA)
- Analyse du règlement de consultation et du cahier des charges
- Extraction des exigences et critères d'attribution
- Construction du mémoire technique
- Rédaction des sections rédactionnelles (présentation de
  l'entreprise, références, méthodologie, équipe)
- Intégration des éléments chiffrés
- Mise en conformité avec les pièces administratives demandées

## Tâche avec IA encadrée
- Synthèse manuelle préalable des exigences de l'AO
- Utilisation de l'IA pour structurer le mémoire technique selon le
  plan attendu
- Reformulation et adaptation des passages standards (présentation
  entreprise, méthodologie)
- Relecture critique systématique
- Vérification manuelle de la conformité aux exigences formelles

## Gain unitaire moyen estimé
- Temps actuel moyen : 600 à 1200 minutes par AO (selon ampleur)
- Temps avec IA encadrée : 350 à 700 minutes par AO
- Gain net moyen : 250 à 500 minutes par AO (4 à 8 heures)
- Hypothèse de calcul retenue : 40 % de gain moyen

## Source des estimations
Études Gartner 2024 sur IA générative et réponse aux appels d'offres :
gains de 35 à 50 % sur la production du mémoire technique, plus
limités sur les parties administratives et de chiffrage.

## Formule de calcul du ROI personnalisé
Variables collectées auprès de l'apprenant :
- temps_actuel = temps moyen actuel pour un AO (minutes)
- frequence = nombre d'AO traités par mois (puis converti en hebdo)

Calcul :
- gain_par_ao = temps_actuel × 0,40
- gain_hebdo_minutes = (gain_par_ao × frequence) / 4,33
- gain_hebdo_heures = gain_hebdo_minutes / 60
- gain_annuel_heures = gain_hebdo_heures × 45 semaines
- gain_annuel_euros = gain_annuel_heures × 35 €

## Prérequis de formation
- Module 1 — Comprendre l'IA générative (obligatoire)
- Module 2 — Risques et confidentialité (obligatoire)
- Module 3 — RGPD et IA générative (obligatoire)
- Module 4 — Cadre AI Act (recommandé)
- Module 5 — Prompt engineering responsable (obligatoire)

## Points de vigilance RGPD et confidentialité
NIVEAU DE VIGILANCE : ÉLEVÉ

Un dossier de consultation (DCE) contient des informations
contractuelles parfois confidentielles. Pour les marchés publics, le
respect du règlement de consultation peut interdire explicitement la
transmission à des tiers.

Pratiques sécurisées :
- Lire EN PREMIER les clauses de confidentialité du règlement de
  consultation
- Si le règlement interdit la transmission à des tiers : n'utiliser
  l'IA QUE sur des passages génériques (présentation entreprise,
  méthodologie type)
- Ne JAMAIS coller le règlement de consultation ou le CCTP brut
- Anonymiser systématiquement les références au pouvoir adjudicateur

À ne pas faire :
- Soumettre le DCE complet à un LLM
- Utiliser l'IA pour fabriquer de fausses références ou des éléments
  d'attestation
- S'appuyer sur l'IA pour générer des éléments engageant la
  responsabilité de l'entreprise sans validation hiérarchique

## Classification AI Act
Risque limité — Assistance à la rédaction.
Note : la réponse à un AO est un document à valeur contractuelle
engageant l'entreprise sur ses prix et engagements. Validation
hiérarchique obligatoire.

## Recommandation d'outil
Claude (interface entreprise) ou ChatGPT Enterprise UNIQUEMENT.

## Prompt type proposé à l'apprenant
"Tu es assistant à la rédaction de mémoires techniques pour réponse à
appels d'offres dans le secteur de la sécurité incendie. À partir du
plan imposé que je te fournis et des éléments de contexte (anonymisés)
sur notre proposition, rédige une trame structurée et argumentée pour
chaque section demandée. Reste factuel, n'invente pas de références
ou de certifications. Ton professionnel et orienté valeur pour le
donneur d'ordre.
Plan imposé : [ICI LE PLAN]
Éléments de contexte : [ICI LES ÉLÉMENTS]"
