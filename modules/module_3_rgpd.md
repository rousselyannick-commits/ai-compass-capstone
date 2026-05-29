---
module: 3
titre: RGPD et IA générative — Réflexes opérationnels
durée_cible: 20-25 minutes
public: Collaborateurs DEF Ouest, tous profils
prérequis: Module 1 — Comprendre l'IA générative
objectifs:
  - Identifier une donnée personnelle dans le contexte d'un prompt
  - Connaître les 4 règles d'or de l'usage RGPD-compatible de l'IA
  - Distinguer outils maîtrisés et outils grand public
  - Savoir où trouver de l'aide en cas de doute
---

# Module 3 — RGPD et IA générative : réflexes opérationnels

## SECTION 1 — Pourquoi ce module existe

### 1.1 — Le problème en une histoire

Un lundi matin chez DEF Ouest. José, commercial Travaux, a un rendez-vous important à 11 heures chez un client industriel. Sur son bureau, un cahier des charges de 40 pages, reçu vendredi soir. Il a deux heures pour s'en imprégner avant de partir.

José ouvre ChatGPT sur son téléphone, copie l'intégralité du cahier des charges dans la fenêtre, et demande : *"Résume-moi ce document en 10 points clés."* En quelques secondes, il a sa synthèse. Il prend la route, serein.

Cette scène se déroule, sous des variantes, des dizaines de fois par semaine chez DEF Ouest. Elle est compréhensible — José gagne du temps réel, il fait son métier. Elle n'est pas malveillante. Et pourtant, en 30 secondes, José a transmis à OpenAI les coordonnées du client, le nom du responsable sécurité, la description précise d'un site industriel sensible, et potentiellement des éléments qui relèvent du secret des affaires.

Ce module ne va pas culpabiliser José. Il va lui donner les réflexes qui lui permettront de gagner le même temps, en évitant les risques.

### 1.2 — Ce qui se passe vraiment, côté technique

Quand on colle du texte dans un LLM grand public, voici ce qui se passe :

- Le texte est envoyé sur les serveurs du fournisseur (OpenAI, Google, Anthropic, etc.), souvent hors de l'Union européenne.
- Le texte est conservé pour des durées variables, selon les conditions d'utilisation.
- Dans les versions gratuites et grand public, le contenu peut être utilisé pour **entraîner les futurs modèles**. C'est-à-dire que le texte de José devient une matière première qui peut influencer ce que ChatGPT répondra à d'autres utilisateurs, dans le monde entier.
- Le contenu peut être consulté par des opérateurs humains (modération, contrôle qualité) selon les conditions du fournisseur.
- En cas de fuite ou d'incident de sécurité chez le fournisseur (ce qui est arrivé plusieurs fois), le contenu peut se retrouver exposé.

Ces faits ne sont pas des fantasmes. Ils sont écrits noir sur blanc dans les conditions d'utilisation des outils grand public. La plupart des utilisateurs ne les lisent pas — ce qui est compréhensible, mais ne change rien à leur applicabilité juridique.

### 1.3 — Les trois familles de risques

Quand un collaborateur de DEF Ouest utilise un LLM grand public avec des données identifiables, il crée trois risques distincts qui ne se confondent pas.

**Risque pour la personne concernée.** Si José transmet le nom et l'email du responsable sécurité du client à OpenAI, cette personne voit ses données traitées sans qu'elle l'ait su ni qu'elle ait pu s'y opposer. C'est ce que le RGPD protège : la maîtrise par chaque individu de ses propres données.

**Risque pour DEF Ouest.** En cas de contrôle CNIL ou de plainte d'une personne concernée, DEF Ouest est responsable du traitement illicite, même si c'est un collaborateur qui a agi seul. Les sanctions vont de l'avertissement à l'amende administrative (jusqu'à 4 % du chiffre d'affaires annuel mondial, soit théoriquement plus de 700 000 euros pour DEF Ouest dans le pire cas — en pratique, les sanctions pour PME se situent plutôt entre 10 000 et 100 000 euros).

**Risque pour le client.** Le cahier des charges décrit le système de sécurité incendie d'un site. Si ce site est un hôpital, un site industriel SEVESO ou une infrastructure critique, les informations transmises à OpenAI peuvent constituer une vulnérabilité de sécurité. Le client n'a jamais autorisé la diffusion de ces informations à un tiers américain. C'est probablement la violation la plus grave, parce qu'elle peut casser la relation commerciale et exposer DEF Ouest à des actions en responsabilité contractuelle.

### 1.4 — Ce que dit la loi en 2025-2026

Deux textes s'appliquent à l'usage de l'IA générative en entreprise.

**Le RGPD**, applicable depuis 2018, encadre tout traitement de données personnelles. Coller un texte contenant des données identifiables dans un LLM grand public constitue un traitement, et déclenche les obligations associées : base légale, information des personnes, droits d'accès, sécurité.

**L'AI Act**, dont les premières obligations sont entrées en vigueur en février 2025. Son article 4 impose aux organisations qui utilisent l'IA de garantir que leurs personnels disposent d'un niveau suffisant de **maîtrise de l'IA** (*AI literacy*). Cette obligation s'applique sans seuil de taille d'entreprise — y compris à une PME comme DEF Ouest. Le module que vous suivez participe directement à cette mise en conformité.

L'AI Act prévoit également une **obligation de transparence** (article 50) : un utilisateur doit savoir quand il interagit avec une IA, et un contenu généré par IA doit pouvoir être identifié comme tel.

---

## SECTION 2 — La notion clé : qu'est-ce qu'une donnée personnelle

### 2.1 — La définition officielle, simplifiée

Le RGPD définit la donnée personnelle comme *"toute information se rapportant à une personne physique identifiée ou identifiable"*.

Le mot qui change tout, c'est **identifiable**. Une donnée n'a pas besoin de désigner directement une personne par son nom pour être personnelle. Elle est personnelle dès lors qu'on peut, en la combinant avec d'autres informations, remonter à une personne physique précise.

