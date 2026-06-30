---
name: grill-me
description: >-
  Interview structurée pour extraire la connaissance de l'utilisateur (business,
  client, projet, process) et la persister en mémoire AVQN (faits clé/valeur via
  avqn_memory_set). À déclencher sur « grill me », « interviewe-moi », ou quand le
  contexte d'un sujet est trop maigre pour bien agir.
---

# Grill me — extraction de connaissance

But : transformer ce que l'utilisateur a en tête en faits persistants dans la mémoire AVQN.

## Étapes

1. **Cadrer.** Si le thème n'est pas donné, le demander (l'utilisateur lui-même, son activité,
   un client, une offre, un process…). Faire `avqn_memory_search` sur le thème pour ne pas
   re-poser des questions dont la réponse est déjà en mémoire.
2. **Interviewer par vagues.** 3 à 5 questions max par message, précises et concrètes : faits,
   chiffres, préférences, décisions prises, exceptions, ce qui agace. Rebondir sur les réponses,
   creuser les zones floues. Continuer tant qu'il reste du flou ou que l'utilisateur ne dit pas
   stop (viser 15–30 questions au total sur un thème riche).
3. **Exploiter les sources fournies.** Si des documents (CV, offres, PDF) ou des liens sont
   joints, les LIRE intégralement (web_fetch / lecture fichier) et croiser avec les réponses :
   ça enrichit, corrige les trous de mémoire, et révèle le niveau de discours déjà public
   (utile pour calibrer privé vs public).
4. **Synthétiser et persister.** En fin d'interview (ou à un checkpoint sur demande — ne pas
   attendre la fin pour les gros morceaux), distiller en faits durables et écrire via
   `avqn_memory_set`, clés en namespace (`core:`, `client:<nom>.`, `projet:<slug>.`…), tags
   pertinents. Les chiffres/états périssables : tag `snapshot` + mention de la source live dans
   la valeur. Marquer explicitement les sections PRIVÉES (faits sensibles, guidance interne) :
   « ⚠️ ne jamais utiliser publiquement sans décision explicite ».
5. **Faire valider.** Lister les clés écrites avec un résumé d'une ligne chacune ; corriger ce
   qui est contesté. Relever 2-3 insights transverses si l'interview en a fait émerger.

## Ton

Curieux et direct, mais humain. Si un sujet sensible ou personnel émerge, marquer une **petite**
pointe de considération sincère — une phrase, pas des caisses — avant de poursuivre. Le bon
dosage : ni froideur d'archiviste, ni excès ; accueillir, honorer en une ligne, continuer.
