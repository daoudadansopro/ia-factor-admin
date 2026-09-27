# Analyse budgétaire et projections — AgentIA

Dernière mise à jour : 27/09/2026. Base : la présentation commerciale (offres, prix, coûts de
revient annoncés) et les coûts **mesurés** sur la plateforme en production.

> ⚠️ Ce sont des **projections**, pas des prévisions : chaque chiffre dépend d'hypothèses listées
> ici. Les résultats sont **avant impôts et cotisations sociales**, et **sans rémunération du temps
> des associés**. Conversion indicative 1 $ ≈ 0,92 €.

## 1. Les offres (présentation initiale)

| Offre | Installation | Abonnement | Coût de revient annoncé | Marge annoncée | Statut |
|---|---|---|---|---|---|
| **Entreprise** (TPE/PME) | 199 € | 30 €/mois | 10–22 €/mois | ≈ 85 % | **MVP en cours** |
| Particulier | 149 € | 20 €/mois | 7–15 €/mois | ≈ 80 % | Après les pilotes (planning 07) |
| AideHandicap | 149–199 € | 20–30 €/mois | 7–15 €/mois | ≈ 80 % | Nécessite un hébergement de santé certifié (coûts à revoir) |

La projection ci-dessous ne porte que sur l'offre **Entreprise**. Les deux autres dépendent de
prérequis juridiques et d'hébergement non chiffrés (voir `agentia/docs/target-architecture-individuals.md`).

## 2. Coût unitaire d'un client Entreprise

La présentation prévoyait Make + 360dialog + OpenAI (10–22 €/mois). L'architecture retenue
(plateforme maison, WhatsApp en direct, Claude Haiku) coûte moins cher :

| Poste par client et par mois | Estimation | Base |
|---|---|---|
| IA (Claude Haiku) | 2–5 € | Mesuré : ~0,2 centime par message, ~1 000 messages/mois pour un commerce actif |
| Messages WhatsApp à l'initiative du commerce (rappels) | 0,5–2 € | *À confirmer* avec la grille Meta ; les réponses sous 24 h sont gratuites |
| Frais Stripe sur l'abonnement | 0,70 € | 1,5 % + 0,25 € sur 30 € *(à vérifier)* |
| Part d'hébergement | incluse dans les coûts fixes | Le VPS actuel suffit pour plusieurs dizaines de clients |
| **Total variable** | **≈ 4–8 €** | vs 10–22 € annoncés |
| **Marge sur coût variable** | **≈ 22–26 € (73–87 %)** | |

À l'installation : 199 € encaissés, moins ~3,24 € de frais Stripe. Le temps d'installation
(1–2 jours selon la présentation) n'est pas valorisé ici.

## 3. Coûts fixes mensuels

| Poste | Scénario central | Remarque |
|---|---|---|
| VPS KVM 2 | 22,50 € | 24,49 $/mois |
| Domaine `ia-factor.fr` | 1 € | 12,99 $/an |
| Domaine `ia-factor.com` | ~1 € | payé par Régis (10 € la 1re année) |
| E-mail professionnel | 2 € | *hypothèse* |
| Abonnement Claude (Claude Code) | 20 € | **hypothèse, à remplacer par le montant réel** |
| Démo publique (API Claude) | 3 € | Plafond technique : 0,30 $/jour, soit ~8 €/mois |
| Assurance RC Pro | 20 € | *estimation* (~240 €/an) |
| Banque pro | 5 € | *estimation* |
| **Total** | **≈ 76 €/mois** | 85 € dans le scénario pessimiste |
| + expert-comptable si société | +80 à 150 € | 0 € en micro-entreprise |

Dépenses ponctuelles prises en compte : dépôt INPI (190 €, mois 2), relecture juridique
(800 € central, 1 000 € pessimiste, mois 3). Création en **micro-entreprise** (0 €).

## 4. Seuil de rentabilité

Marge par client ≈ 24 €/mois (30 € − ~6 € de coûts variables).

| Structure | Coûts fixes | Clients nécessaires pour couvrir les coûts fixes |
|---|---|---|
| Micro-entreprise | ~75 €/mois | **4 clients** |
| Société avec expert-comptable | ~195 €/mois | **9 clients** |

Les frais d'installation (199 €) financent en plus le démarrage : **5 installations couvrent les
dépenses ponctuelles** (INPI + relecture juridique).

## 5. Projections sur 24 mois (octobre 2026 → septembre 2028)

### Hypothèses