Un email professionnel est une donnée personnelle. Un poste précis dans une entreprise donnée aussi (*"le responsable sécurité du site Y"* identifie une personne unique). Une photo prise sur un chantier où on voit le visage d'un opérateur en est une. Un identifiant client dans une base, croisé avec une géolocalisation, en est une.

### 2.2 — Les six fausses bonnes idées qui exposent DEF Ouest

Voici les six idées reçues les plus fréquentes en entreprise, et pourquoi elles sont fausses.

**Idée reçue n°1 — "Si je ne mets pas le nom, c'est anonyme."**

Faux. La ré-identification par le contexte est très facile. *"Le chef de projet sécurité incendie de l'hôpital de [ville moyenne]"* désigne une personne unique, même sans son nom. Le RGPD considère qu'une donnée est personnelle dès qu'on peut remonter à la personne avec des moyens raisonnables. Et "raisonnable" en 2025, avec les outils de recherche disponibles, ça veut dire beaucoup.

**Idée reçue n°2 — "C'est une donnée pro, ce n'est pas du RGPD."**

Faux. Le RGPD ne distingue pas vie privée et vie professionnelle. L'email professionnel `jean.dupont@client.fr` est une donnée personnelle. Le numéro de téléphone professionnel l'est. Le poste précis aussi. Le contexte professionnel ne crée pas d'exemption — il change parfois la base légale qui peut être mobilisée, mais le statut de donnée personnelle reste.

**Idée reçue n°3 — "Mon compte ChatGPT est payant, donc c'est conforme."**

Faux. Un compte ChatGPT Plus est un compte personnel payant. Ce n'est pas la même chose qu'un compte ChatGPT Enterprise (offre entreprise avec garanties contractuelles renforcées). Dans la version Plus, les données saisies peuvent toujours être utilisées par OpenAI pour entraîner les modèles, sauf si vous avez explicitement désactivé cette option dans les paramètres. Et même si vous l'avez désactivée, vous n'avez pas de contrat de sous-traitance RGPD avec OpenAI, ce qui est obligatoire pour un usage professionnel.

**Idée reçue n°4 — "Je n'enregistre rien, c'est éphémère."**

Faux. Le simple fait de transmettre la donnée à un serveur tiers constitue un traitement au sens du RGPD, indépendamment de ce qu'il advient ensuite. Et concrètement, les LLM conservent les conversations pour des durées variables (souvent 30 jours minimum, parfois davantage) à des fins de modération et d'amélioration.

**Idée reçue n°5 — "Le client est une entreprise, pas une personne."**

Vrai pour l'entreprise. Faux pour ses interlocuteurs. L'entreprise cliente n'est pas une personne au sens du RGPD, mais les personnes qui y travaillent en sont. Le nom du responsable sécurité, l'email du directeur achat, le numéro du chargé d'affaires — toutes ces données sont personnelles, même si le client est une société.

**Idée reçue n°6 — "C'est public sur LinkedIn donc je peux l'utiliser."**

Faux. Le fait qu'une donnée soit publiquement accessible ne signifie pas qu'elle puisse être utilisée librement. Le RGPD impose une **finalité légitime** et une **base légale** pour chaque traitement. Quelqu'un qui publie son poste sur LinkedIn ne s'attend pas à voir son nom transmis à OpenAI pour générer une stratégie commerciale. Le caractère public n'efface pas le besoin de respecter le cadre du RGPD.

### 2.3 — Le test pratique en 3 questions

Avant de coller un texte dans un LLM, posez-vous ces trois questions. Le test prend 10 secondes.

**Question 1 — Y a-t-il un nom, un email, un téléphone, un poste précis, un identifiant ?**

Si oui, c'est probablement une donnée personnelle. Passez à la question 3 directement.

**Question 2 — Pourrait-on identifier quelqu'un en combinant les éléments restants ?**

Même sans nom, certaines combinaisons identifient une personne unique : un poste précis dans une entreprise donnée, un site géographique précis associé à une fonction, des coordonnées partielles qui se recoupent avec d'autres sources. Si vous avez un doute, considérez que c'est une donnée personnelle.

**Question 3 — La personne s'attendrait-elle à ce que ses données partent vers ce LLM ?**

C'est la question morale, mais c'est aussi un excellent indicateur juridique. Si vous pensez que la personne serait surprise, gênée ou hostile en apprenant ce que vous vous apprêtez à faire, c'est probablement que vous êtes hors cadre.

### 2.4 — Cas particuliers DEF Ouest

Pour le métier de DEF Ouest, certaines situations méritent un éclairage spécifique.

**Adresse d'un site client.** L'adresse seule peut être une donnée d'organisation (donc pas personnelle). Mais l'adresse associée à des informations techniques sur l'installation devient une information sensible relevant de la sécurité, voire de la confidentialité contractuelle. Pour les sites OIV ou SEVESO, l'adresse précise associée à des éléments de configuration sécuritaire est à protéger au même niveau qu'une donnée personnelle.

**Plan d'une installation.** Pas une donnée personnelle au sens strict du RGPD, mais une information à très haute sensibilité technique et contractuelle. À traiter avec la même rigueur que les données personnelles : ne jamais coller dans un LLM grand public.

**Nom du responsable sécurité ou du chef d'établissement.** Donnée personnelle classique. Si vous avez besoin de mentionner sa fonction dans un prompt, utilisez une codification : *"le responsable sécurité du Client X"*.

**Photo prise sur un chantier où on voit un opérateur.** Donnée personnelle (l'image d'une personne est une donnée biométrique potentielle). Ne jamais transmettre à un LLM sans accord explicite.

**Compte rendu d'intervention contenant des observations sur les pratiques d'un client.** Données potentiellement personnelles (jugements sur des personnes identifiables) ET sensibles côté relation commerciale. À ne traiter qu'avec un outil maîtrisé et avec validation.

