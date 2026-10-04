# Dépenses — qui paie quoi, et quand

Projet **AgentIA / IA Factor** — associés : **Daouda Danso** (technique) et **Régis Pepin** (chef de projet).
Dernière mise à jour : 27/09/2026.

> Conventions : montants en **$** quand le fournisseur facture en dollars (Hostinger, Anthropic),
> conversion indicative **1 $ ≈ 0,92 €** (hypothèse, à ajuster). « À renseigner » = montant à
> reprendre sur la facture. Les montants marqués *(estimation)* ne sont pas encore engagés.

## 1. Déjà payé

| Date | Dépense | Fournisseur | Montant | Payé par | Remarque |
|---|---|---|---|---|---|
| 26/09/2026 | Domaine `ai-team.fr` | Hostinger | **10,25 $** | Daouda | Abandonné, **non renouvelé** (aucune autre dépense à venir) |
| 26/09/2026 | Domaine `ia-factor.fr` (1re année) | Hostinger | à renseigner | Daouda | Domaine du projet |
| 26/09/2026 | Domaine `ia-factor.com` (1re année) | IONOS | **10 €** | **Régis** | Protège la marque ; usage à décider (redirection vers `ia-factor.fr` recommandée) |
| 26/09/2026 | VPS KVM 2 (1re période) | Hostinger | à renseigner (facture hPanel) | Daouda | Serveur de la plateforme et du site |
| 27/09/2026 | Crédits API Claude (prépayés) | Anthropic | 5,00 $ + 1,00 $ de taxes = **6,00 $** | Daouda | Expirent le 27/09/2027 ; recharge automatique désactivée |
| mensuel | Abonnement Claude (utilisé avec Claude Code pour développer) | Anthropic | à renseigner | Daouda | À décider : dépense du projet ou dépense personnelle (voir §4) |

## 2. Dépenses récurrentes

| Poste | Fournisseur | Montant | Fréquence | Prochaine échéance | Payé par | Remarque |
|---|---|---|---|---|---|---|
| **VPS KVM 2** (2 vCPU, 8 Go) | Hostinger | **24,49 $** (~22,50 €) | mensuel | **26/10/2026**, puis le 26 de chaque mois | Daouda | Facturation au mois : comparer avec un engagement 12/24 mois avant l'échéance |
| **Domaine `ia-factor.fr`** | Hostinger | **12,99 $** (~12 €) | annuel | 30/08/2027 (date affichée par hPanel) | Daouda | Renouvellement automatique activé |
| **Domaine `ia-factor.com`** | IONOS | tarif de renouvellement à renseigner (1re année : 10 €) | annuel | **26/09/2027** | Régis | Renouvellement automatique **activé** (confirmé le 27/09/2026) |
| **API Claude** (réponses de l'agent) | Anthropic | à l'usage, **prépayé** | recharges ponctuelles | quand le solde approche de 0 | Daouda | Démo plafonnée à 0,30 $/jour (≤ ~9 $/mois) ; clients : ~2–5 $/mois chacun *(estimation)* |
| **Abonnement Claude** (Claude Code) | Anthropic | à renseigner | mensuel | à renseigner | Daouda | Outil de développement |
| Adresse e-mail `contact@ia-factor.fr` | à choisir | 0–3 €/mois *(estimation)* | mensuel | — | à définir | **Pas encore créée** : aucun forfait web/e-mail chez Hostinger. Nécessaire pour Meta, Let's Encrypt, contact |
| Messages WhatsApp (rappels la veille) | Meta | quelques centimes par message *(à vérifier sur la grille Meta)* | à l'usage | après la mise en service WhatsApp | à définir | Réponses aux clients dans les 24 h : gratuites |
| Frais de paiement des clients | Banque | **0 €** : les clients paient par **virement** (décidé le 04/10/2026) | — | — | — | Pas de carte bancaire, donc pas de Stripe |

## 3. Gratuit (à surveiller)

| Service | Usage | Limite gratuite |
|---|---|---|
| GitHub | Dépôts privés `agentia`, `ia-factor-site`, CI | Minutes de CI incluses dans le plan gratuit |
| Telegram | Bot de démo, notifications gérant | — |
| Caddy, Let's Encrypt | HTTPS | — |
| Uptime Kuma, GlitchTip | Supervision, erreurs | Auto-hébergés sur le VPS |
| Google Cloud (API Calendar) | Intégration agenda (phase C) | Quotas gratuits largement suffisants |
| Meta (vérification Business, API WhatsApp) | Canal WhatsApp | Accès gratuit ; seuls les templates sont payants |
| Backblaze B2 | Sauvegardes (à mettre en place) | 10 Go |

## 4. Dépenses ponctuelles à prévoir *(estimations)*

| Poste | Montant estimé | Quand | Payé par | Remarque |
|---|---|---|---|---|
| Création de la structure juridique | 0 € (micro-entreprise) à ~300–500 € (SASU/SAS avec annonce légale) | avant le 1er client payant | à définir | Le choix conditionne aussi la comptabilité (voir analyse) |
| Dépôt de marque INPI « AgentIA » (1 classe) | ~190 € *(à vérifier sur inpi.fr)* | avant la communication publique | à définir | Vérifier d'abord la disponibilité (`agentia.fr` appartient à un tiers) |
| Relecture juridique (mentions légales, confidentialité, CGV, contrat de sous-traitance) | ~500–1 000 € | avant le 1er client payant | à définir | Indispensable pour le RGPD |
| Assurance responsabilité civile professionnelle | ~150–400 €/an | à la création | à définir | |
| Compte bancaire professionnel | 0–10 €/mois | à la création | société | |
| Expert-comptable | 0 € (micro) à ~80–150 €/mois (société) | à la création | société | |

## 5. Règles de répartition entre associés — **à décider ensemble**

Aujourd'hui, **presque tout est payé par Daouda** (comptes Hostinger, Anthropic et GitHub à son
nom) ; **Régis** a payé le domaine `ia-factor.com` (compte IONOS à son nom). Points à trancher :

