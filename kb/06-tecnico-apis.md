---
slug: tecnico-apis
title: Visão Técnica — Endpoints (Resumo)
category: Técnico
tags: [api, endpoints, dev, integracao]
language: pt-BR
version: 1.0.0
last_reviewed_at: 2025-08-31
owner: tech@savvix.com.br
status: published
---

# Endpoints — Resumo

> Rotas e contratos podem evoluir. Consulte o repositório e o Postman/Swagger da versão vigente.



## Observações
- **Pagamentos**: quando existirem no app, devem usar provedores certificados (ex.: Pix dinâmico via gateway externo).
- **Segurança**: HTTPS, tokens curtos, escopos e *rate limits*. Evitar dados sensíveis nos logs.