---

## SECTION 3 — Les 4 règles d'or

Cette section est le cœur opérationnel du module. Si vous ne retenez qu'une chose, retenez ces quatre règles. Elles couvrent 95 % des situations professionnelles d'usage de l'IA générative.

### Règle 1 — Outil maîtrisé uniquement

**Le principe.** Quand vous utilisez un LLM pour le travail, vous devez utiliser un outil maîtrisé par l'entreprise, c'est-à-dire un outil pour lequel DEF Ouest a un contrat qui garantit la non-utilisation des données pour l'entraînement, l'hébergement maîtrisé, et l'engagement contractuel du fournisseur.

**Distinction outils maîtrisés vs grand public.**

| Catégorie | Exemples | Statut |
|---|---|---|
| Outils maîtrisés entreprise | Claude entreprise (Anthropic Enterprise), ChatGPT Enterprise, Microsoft Copilot avec licence M365, Mistral entreprise | Acceptable pour usage professionnel encadré |
| Outils grand public | ChatGPT gratuit, ChatGPT Plus personnel, Gemini grand public, Copilot personnel (hors M365 entreprise), Mistral Le Chat grand public | À éviter pour toute donnée non strictement publique et générique |

**Pourquoi ça change tout.** Avec un outil maîtrisé entreprise, vous avez :
- Un contrat de sous-traitance RGPD (article 28) signé entre DEF Ouest et le fournisseur
- Une garantie contractuelle de non-utilisation des données pour l'entraînement
- Un hébergement souvent localisé en UE
- Une traçabilité des usages
- Une responsabilité juridique du fournisseur engagée

Sans outil maîtrisé, vous n'avez aucune de ces garanties.

**Situation actuelle chez DEF Ouest.** À ce jour, DEF Ouest n'a pas encore déployé d'outil IA maîtrisé. C'est précisément ce que ce projet d'acculturation prépare. En attendant, la conduite à tenir est la suivante : si vous devez absolument utiliser un LLM grand public pour gagner du temps, **respectez impérativement les trois autres règles ci-dessous**, qui réduisent le risque sans l'annuler. Et signalez au référent IA (DSI) les usages que vous faites, pour qu'ils nourrissent la réflexion sur l'outil à déployer.

**Exemple à reproduire.** Marie, chargée d'affaires, doit rédiger un email de relance générique pour des prospects qui ont demandé une documentation sans suite. Elle utilise un LLM grand public en restant 100 % générique : pas de nom de prospect, pas de société, pas de montant, pas de date précise. Le prompt et la sortie sont anonymes par construction.

**Exemple à éviter.** Marie copie sa base de prospects (40 noms, sociétés, statuts) dans ChatGPT gratuit pour générer une stratégie de relance personnalisée. Données identifiables transmises à OpenAI, sans base légale, sans information des personnes.

**À retenir.** Outil maîtrisé = règle. Outil grand public = exception, sous trois conditions : nécessité réelle, anonymisation systématique, signalement au référent IA.

### Règle 2 — Minimisation des données

**Le principe.** Le RGPD impose la minimisation : on ne traite que les données strictement nécessaires à la finalité poursuivie. Appliqué à l'IA générative, ça veut dire : ne jamais coller plus que ce qui est nécessaire à la tâche demandée.

**Pourquoi c'est puissant.** La minimisation transforme la question *"est-ce que j'ai le droit ?"* en question *"est-ce que j'en ai vraiment besoin ?"*. Et 90 % du temps, on n'a pas besoin de transmettre les données identifiantes pour obtenir le résultat qu'on veut.

**Les trois techniques de minimisation.**

*Extraction préalable manuelle.* Au lieu de coller un cahier des charges de 40 pages, on en extrait manuellement une synthèse anonymisée de 15 lignes : *"Demande d'un client industriel, secteur agroalimentaire, site de 8 000 m², détection automatique + sprinklage, mise en service souhaitée sous 6 mois, budget indicatif 200 K€."* On a tout ce qu'il faut pour que l'IA aide, sans aucune donnée identifiante.

*Anonymisation.* On remplace les noms réels par des codes. *"Client X"*, *"interlocuteur Y"*, *"site Z"*. La structure du raisonnement reste, l'identification disparaît.

*Codification des montants et dates.* Plutôt que *"offre à 187 432 € envoyée le 14 mars"*, on dit *"offre à environ 190 K€ envoyée mi-mars"*. L'IA produit la même qualité de réponse, on protège la précision commerciale.

**Exemple appliqué — compte rendu de visite.**

Version à éviter : *"Visite hier chez M. Dupont, directeur sécurité de l'usine LafargeHolcim de Saint-Pierre-la-Cour. Il m'a parlé de problèmes récurrents avec leur système Siemens existant, notamment des fausses alarmes nocturnes. Budget évoqué : 250 K€ pour rénovation complète. Décision prévue avant fin Q2."*

Version conforme : *"Visite chez un client industriel, secteur ciment, site de production. L'interlocuteur sécurité signale des problèmes de fausses alarmes nocturnes sur leur système existant. Une rénovation complète est envisagée, budget cohérent. Décision attendue dans le trimestre. Structure-moi un compte rendu à partir de mes notes."*

**À retenir.** Avant de coller : qu'est-ce que je peux retirer sans changer la qualité de la réponse attendue ? Tout ce qui peut être retiré doit l'être.

### Règle 3 — Validation humaine systématique

**Le principe.** L'IA propose, l'humain dispose. Aucun contenu généré par IA ne doit être diffusé en externe sans relecture critique humaine.

**Pourquoi c'est non négociable.** Trois raisons.

*Les hallucinations.* Un LLM peut produire des affirmations fausses présentées avec assurance. Une référence de norme qui n'existe pas, un chiffre inventé, une citation attribuée à quelqu'un qui ne l'a jamais prononcée. Dans le contexte commercial DEF Ouest, c'est inacceptable : un client qui reçoit une offre contenant une fausse référence APSAD vous perdra durablement.