| | Pessimiste | Central | Optimiste |
|---|---|---|---|
| 1er client payant | janv. 2027 (M4) | déc. 2026 (M3) | déc. 2026 (M3) |
| Nouveaux clients par mois ensuite | 1 | 2 | 4 |
| Résiliation mensuelle | 4 % | 2 % | 1 % |
| Coût variable par client | 10 € | 6 € | 4 € |
| Coûts fixes | 85 €/mois | 75 €/mois | 75 €/mois |
| Octobre–novembre 2026 | pilotes gratuits | pilotes gratuits | pilotes gratuits |

### Résultats

| | Pessimiste | Central | Optimiste |
|---|---|---|---|
| Clients actifs à 12 mois (sept. 2027) | ~8 | ~17 | ~35 |
| Clients actifs à 24 mois (sept. 2028) | ~14 | ~35 | ~77 |
| Revenu mensuel récurrent à 12 mois | ~230 € | ~520 € | ~1 070 € |
| Revenu mensuel récurrent à 24 mois | ~430 € | ~1 060 € | ~2 310 € |
| **Chiffre d'affaires année 1** (oct. 26 – sept. 27) | ~3 000 € | ~6 600 € | ~12 900 € |
| **Chiffre d'affaires année 2** | ~6 600 € | ~14 700 € | ~30 600 € |
| Résultat année 1 | ~+330 € | ~+4 000 € | ~+10 000 € |
| Résultat année 2 | ~+4 000 € | ~+11 500 € | ~+26 200 € |
| Besoin de trésorerie maximum (creux) | **~1 450 €** (déc. 2026) | **~1 000 €** (déc. 2026) | **~1 000 €** (déc. 2026) |
| Trésorerie cumulée redevient positive | août 2027 | mars 2027 | février 2027 |

### Détail du scénario central

| Mois | Clients actifs | CA du mois | Résultat du mois | Cumul |
|---|---|---|---|---|
| déc. 2026 (M3) | 1 | 229 € | −656 € | −996 € |
| mars 2027 (M6) | ~7 | 603 € | +475 € | +297 € |
| juin 2027 (M9) | ~12 | 767 € | +603 € | +1 980 € |
| sept. 2027 (M12) | ~17 | 922 € | +723 € | +4 032 € |
| mars 2028 (M18) | ~27 | 1 204 € | +943 € | +9 153 € |
| sept. 2028 (M24) | ~35 | 1 455 € | +1 137 € | +15 502 € |

## 6. Lecture

- **Le projet est peu risqué financièrement** : le besoin de trésorerie reste autour de 1 000 à
  1 500 €, principalement la relecture juridique et l'INPI, pas l'infrastructure.
- **Le vrai coût est le temps** : 1 à 2 jours d'installation par client, le suivi et la
  prospection ne sont pas chiffrés. À 20 clients par an, c'est 20 à 40 jours d'installation.
  C'est l'argument pour automatiser l'onboarding (planning 04).
- **Le revenu dépend surtout du rythme de signature**, pas des coûts : passer de 2 à 4 nouveaux
  clients par mois double le résultat. Régis (chef de projet) porte cet indicateur.
- **Un complément de revenu, pas un salaire**, à ce stade : même en optimiste, ~2 300 € de
  revenu mensuel récurrent à 24 mois, avant cotisations (micro-entreprise : ~21–25 % du CA pour
  les prestations de services, *à vérifier*) et avant partage entre associés.
- **Particulier et AideHandicap** ouvrent des marchés bien plus larges (19–20 M de seniors,
  13–14 M de personnes en situation de handicap) mais avec des coûts d'hébergement de santé et
  des prérequis juridiques à chiffrer avant toute projection.

## 7. Indicateurs à suivre chaque mois

| Indicateur | Source |
|---|---|
| Nouveaux clients, résiliations, clients actifs | Suivi commercial (Régis) |
| Revenu mensuel récurrent, installations facturées | Stripe / facturation |
| Coût IA par client | Rapport quotidien 📊 de la plateforme, Console Anthropic |
| Coûts fixes réels | `depenses.md` |
| Conversion démo → client | Invitations envoyées (`/invitations`) vs signatures |

## 8. Points à valider

- [ ] Montant réel de l'abonnement Claude (hypothèse : 20 €/mois)
- [ ] Forme juridique (micro-entreprise ou société) → coûts fixes et fiscalité
- [ ] Grille WhatsApp de Meta pour les messages « utility » en France
- [ ] Taux et seuils de cotisations / TVA en vigueur
- [ ] Rythme de signature réaliste selon Régis (1, 2 ou 4 par mois ?)