1. **Clé de répartition** : 50/50 ? Proportionnelle aux parts de la future société ? Chacun paie
   « son » périmètre (technique vs commercial) ?
2. **Outils personnels** : l'abonnement Claude (Claude Code) et le temps passé sont-ils des
   dépenses du projet ?
3. **Avances** : tant que la société n'existe pas, chaque dépense avancée est notée dans le
   tableau ci-dessous. À la création, les avances deviennent un **compte courant d'associé**
   (remboursable par la société) et les abonnements passent sur la carte de la société.
4. **Validation** : au-delà d'un seuil (ex. 100 €), une dépense est validée par les deux associés
   avant d'être engagée.

### Suivi des avances

| Date | Dépense | Montant | Avancé par | Part Daouda | Part Régis | Remboursé le |
|---|---|---|---|---|---|---|
| 26/09/2026 | Domaine `ai-team.fr` | 10,25 $ | Daouda | | | |
| 26/09/2026 | Domaine `ia-factor.fr` | à renseigner | Daouda | | | |
| 26/09/2026 | VPS KVM 2, 1re période | à renseigner | Daouda | | | |
| 26/09/2026 | Domaine `ia-factor.com` | 10 € | Régis | | | |
| 27/09/2026 | Crédits API Claude | 6,00 $ | Daouda | | | |
| | | | | | | |

## 6. Calendrier des prochains paiements

| Date | Paiement | Montant | Payeur actuel |
|---|---|---|---|
| **26/10/2026** | VPS KVM 2 | 24,49 $ | Daouda (carte enregistrée chez Hostinger) |
| mensuel | Abonnement Claude | à renseigner | Daouda |
| selon usage | Recharge des crédits API Claude | 5–20 $ | Daouda |
| 26/11/2026 et le 26 de chaque mois | VPS KVM 2 | 24,49 $ | Daouda |
| 30/08/2027 | Domaine `ia-factor.fr` | 12,99 $ | Daouda |
| 26/09/2027 | Domaine `ia-factor.com` (renouvellement automatique) | tarif IONOS à renseigner | Régis (IONOS) |
| 27/09/2027 | Expiration des crédits API non consommés | — | — |

## À compléter

- [ ] Montants réels : `ia-factor.fr` (1re année), VPS (1re période), abonnement Claude, tarif de renouvellement de `ia-factor.com`
- [ ] Solution e-mail pour `contact@ia-factor.fr`
- [ ] Règles de répartition (§5) validées par Daouda et Régis
- [ ] Forme juridique et date de création de la société