*Les biais.* Le LLM peut produire des formulations inadaptées au contexte (ton trop familier, anglicismes, tournures américaines), des assertions stéréotypées, ou des omissions importantes.

*La responsabilité juridique.* Quand une offre commerciale est envoyée à un client, elle engage DEF Ouest. Si elle a été générée par IA sans relecture, la responsabilité reste entière côté DEF Ouest. *"C'est l'IA qui l'a écrit"* n'est pas une défense juridique.

**Comment ça s'organise concrètement.**

*Pour les contenus internes peu engageants* (notes, brouillons, comptes rendus internes) : relecture critique par l'auteur, vérification des faits cités, ajustement du ton.

*Pour les contenus externes peu engageants* (emails de relance, présentations génériques) : relecture critique par l'auteur, double passe avant envoi.

*Pour les contenus engageants* (offres, réponses à AO, plans d'action, synthèses d'audit) : relecture critique par l'auteur, validation hiérarchique formelle avant transmission au client.

**À retenir.** Si vous ne relisez pas, ne diffusez pas. Plus le contenu engage l'entreprise, plus la validation doit être formelle.

### Règle 4 — Traçabilité et transparence

**Le principe.** Vous devez pouvoir dire ce que vous avez fait avec l'IA, à qui demande. Et ne jamais masquer l'usage de l'IA quand il est pertinent de le mentionner.

**Pourquoi cette règle existe.** Trois raisons.

*L'obligation AI Act de transparence* (article 50). Quand un contenu est généré par IA, il doit pouvoir être identifié comme tel si la question est posée. Cette obligation s'applique progressivement à toutes les organisations en Europe.

*La traçabilité interne.* Si un problème survient (erreur dans une offre, fuite de données), il faut pouvoir reconstituer ce qui s'est passé. Garder une trace de ce qu'on a fait avec quel outil, sur quelles données, à quelle date, est une bonne pratique de gouvernance.

*La cohérence éthique.* Cacher l'usage de l'IA, c'est suggérer qu'on en a honte. Si vous l'utilisez bien, vous n'avez aucune raison de le cacher. Si vous avez besoin de le cacher, c'est probablement que vous ne l'utilisez pas bien.

**Les bonnes pratiques de traçabilité.**

