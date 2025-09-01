# Ingestão da Base SAVVIX (RAG)

## Passos
1. Ler arquivos `.md` de `kb/` e `prompts/` (se for útil) e `faqs/*.json`, `glossary/*.json`.
2. **Chunking** (800–1200 chars; overlap 150). Cada `##` sugere boundary.
3. Gerar **embeddings** para cada chunk (guardar `slug`, `title`, `category`, `tags`, `language`, `source`).
4. Gravar no banco vetorial (Qdrant/Weaviate/Pinecone/Mongo Atlas com vetor).
5. Implementar **busca híbrida** (keyword + vetor) e fundir por **RRF**.
6. Em `/ask`, recuperar top-6 chunks, montar contexto e responder com o *system prompt* de `prompts/agent_system_prompt.txt`.

## Dicas
- Normalize markdown removendo HTML, mantendo títulos.
- Deduplicate por `hash(content)`.
- Não indexar preços ou datas sem fonte validada.
- Reindexar no máximo a cada 24h ou em *webhook* de mudança no Git.

## Campos mínimos por chunk
`id`, `slug`, `title`, `content`, `category`, `tags`, `language`, `source`, `last_reviewed_at`.
