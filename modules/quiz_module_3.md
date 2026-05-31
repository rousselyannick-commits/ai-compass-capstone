# quiz_module_3.md
# AI Compass — Quiz d'ancrage — Module 3 : RGPD et IA

---

## MÉTADONNÉES

module: M3
titre: RGPD et IA
nb_questions: 6
niveaux: facile → avancé
usage: ancrage en fin de module + retest ciblé si score < 4/5 au quiz final
format: QCM 4 options, 1 seule bonne réponse par question

---

## QUESTION 1 — Niveau : Facile

**José colle dans ChatGPT le nom, le numéro de téléphone et l'adresse d'un
client pour rédiger un email de relance. Il fait quoi comme erreur ?**

A. Rien, ChatGPT est un outil professionnel sécurisé
B. Il traite des données personnelles sans base légale dans un outil
   grand public non conforme
C. Il viole uniquement la politique interne de DEF Ouest, pas le RGPD
D. Il fait une erreur technique, pas juridique

**Bonne réponse : B**

Explication si erreur :
Le nom, le téléphone et l'adresse d'un client sont des données personnelles
au sens du RGPD. Les coller dans un LLM grand public constitue un transfert
de données à un tiers sans garantie de conformité. C'est une violation RGPD
potentielle, pas seulement un problème interne.

---

## QUESTION 2 — Niveau : Facile

**Parmi ces éléments, lequel N'EST PAS une donnée personnelle ?**

A. Le numéro de chantier d'un site industriel anonyme
B. L'adresse email professionnelle d'un contact client
C. Le prénom et le nom d'un chef de sécurité incendie
D. Le numéro de portable d'un décideur chez un client

**Bonne réponse : A**

Explication si erreur :
Un numéro de chantier attribué à un site, sans lien avec une personne
identifiable, n'est pas une donnée personnelle. Les autres exemples
permettent d'identifier directement une personne physique — ils sont
donc protégés par le RGPD.

---

## QUESTION 3 — Niveau : Intermédiaire

**José prépare une synthèse d'audit pour un site SEVESO. Il veut utiliser
l'IA pour structurer le document. Quelle est la bonne pratique ?**

A. Coller le rapport brut dans ChatGPT, c'est plus rapide
B. Utiliser uniquement un outil validé par DEF Ouest, sans données
   sensibles du site
C. Envoyer le rapport par email à son référent IA avant d'utiliser l'IA
D. Ne jamais utiliser l'IA sur ce type de document, sans exception

**Bonne réponse : B**

Explication si erreur :
Les documents d'audit sur sites SEVESO ou OIV contiennent des informations
sensibles (plans, vulnérabilités, contacts). La règle est : outil validé
+ minimisation des données. L'interdiction totale (D) est trop rigide —
l'IA peut aider sur la mise en forme si les données sensibles sont retirées.
Demander l'avis du référent IA (C) est une bonne pratique générale,
mais ne remplace pas les règles d'usage.

---

## QUESTION 4 — Niveau : Intermédiaire

**Qu'est-ce que la minimisation des données dans le contexte de l'IA ?**

A. Réduire la taille du fichier avant de l'envoyer à l'outil IA
B. N'inclure dans le prompt que les données strictement nécessaires
   à la tâche demandée
C. Supprimer les données après utilisation dans l'outil IA
D. Demander l'accord du client avant chaque usage IA

**Bonne réponse : B**

Explication si erreur :
La minimisation est un principe fondamental du RGPD (article 5) : on ne
traite que les données nécessaires à la finalité. Appliqué à l'IA, cela
signifie : si tu n'as pas besoin du nom du client pour rédiger un email
type, tu ne le mets pas dans le prompt. Moins de données = moins de risque.

---

## QUESTION 5 — Niveau : Avancé

**Un client de DEF Ouest demande à consulter les données que l'entreprise
détient sur lui. Ce droit s'appelle :**

A. Droit à l'effacement
B. Droit d'accès
C. Droit à la portabilité
D. Droit d'opposition

**Bonne réponse : B**

Explication si erreur :
Le droit d'accès (article 15 du RGPD) permet à toute personne de demander
quelles données la concernant sont traitées, pourquoi, et par qui. C'est
différent du droit à l'effacement (demander la suppression), de la
portabilité (récupérer ses données dans un format réutilisable) ou de
l'opposition (refuser un traitement).

---

## QUESTION 6 — Niveau : Avancé

**José génère avec l'IA une offre commerciale pour un client. Qui est
responsable de vérifier que le contenu est exact et conforme avant envoi ?**

A. L'outil IA, qui garantit l'exactitude de ses outputs
B. Le responsable informatique de DEF Ouest
C. José lui-même — la validation humaine est obligatoire
D. Le client, qui valide l'offre à réception

**Bonne réponse : C**

Explication si erreur :
Un LLM peut produire des erreurs factuelles, des hallucinations, ou des
formulations inadaptées. La validation humaine avant tout envoi est une
règle d'or — juridiquement, DEF Ouest est responsable du contenu qu'elle
envoie, pas l'outil IA. C'est aussi l'un des principes de l'AI Act :
maintenir un contrôle humain significatif sur les outputs.

---

## INSTRUCTIONS POUR L'AGENT

- Présente une question à la fois, attends la réponse avant de passer
  à la suivante.
- Ne révèle pas la bonne réponse avant que l'apprenant ait répondu.
- Si réponse correcte : valide brièvement et enchaîne.
- Si réponse incorrecte : donne l'explication, reformule le principe clé
  en une phrase, puis passe à la suite sans insister.
- Score final sur 6 — communiqué à la fin des 6 questions.
- Seuil de réussite module : 4/6 minimum.
- Si score < 4/6 : signaler à l'agent Formation pour repassage ciblé
  des questions ratées (pas tout le module).