*Conserver les prompts importants.* Pour les tâches récurrentes, conserver les prompts qui marchent bien dans un dossier personnel (ou dans le futur référentiel d'entreprise) — ça permet de les réutiliser et de documenter votre démarche.

*Mentionner l'usage de l'IA quand c'est pertinent.* Dans un compte rendu interne, vous pouvez indiquer *"synthèse assistée par IA, relue et validée par X"*. Pas une obligation systématique, mais une pratique recommandée pour les documents engageants.

*Ne pas mentir si on vous demande.* Si un client, un collègue ou votre hiérarchie vous demande si vous avez utilisé l'IA pour produire un document, répondez honnêtement. La transparence protège ; la dissimulation expose.

**À retenir.** L'IA n'est pas un secret coupable. Tracez vos usages, soyez transparent quand pertinent, ne mentez jamais si la question est posée.

---

## SECTION 4 — Les bases légales pour aller plus loin

Cette section approfondit le cadre juridique pour les apprenants qui souhaitent une compréhension plus complète. Elle n'est pas indispensable pour appliquer les 4 règles d'or, mais elle aide à comprendre **pourquoi** elles existent et à raisonner sur les cas non couverts.

### 4.1 — Les 6 bases légales du RGPD en une minute

Tout traitement de données personnelles doit reposer sur l'une des six bases légales prévues par l'article 6 du RGPD. C'est la "raison juridique" qui rend le traitement licite.

| Base légale | En clair | Exemple DEF Ouest |
|---|---|---|
| **Consentement** | La personne a dit oui de manière libre, éclairée, spécifique et révocable | Inscription d'un prospect à la newsletter DEF Ouest avec case à cocher |
| **Contrat** | Le traitement est nécessaire à l'exécution d'un contrat avec la personne | Traitement des coordonnées du contact client pour exécuter le contrat de maintenance |
| **Obligation légale** | La loi oblige DEF Ouest à traiter ces données | Conservation des factures pour respecter le code de commerce |
| **Intérêt vital** | Protéger une vie humaine | Très rare en contexte d'entreprise, applicable aux situations d'urgence |
| **Mission d'intérêt public** | Une mission confiée par l'autorité publique | Non applicable à DEF Ouest |
| **Intérêt légitime** | DEF Ouest a un intérêt légitime, équilibré avec les droits de la personne | Traitement des contacts professionnels d'un prospect pour le démarchage commercial |

### 4.2 — Laquelle s'applique à l'usage de l'IA en entreprise

Pour l'usage de l'IA générative par les collaborateurs dans le cadre de leur travail, la base légale mobilisable est généralement l'**intérêt légitime de l'employeur** (DEF Ouest a un intérêt légitime à doter ses collaborateurs d'outils de productivité). Cette base légale n'est pas un blanc-seing : elle est conditionnée à trois exigences.

**Un équilibrage des intérêts.** L'intérêt de DEF Ouest doit être mis en balance avec les droits et libertés des personnes dont les données sont traitées (vos interlocuteurs clients, vos collègues mentionnés dans les prompts). Si l'usage de l'IA crée pour eux un risque disproportionné, l'intérêt légitime ne tient plus.

**Une information préalable.** Les personnes dont les données sont susceptibles d'être traitées doivent être informées. C'est pour cela que ce module existe et que DEF Ouest s'engage dans une démarche d'acculturation : on informe explicitement les collaborateurs et, plus largement, on construit une charte d'usage qui sera communiquée aux interlocuteurs externes.

**Le respect des autres principes.** Minimisation, sécurité, limitation de la conservation, exactitude. Tous les principes RGPD s'appliquent même quand l'intérêt légitime est invoqué.

**Cas particulier — les données sensibles.** Le RGPD identifie des catégories de données qui bénéficient d'une protection renforcée : santé, orientation sexuelle, opinions politiques, convictions religieuses, origine ethnique, données biométriques, données de localisation précise. **Ces données ne peuvent JAMAIS être traitées par un LLM sans précautions extrêmes et base légale renforcée.** En contexte DEF Ouest, le cas le plus fréquent serait des informations sur la santé d'un opérateur (arrêt maladie, restriction médicale) qui apparaîtraient dans un compte rendu. À retirer systématiquement avant tout usage IA.

### 4.3 — Les droits des personnes concernées

Le RGPD confère aux personnes dont les données sont traitées un ensemble de droits. Vous devez les connaître, parce qu'ils peuvent s'exercer y compris sur des traitements impliquant l'IA.

**Droit à l'information.** La personne doit savoir que ses données sont traitées, par qui, pour quoi, et combien de temps. Ce module y contribue côté collaborateurs ; une mention dans les communications clients DEF Ouest y contribuera côté externe.

**Droit d'accès.** La personne peut demander à savoir quelles données vous détenez sur elle, comment vous les utilisez et avec qui vous les partagez. Si quelqu'un demande *"avez-vous saisi mes données dans un LLM ?"*, la réponse doit pouvoir être documentée.

**Droit de rectification.** Une personne peut exiger la correction de données inexactes la concernant. Vous devez pouvoir intervenir sur les contenus produits avec son aide.

**Droit à l'effacement (droit à l'oubli).** Une personne peut, sous conditions, demander l'effacement de ses données. C'est l'un des points les plus délicats avec l'IA générative : effacer une donnée d'un modèle entraîné est techniquement très difficile. Raison de plus pour éviter d'y introduire des données identifiables.

**Droit d'opposition.** Une personne peut s'opposer à un traitement basé sur l'intérêt légitime. Si un client vous dit *"je ne veux pas que mes données soient traitées par une IA"*, vous devez en tenir compte.

**Droit à la portabilité.** Récupération des données dans un format structuré et leur transmission à un autre prestataire. Moins central pour notre contexte.

**Pas de décision entièrement automatisée.** Le RGPD (article 22) interdit en principe qu'une décision produisant des effets juridiques significatifs soit prise par une machine seule, sans intervention humaine. C'est l'une des raisons pour lesquelles AI Compass et ses cas d'usage prévoient systématiquement une **validation humaine** des contenus engageants.

---

## SECTION 5 — Quand on a un doute

C'est probablement la section la plus utile au quotidien. Aucun module ne couvrira jamais 100 % des cas. Vous serez régulièrement face à une situation qui ne ressemble exactement à aucun exemple. Voici comment réagir.

### 5.1 — Le réflexe en trois niveaux

**Niveau 1 — Je sais : j'applique.**

Vous reconnaissez la situation, vous savez quelle règle s'applique, vous agissez en conformité. Pas besoin d'aide extérieure. C'est l'objectif de la formation : que la majorité des situations se rangent dans ce niveau.

**Niveau 2 — J'ai un doute : je ne fais pas, je me renseigne.**

C'est le réflexe de sécurité. Quand vous n'êtes pas sûr, **vous ne faites pas**. Vous ne tentez pas en vous disant *"on verra bien"*. Le coût d'une erreur RGPD est très supérieur au coût d'attendre 30 minutes pour avoir une confirmation.

Ce que vous faites : vous mettez le travail de côté, vous interrogez le référent IA ou votre hiérarchie, vous reprenez une fois la réponse obtenue.

**Niveau 3 — Je vais le faire quand même : je documente et je remonte.**

Il arrive qu'on doive prendre une décision dans l'urgence, sans pouvoir attendre une validation. Dans ce cas, vous le faites, mais :

- vous documentez précisément ce que vous avez fait (quoi, avec quel outil, avec quelles données, pour quelle raison)
- vous remontez à votre hiérarchie et au référent IA dans les 24 heures
- vous acceptez que la décision puisse être contestée a posteriori

Cette pratique est précieuse parce qu'elle nourrit la connaissance collective de l'entreprise sur les cas-limites, et elle vous protège individuellement.

### 5.2 — À qui s'adresser chez DEF Ouest

**Le référent IA de l'entreprise** (DSI, Responsable Informatique et télécommunication). Premier interlocuteur pour toute question opérationnelle sur l'usage de l'IA : choix d'outil, conformité d'un usage, conduite à tenir face à une situation nouvelle. Il oriente, tranche ou remonte au niveau supérieur si nécessaire.

**Votre hiérarchie directe.** Pour les décisions engageant l'entreprise (validation d'une offre, choix de transmettre un document à un client, traitement d'un cas litigieux). Le manager de proximité est votre relais habituel ; le directeur métier (Travaux, Maintenance) pour les sujets plus structurants ; le DG pour les arbitrages stratégiques.

**Le DPO mutualisé du Réseau DEF**, s'il existe, pour les questions strictement RGPD complexes (exercice d'un droit par une personne, signalement d'un incident, AIPD).

**Les représentants du personnel.** Pour les questions touchant aux conditions de travail, à la surveillance, ou au déploiement d'outils impactant les collaborateurs.

### 5.3 — Les ressources externes fiables

Quand vous voulez vous renseigner par vous-même, voici les sources sérieuses.

**La CNIL** (cnil.fr) publie depuis 2024 des fiches pratiques sur l'IA générative, des recommandations pour les entreprises et un guide d'auto-évaluation. C'est la source de référence française.

**La Commission européenne** maintient une page officielle sur l'AI Act (digital-strategy.ec.europa.eu/en/policies/ai-act) avec le calendrier d'application, les FAQ officielles et les guidances en cours de publication.

**Le site du gouvernement français sur l'IA** (numerique.gouv.fr) publie des analyses et des outils pour l'administration et le secteur privé.

**Le Hub France IA** (hub-franceia.fr) publie des analyses sectorielles et des panoramas accessibles.

À éviter : les blogs commerciaux d'éditeurs d'outils IA, qui peuvent être pertinents techniquement mais sont rarement neutres juridiquement.

---

## SECTION 6 — Synthèse opérationnelle

### 6.1 — Les 4 règles d'or sur une page

> **Règle 1 — Outil maîtrisé uniquement.**
> Un outil IA validé par l'entreprise, avec contrat de sous-traitance RGPD. Tant que DEF Ouest n'a pas déployé un tel outil, utiliser un outil grand public reste l'exception, en respectant les trois règles suivantes.
>
> **Règle 2 — Minimisation des données.**
> Avant de coller un texte, retirer tout ce qui n'est pas indispensable à la tâche. Anonymiser les noms, codifier les montants, agréger les chiffres précis. Le bon réflexe : *"qu'est-ce que je peux retirer sans dégrader la qualité de la réponse attendue ?"*
>
> **Règle 3 — Validation humaine systématique.**
> L'IA propose, l'humain dispose. Aucun contenu généré par IA n'est diffusé en externe sans relecture critique. Plus le contenu engage DEF Ouest, plus la validation doit être formelle.
>
> **Règle 4 — Traçabilité et transparence.**
> Documenter ses usages, être transparent quand on est interrogé, ne jamais mentir sur le recours à l'IA. La transparence protège ; la dissimulation expose.

### 6.2 — Le checklist avant chaque prompt

À se poser en 10 secondes avant de cliquer "envoyer" sur un LLM.

1. **Est-ce que j'utilise un outil maîtrisé entreprise ?**
   *Si non, suis-je conscient que je dois redoubler de vigilance ?*

2. **Mon prompt contient-il des données identifiantes (nom, email, poste précis, identifiant) ?**
   *Si oui, est-ce que je peux les retirer ou les anonymiser ?*

3. **Mon prompt mentionne-t-il un client, un site ou un partenaire identifiable ?**
   *Si oui, ce client serait-il à l'aise s'il voyait ce que je m'apprête à transmettre ?*

4. **Le contenu généré sera-t-il diffusé en externe ?**
   *Si oui, ai-je prévu une relecture critique avant envoi ?*

5. **En cas de question, pourrais-je dire ce que j'ai fait sans gêne ?**
   *Si non, je m'arrête et je me renseigne.*

### 6.3 — Les 3 erreurs qui exposent le plus DEF Ouest

Sur la base des situations les plus fréquemment observées en PME B2B, voici les trois comportements qui créent le plus de risque pour DEF Ouest. Ce sont eux qu'il faut éliminer en priorité.

**Erreur n°1 — Coller un cahier des charges client brut dans un LLM grand public pour le résumer.**
*Pourquoi c'est grave* : transmission massive de données identifiantes, d'informations techniques sensibles, parfois d'éléments de sites critiques (OIV, SEVESO). C'est le scénario que ce module combat en priorité.
*Le bon réflexe* : extraction préalable manuelle d'une synthèse anonymisée, puis demande d'aide à l'IA sur cette synthèse.

**Erreur n°2 — Demander à un LLM de "vérifier" ou "compléter" des éléments techniques d'une offre.**
*Pourquoi c'est grave* : les LLM hallucinent fréquemment sur les normes, références et chiffres techniques. Une offre contenant une fausse référence APSAD ou une norme inventée est un risque commercial et juridique.
*Le bon réflexe* : les éléments techniques sont validés par le bureau d'études et par la documentation interne, jamais par un LLM.

**Erreur n°3 — Utiliser l'IA pour traiter des informations sur des collaborateurs ou des candidats.**
*Pourquoi c'est grave* : données potentiellement sensibles (évaluations, situations personnelles), risque de biais, encadrement RH spécifique (information du salarié, base légale). Ce cas d'usage n'est PAS couvert par le catalogue AI Compass et nécessite une démarche formelle.
*Le bon réflexe* : remonter au référent IA ou aux RH, ne pas tenter en autonomie.

---

## ANNEXE A — Glossaire opérationnel

**AI Act** — Règlement européen sur l'intelligence artificielle adopté en 2024, dont les obligations s'appliquent par paliers entre 2025 et 2027.

**AIPD (Analyse d'Impact relative à la Protection des Données)** — Étude formalisée à conduire avant un traitement présentant un risque élevé pour les personnes. Obligatoire dans certains cas, recommandée comme bonne pratique dans d'autres.

**AI literacy** — Maîtrise de l'IA. Obligation issue de l'article 4 de l'AI Act imposant aux organisations de garantir que leurs personnels disposent d'un niveau suffisant de compréhension de l'IA pour l'utiliser de manière éclairée.

**Base légale** — Fondement juridique qui rend licite un traitement de données personnelles (article 6 du RGPD). Doit être identifiée pour chaque traitement.

**CNIL** — Commission Nationale de l'Informatique et des Libertés. Autorité française de protection des données personnelles, compétente pour l'application du RGPD en France.

**Donnée personnelle** — Toute information se rapportant à une personne physique identifiée ou identifiable, directement ou indirectement.

**DPO (Data Protection Officer)** — Délégué à la protection des données. Personne désignée par l'organisation comme référent RGPD, obligatoire dans certains cas.

**Hallucination** — Production par un LLM d'une affirmation factuellement fausse, présentée avec assurance. Phénomène inhérent au fonctionnement statistique des modèles.

**Human-in-the-loop** — Principe de conception qui maintient l'humain comme acteur central de la décision, l'IA jouant un rôle d'assistance et non de substitution.

**LLM (Large Language Model)** — Grand modèle de langage. Famille de modèles d'IA capables de générer du texte. ChatGPT, Claude, Gemini, Mistral sont des LLM.

**LLM grand public** — Version d'un LLM accessible aux particuliers, gratuite ou payante (ChatGPT Plus, Gemini Advanced, etc.), sans garantie contractuelle entreprise.

**LLM maîtrisé entreprise** — Version d'un LLM avec contrat de sous-traitance RGPD signé entre l'organisation et le fournisseur, garanties de non-utilisation pour l'entraînement, et engagement de sécurité (Claude Enterprise, ChatGPT Enterprise, Copilot M365 entreprise, etc.).

**NIS2** — Directive européenne sur la cybersécurité applicable à un large périmètre d'entités essentielles et importantes, complémentaire du RGPD sur le volet sécurité.

**OIV (Opérateur d'Importance Vitale)** — Organisation dont l'activité est jugée essentielle au fonctionnement de la nation. Soumise à des obligations de sécurité renforcées.

**Prompt** — Instruction ou question saisie par l'utilisateur à destination du LLM. Peut contenir du texte, des données, des exemples.

**Responsable de traitement** — Entité qui détermine les finalités et les moyens d'un traitement de données personnelles. DEF Ouest est responsable de traitement pour ses traitements internes.

**RGPD** — Règlement général sur la protection des données. Règlement européen 2016/679 applicable depuis mai 2018.

**Sous-traitant** — Entité qui traite des données personnelles pour le compte du responsable de traitement, encadrée par un contrat de sous-traitance (article 28 RGPD). Un fournisseur de LLM utilisé professionnellement est un sous-traitant.

**Traitement** — Toute opération effectuée sur des données personnelles (collecte, enregistrement, organisation, structuration, conservation, consultation, utilisation, communication, effacement, etc.).

**Transparence** — Principe RGPD et obligation AI Act (article 50) imposant que l'usage de l'IA soit identifiable et explicable.

---

## ANNEXE B — Banque d'exemples par profil métier

Cette annexe est utilisée par l'agent pour générer des cas pratiques adaptés au profil de l'apprenant.

### Profil Commercial Travaux

**Situation 1 — Préparation d'une offre.**
*Tâche* : rédiger une offre pour un hôpital de 200 lits.
*Mauvaise pratique* : coller le cahier des charges du CHU de la ville X dans ChatGPT en demandant "résume-moi et propose une trame d'offre".
*Bonne pratique* : extraire manuellement les caractéristiques anonymisées (établissement de santé, ~200 lits, type de bâtiment, exigences réglementaires applicables) et travailler la trame sur cette base.

**Situation 2 — Réponse à un email client sensible.**
*Tâche* : répondre à un client mécontent suite à un incident de maintenance.
*Mauvaise pratique* : coller l'historique des échanges dans un LLM grand public en demandant "rédige une réponse apaisante".
*Bonne pratique* : décrire la situation en termes génériques (incident technique, client mécontent, enjeu de fidélisation), obtenir une trame de réponse, l'adapter au cas réel avec les éléments précis hors LLM.

**Situation 3 — Préparation d'un rendez-vous.**
*Tâche* : préparer un rendez-vous avec un nouveau prospect dont vous avez le nom de la société.
*Mauvaise pratique* : demander à un LLM "donne-moi des informations sur la société X et son responsable sécurité Y".
*Bonne pratique* : demander des informations génériques sur le secteur d'activité du prospect et les enjeux sécurité incendie typiques, puis se documenter sur les éléments spécifiques via les sources officielles (site web du prospect, presse).

### Profil Manager / Chargé d'affaires

**Situation 1 — Compte rendu de réunion d'équipe.**
*Tâche* : rédiger un compte rendu d'une réunion d'équipe ayant abordé les performances individuelles.
*Mauvaise pratique* : coller ses notes contenant les noms des collaborateurs et les commentaires sur leurs performances dans un LLM.
*Bonne pratique* : ne JAMAIS faire passer par un LLM des éléments d'évaluation individuelle. Rédaction manuelle obligatoire pour cette catégorie de contenu.

**Situation 2 — Préparation d'un plan d'action chantier.**
*Tâche* : structurer un plan d'action suite à un retard sur un chantier client.
*Mauvaise pratique* : coller les comptes rendus chantier (avec noms des techniciens, dates précises, coordonnées client) dans un LLM.
*Bonne pratique* : synthèse anonymisée préalable, génération de structure par l'IA, complétion manuelle avec les éléments réels.

### Profil Technicien

**Situation 1 — Rédaction d'un compte rendu d'intervention.**
*Tâche* : produire un compte rendu suite à une intervention de maintenance préventive.
*Mauvaise pratique* : dicter ou taper l'ensemble du compte rendu (avec adresse du site, nom du contact, observations sur l'installation) dans un LLM pour mise en forme.
*Bonne pratique* : pour les comptes rendus de routine, utiliser les modèles internes DEF Ouest. L'IA n'est pas indispensable et introduit un risque disproportionné.

**Situation 2 — Recherche d'information technique.**
*Tâche* : trouver une référence de norme applicable à une installation particulière.
*Mauvaise pratique* : faire confiance à la réponse brute d'un LLM sur une référence de norme.
*Bonne pratique* : utiliser le LLM pour identifier des pistes (familles de normes, organismes), puis VÉRIFIER systématiquement la référence exacte sur les sources officielles (AFNOR, CNPP, APSAD).

### Profil Fonction support (ADV, assistante, comptable)

**Situation 1 — Rédaction d'un courrier administratif.**
*Tâche* : rédiger une relance de facture impayée.
*Mauvaise pratique* : coller la facture (avec nom du client, montant, références) dans un LLM grand public.
*Bonne pratique* : générer un modèle de courrier de relance générique avec l'IA, puis renseigner manuellement les éléments client dans le modèle final.

**Situation 2 — Préparation d'un reporting interne.**
*Tâche* : produire un reporting hebdomadaire des activités support.
*Mauvaise pratique* : coller les données extraites de l'ERP (noms clients, montants précis) dans un LLM pour mise en forme.
*Bonne pratique* : agréger les données avant transmission (chiffres globaux, codification des clients), demander la mise en forme sur les données agrégées.

---

## ANNEXE C — Foire aux questions

**Q1 — Et si je supprime ma conversation dans ChatGPT, c'est OK ?**

Non. La suppression de votre conversation côté interface ne signifie pas que les données sont effacées des serveurs du fournisseur. Selon les conditions d'utilisation, OpenAI conserve les données pour des durées variables (généralement 30 jours minimum, parfois davantage à des fins de modération ou de prévention des abus). De plus, si vos données ont déjà été utilisées pour l'entraînement, elles sont intégrées au modèle de manière irréversible. La suppression n'efface pas la transmission initiale.

**Q2 — Puis-je utiliser DeepL pour traduire un mail client ?**

DeepL est un service de traduction qui traite les contenus saisis. Les mêmes principes RGPD s'appliquent : si le mail contient des données identifiantes (nom du contact client, références d'affaires, montants), vous transmettez ces données à un sous-traitant. DeepL propose une offre Pro avec garanties renforcées (DeepL Pro avec engagement de non-conservation des données saisies) qui est préférable à la version gratuite pour un usage professionnel. En version gratuite, anonymisez avant traduction.

**Q3 — Que faire si mon manager me demande de coller un document client dans ChatGPT pour gagner du temps ?**

Vous expliquez les risques avec calme et professionnalisme (transmission de données à un tiers, RGPD, exposition de DEF Ouest), et vous proposez une alternative : extraction préalable d'une synthèse anonymisée, puis usage de l'IA sur cette synthèse. Si la pression se maintient, vous documentez la demande, vous remontez au référent IA, et vous laissez l'arbitrage à la hiérarchie. Vous n'avez pas à prendre seul un risque de conformité pour gagner 10 minutes.

**Q4 — J'ai utilisé ChatGPT avec des données clients pendant six mois sans le savoir. Que faut-il faire ?**

Pas de panique, mais action immédiate. Vous remontez au référent IA en décrivant honnêtement ce qui s'est passé (volume, type de données, fréquence). Cette information permettra de qualifier le risque et, le cas échéant, de prendre les mesures appropriées (analyse d'impact, information des personnes concernées, signalement à la CNIL si la violation est avérée et significative). La transparence est protectrice ; la dissimulation aggrave juridiquement la situation.

