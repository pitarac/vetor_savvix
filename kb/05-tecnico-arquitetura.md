---
slug: tecnico-arquitetura
title: Visão Técnica — Arquitetura
category: Técnico
tags: [arquitetura, backend, mobile, infra, escalabilidade]
language: pt-BR
version: 1.0.0
last_reviewed_at: 2025-08-31
owner: tech@savvix.com.br
status: published
---

# Visão Técnica — Arquitetura

## Stack
- **App**: React Native (Expo) — push, leitura de QR Code, filtros por categoria/segmento/estado/cidade.
- **Backend**: Node.js (Express) com microserviços, autenticação, rate-limiting, cache.
- **Banco**: MongoDB Atlas (índices planejados; leitura via réplicas quando aplicável).
- **Infra**: Nginx, PM2, logs estruturados, monitoramento.

## Funcionalidades-Chave
- **Login social** (Google, Facebook, Apple) e **refresh tokens**.
- Registro de **dispositivos**: userId, deviceToken, latitude, longitude, modelo, OS.
- Métricas de resgate, limites e regras (ex.: 5 ações/dia por usuário em fluxo de jogo/quizz, quando aplicável).
- Filtros dinâmicos de **categoria/segmento/estado/cidade**.

## Escalabilidade e Resiliência
- **Cache** agressivo em endpoints de leitura.
- **Fila** para envio de push/relatórios.
- **Healthchecks** e **backpressure** em pico de tráfego.
- **N+1** instâncias com PM2/containers, *graceful shutdown*.
