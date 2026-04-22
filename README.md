# 3 Agents IA n8n — Google Ads & Meta

Workflows n8n prêts à importer pour automatiser la gestion de campagnes paid media.

## Les 3 agents

| Agent | Fichier | Description |
|-------|---------|-------------|
| Agent 1 | [agent1_google_ads_performance_intelligence.json](agent1_google_ads_performance_intelligence.json) | Revue de compte Google Ads en 10 min — alertes, tendances, recommandations |
| Agent 2 | [agent2_search_terms_triage.json](agent2_search_terms_triage.json) | Triage de 2 000 termes de recherche en 60 secondes |
| Agent 3 | [agent3_restructuring_brief.json](agent3_restructuring_brief.json) | Brief de restructuration complet avant de toucher un seul paramètre |

## Installation

1. Ouvrir n8n → Import workflow → coller le contenu du fichier JSON
2. Créer une credential **HTTP Header Auth** avec ta clé API Anthropic :
   - Header name : `x-api-key`
   - Header value : ta clé `sk-ant-....`
3. Remplacer `YOUR_ANTHROPIC_CREDENTIAL_ID` dans chaque workflow par l'ID de ta credential
4. Activer le workflow

## Stack

- **n8n** (self-hosted ou cloud)
- **Claude API** (Anthropic) — Haiku pour Agent 2, Sonnet pour Agents 1 & 3
- Webhook POST → traitement → JSON response

## Auteur

Aliou Ba — [Automation Act](https://automationact.com)