**Q5 — Les outils internes Microsoft 365 sont-ils des outils maîtrisés ?**

Microsoft 365 Copilot, déployé dans le cadre d'une licence entreprise Microsoft 365, est considéré comme un outil maîtrisé entreprise. Microsoft signe un contrat de sous-traitance RGPD, garantit l'hébergement UE et l'absence d'utilisation des données pour l'entraînement des modèles. C'est différent de Copilot grand public (associé à un compte Microsoft personnel) qui n'offre pas ces garanties.

**Q6 — Est-ce que je peux utiliser l'IA pour rédiger un avis sur un collaborateur ?**

Non. Les éléments d'évaluation de personnes (collaborateurs, candidats, sous-traitants) sont des données sensibles dans le contexte professionnel, soumis à un encadrement RH spécifique et à des obligations d'information renforcées. Ce cas n'est PAS couvert par le catalogue AI Compass. Si vous avez besoin d'aide rédactionnelle sur ce type de contenu, voyez avec les RH ou avec le référent IA — il faudra probablement un dispositif spécifique avec base légale, information du collaborateur et garde-fous techniques.

**Q7 — Quelle différence entre Claude et Claude Enterprise ?**

Claude (claude.ai) en version grand public ou Pro est un outil destiné aux particuliers, sans contrat d'entreprise. Claude Enterprise (ou Claude pour les équipes) est l'offre destinée aux organisations, avec contrat de sous-traitance, engagement de non-utilisation pour l'entraînement, journalisation, gestion centralisée des utilisateurs. Pour un usage professionnel, c'est cette offre qu'il faut viser.

