# CAS D'USAGE 08 — Synthèse d'audit de conformité incendie

## Description courte
Produire une synthèse exécutive d'un audit de conformité incendie
réalisé chez un client, à partir des observations terrain détaillées,
pour faciliter la communication des constats aux décideurs et le
suivi des actions correctives.

## Profils métier cibles
Chargé d'affaires Travaux, Commercial Maintenance, Responsables
techniques

## Mots-clés de détection
"audit", "synthèse audit", "rapport audit", "compte rendu audit",
"diagnostic conformité", "audit incendie", "rapport d'inspection"

## Tâche actuelle (avant IA)
- Compilation des observations terrain (rapports de techniciens,
  photos, mesures)
- Identification des non-conformités majeures et mineures
- Hiérarchisation par criticité
- Rédaction de la synthèse exécutive
- Rédaction des recommandations associées

## Tâche avec IA encadrée
- L'utilisateur fournit à l'IA la liste des constats (sans données
  identifiantes du site)
- L'IA structure une synthèse exécutive selon un format standard
- L'IA propose une hiérarchisation des constats par criticité
- L'utilisateur valide, ajuste, complète avec sa connaissance du
  contexte client

## Gain unitaire moyen estimé
- Temps actuel moyen : 90 à 180 minutes par synthèse d'audit
- Temps avec IA encadrée : 35 à 75 minutes par synthèse
- Gain net moyen : 55 à 105 minutes par synthèse
- Hypothèse de calcul retenue : 55 % de gain moyen (prudence
  renforcée vu la sensibilité)

## Source des estimations
Études sectorielles 2024 sur l'usage de l'IA dans la production de
rapports d'audit et de conformité : gains de 50 à 65 % sur la
structuration et la mise en forme, plus limités sur l'analyse
critique.

## Formule de calcul du ROI personnalisé
Variables collectées auprès de l'apprenant :
- temps_actuel = temps moyen actuel pour une synthèse d'audit (minutes)
- frequence = nombre de synthèses d'audit par mois (puis converti
  en hebdo)

Calcul :
- gain_par_synthese = temps_actuel × 0,55
- gain_hebdo_minutes = (gain_par_synthese × frequence) / 4,33
- gain_hebdo_heures = gain_hebdo_minutes / 60
- gain_annuel_heures = gain_hebdo_heures × 45 semaines
- gain_annuel_euros = gain_annuel_heures × 35 €

## Prérequis de formation
- Module 1 — Comprendre l'IA générative (obligatoire)
- Module 2 — Risques et confidentialité (obligatoire)
- Module 3 — RGPD et IA générative (obligatoire, CRITIQUE)
- Module 4 — Cadre AI Act (obligatoire)
- Module 5 — Prompt engineering responsable (obligatoire)
- Module 6 — Cas pratiques métier (obligatoire)

## Points de vigilance RGPD et confidentialité
NIVEAU DE VIGILANCE : TRÈS ÉLEVÉ

Les audits de conformité incendie portent fréquemment sur des sites
clients sensibles : établissements recevant du public, sites
industriels SEVESO, infrastructures critiques (hôpitaux, datacenters,
sites OIV). Les constats détaillent les VULNÉRABILITÉS de
l'installation existante — informations à très haute sensibilité.

L'AI Act prévoit pour les infrastructures critiques des obligations
renforcées de protection des données techniques. Le RGPD ne suffit
pas, NIS2 impose également des obligations de sécurité.

Pratiques sécurisées OBLIGATOIRES :
- NE JAMAIS coller un rapport d'audit brut dans un LLM
- Extraire manuellement une liste anonymisée des constats par
  catégorie (sans nom du site, sans coordonnées, sans informations
  permettant d'identifier l'établissement)
- Pour les sites OIV / SEVESO / infrastructures critiques :
  utilisation de l'IA INTERDITE sur les constats détaillés —
  uniquement sur les sections génériques (méthodologie, cadre
  réglementaire de référence)
- Validation systématique par le responsable technique avant
  diffusion

À ne pas faire :
- Coller un rapport d'audit brut ou des photos de constats
- Mentionner le nom du site, l'adresse, le client
- Détailler les vulnérabilités spécifiques d'une installation dans
  le prompt
- Utiliser l'IA pour générer la classification finale de non-conformité

## Classification AI Act
Risque limité au sens de l'AI Act PAR L'OUTIL utilisé (assistance
à la rédaction), MAIS le contexte d'usage relève d'infrastructures
sensibles relevant de NIS2 et de la sécurité nationale dans certains
cas. Approche restrictive recommandée.

## Recommandation d'outil
Claude (interface entreprise) ou ChatGPT Enterprise UNIQUEMENT, et
uniquement sur des constats anonymisés et agrégés.
Pour sites OIV / SEVESO : limiter à la production de sections
génériques sans constats spécifiques.

## Prompt type proposé à l'apprenant
"Tu es assistant à la rédaction de synthèses d'audit de conformité
incendie. À partir de la liste anonymisée de constats que je te
fournis (sans identification du site), structure une synthèse
exécutive selon les sections : 1) Méthodologie d'audit (générique),
2) Synthèse des constats par catégorie (détection, désenfumage,
moyens de secours, organisation), 3) Hiérarchisation par criticité
(majeur / important / mineur), 4) Recommandations d'actions
correctives. Reste factuel, n'invente aucun constat absent de ma
liste. Ne propose aucune classification définitive de non-conformité
(décision technique réservée au responsable).
Liste anonymisée de constats : [ICI LES CONSTATS]"
