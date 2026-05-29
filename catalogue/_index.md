# Catalogue des cas d'usage IA — AI Compass

Index des cas d'usage IA générative documentés pour AI Compass.
Ce fichier est lu par l'agent en phase de cartographie pour identifier
les cas pertinents en fonction du profil et des tâches décrites par
l'apprenant.

## Profil Commercial (10 cas)

| ID | Titre | Profils ciblés | Mots-clés | Gain unitaire moyen | Vigilance | Fichier détaillé |
|----|-------|----------------|-----------|---------------------|-----------|------------------|
| 01 | Compte rendu de visite prospect ou client | Commercial Travaux, Commercial Maintenance, Chargé d'affaires | CR visite, visite client, visite prospect, rendez-vous, synthèse entretien | 60 % de gain (20-30 min/CR) | Modérée | cas_01_compte_rendu_visite.md |
| 02 | Préparation d'offre commerciale et devis technique | Commercial Travaux, Commercial Maintenance, Chargé d'affaires Travaux | offre, devis, proposition commerciale, chiffrage, cotation | 55 % de gain (100-170 min/offre) | Élevée | cas_02_offre_commerciale.md |
| 03 | Réponse à un appel d'offres | Commercial Travaux, Chargé d'affaires Travaux | appel d'offres, AO, consultation, DCE, mémoire technique | 40 % de gain (250-500 min/AO) | Élevée | cas_03_appel_offres.md |
| 04 | Argumentaire produit ou solution | Commercial Travaux, Commercial Maintenance | argumentaire, pitch, présenter une solution, vendre, discours commercial | 65 % de gain (30-60 min/argumentaire) | Faible | cas_04_argumentaire_produit.md |
| 05 | Email de relance et suivi d'affaires | Commercial Travaux, Commercial Maintenance, Chargé d'affaires | relance, email de suivi, follow-up, réactivation, courriel client | 65 % de gain (7-13 min/email) | Modérée | cas_05_email_relance.md |
| 06 | Synthèse de réunion technique avec client | Commercial Travaux, Chargé d'affaires Travaux, Commercial Maintenance | CR réunion, synthèse réunion, réunion technique, réunion de chantier | 60 % de gain (30-50 min/CR) | Modérée | cas_06_synthese_reunion.md |
| 07 | Présentation pour décideurs client | Commercial Travaux, Chargé d'affaires Travaux, Responsables techniques | présentation, slides, deck, PowerPoint, pitch décideurs, présenter au CODIR | 60 % de gain (80-150 min/présentation) | Faible | cas_07_presentation_decideurs.md |
| 08 | Synthèse d'audit de conformité incendie | Chargé d'affaires Travaux, Commercial Maintenance, Responsables techniques | audit, synthèse audit, rapport audit, diagnostic conformité | 55 % de gain (55-105 min/synthèse) | Très élevée | cas_08_synthese_audit.md |
| 09 | Plan d'action correctif post non-conformité | Commercial Maintenance, Chargé d'affaires Travaux, Responsables techniques | plan d'action, plan correctif, mise en conformité, actions correctives, préconisations | 50 % de gain (50-95 min/plan) | Élevée | cas_09_plan_action_correctif.md |
| 10 | Rapport d'activité commerciale périodique | Commercial Travaux, Commercial Maintenance, Chargé d'affaires | rapport d'activité, reporting commercial, rapport hebdo, bilan d'activité | 65 % de gain (20-50 min/rapport) | Modérée | cas_10_rapport_activite.md |

## Légende des niveaux de vigilance

- **Faible** : contenu commercial générique, peu ou pas de données client identifiantes. Utilisation IA possible avec précautions standard.
- **Modérée** : contenu contenant des données contact client ou des éléments commerciaux. Nécessite outil IA maîtrisé entreprise + bonnes pratiques d'anonymisation.
- **Élevée** : contenu engageant juridiquement DEF Ouest et/ou contenant des informations clients sensibles. Validation humaine obligatoire, anonymisation préalable systématique.
- **Très élevée** : contenu portant sur des sites sensibles (infrastructures critiques, OIV, SEVESO) ou contenant des vulnérabilités techniques. Approche restrictive, validation hiérarchique non négociable.

## Méthodologie commune à toutes les fiches

Toutes les fiches du catalogue partagent une méthodologie unifiée :
- Estimations de gain basées sur les études McKinsey 2024, BCG, HubSpot, Microsoft 365 Copilot et études sectorielles
- Coût horaire chargé de référence : 35 € (commercial PME)
- Base annuelle : 45 semaines travaillées
- Hypothèse de prudence : ajustement -10 % par rapport aux études pour tenir compte du contexte PME et de la courbe d'apprentissage

## Cas non couverts par le catalogue

Si un usage décrit par l'apprenant ne correspond à aucun cas du catalogue, l'agent oriente vers le référent IA humain de DEF Ouest. Cas explicitement écartés du catalogue (à traiter en module dédié "Ce qu'on ne fait pas avec l'IA") :

- Rapports de vérifications périodiques VPO/RIA (valeur de preuve juridique, opposables en justice)
- Fiches techniques chantier et installation (documents de référence technique opposables)
- Tout document à valeur réglementaire d'attestation ou de certification
