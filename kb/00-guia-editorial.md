---
slug: guia-editorial
title: Guia Editorial e Padrões da Base
category: Governança
tags: [guia, estilo, governanca, qualidade]
language: pt-BR
version: 1.0.0
last_reviewed_at: 2025-08-31
owner: conteudo@savvix.com.br
status: published
---

# Guia Editorial da Base de Conhecimento — SAVVIX

## Objetivo
Garantir consistência, precisão e segurança das informações usadas pelo agente de IA (RAG) e por equipes internas.

## Estilo
- Tom: claro, direto, amigável.
- Evite jargões quando houver termo simples equivalente.
- Use títulos (`#`, `##`, `###`) e listas objetivas.
- Prefira exemplos reais e breves.

## Escopo
- Incluir: funcionamento do app, painel, diferenciais, comerciais (B2B/B2C), visão técnica, privacidade.
- Não incluir: dados sigilosos, credenciais, roadmap não público, estimativas não validadas.

## Regras de Conteúdo
- Indique fontes internas com *slug* dos artigos (ex.: `[visao-geral-savvix]`).
- Não invente preços ou datas. Se incerto, sinalize: “verifique o painel/admin”.
- Dados pessoais: orientar o usuário a abrir ticket pelo suporte oficial.

## Sinais de Qualidade
- `last_reviewed_at` ≤ 90 dias.
- Ortografia verificada.
- Links internos válidos.
- Seção “Dúvidas frequentes” atualizada conforme analytics.

## Estrutura Recomendada por Arquivo
1. **Resumo** (3–6 linhas)
2. **Tópicos-chave** (bullets)
3. **Como fazer** (se aplicável)
4. **Métricas / Glossário** (se aplicável)
5. **Limitações / Observações**

## Metadados (YAML)
- `slug`, `title`, `category`, `tags`, `language`, `version`, `last_reviewed_at`, `owner`, `status`.

## Chunking para Banco Vetorial
- Tamanho-alvo 800–1.200 caracteres, *overlap* ~150.
- Respeite seções (`##`) como unidades de chunk.
- Preservar `slug` e `title` como metadados de cada chunk.

## Privacidade & Segurança
- Não exponha chaves, URIs, tokens.
- Dados pessoais somente em contexto de suporte.