**Q8 — Si je travaille sur un site OIV, ai-je le droit d'utiliser l'IA tout court ?**

L'usage de l'IA n'est pas interdit, mais il est très encadré. Pour les informations détaillées sur des sites OIV ou SEVESO (configurations sécuritaires, vulnérabilités identifiées, plans d'intervention), l'usage d'un LLM — même maîtrisé — est à proscrire. Pour les contenus génériques sans lien avec ces sites (méthodologie d'intervention, présentation type, références réglementaires), l'usage est possible avec les règles habituelles. En cas de doute, escalade au référent IA et à la hiérarchie : ce périmètre relève également de NIS2 et parfois de la sécurité nationale.

**Q9 — L'IA peut-elle remplacer la formation continue obligatoire ?**

Non. L'IA peut accompagner votre montée en compétences, vous aider à structurer des contenus, à préparer des points de formation. Elle ne remplace pas les formations qualifiantes (CACES, habilitations électriques, formations APSAD) qui restent encadrées réglementairement et délivrées par des organismes habilités. AI Compass lui-même est un dispositif d'acculturation et de sensibilisation, pas un substitut aux formations métier.

**Q10 — Que dois-je faire si je vois un collègue exposer des données clients dans ChatGPT ?**

Vous avez plusieurs niveaux d'action selon votre relation avec ce collègue et la sévérité de la situation. **En premier lieu, parlez-en avec le collègue concerné** sans posture moralisatrice, en lui expliquant ce que vous avez appris dans ce module. La plupart du temps, c'est suffisant — il ignorait simplement les risques. **En second lieu, si la pratique persiste ou si elle concerne des informations très sensibles** (sites OIV, données financières précises, informations RH), vous remontez au référent IA pour qu'une action de sensibilisation ciblée soit menée. Vous n'êtes pas dans une posture de délation : vous protégez DEF Ouest et vos clients. La règle est de remonter par la voie de la sensibilisation, pas par la voie disciplinaire.

---

*Fin du Module 3 — RGPD et IA générative.*
*Module suivant recommandé : Module 4 — Cadre AI Act.*
