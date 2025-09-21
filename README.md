# Personal Patient Manager — MVP v3

Novidades desta versão:
- **Gráficos de evolução** (Chart.js) para **UPDRS-III**, **SARA**, **mFARS**.
- **Campos OFF/ON** e **wearing-off** em **UPDRS-III** (inclui minutos desde última dose).
- **Modo Leitura Rápida**: highlights com tendências, últimas consultas, medicações em uso e red flags heurísticas.
- Mantém: LLM local (WebLLM), Supabase (tabelas+RLS), anexos privados, exportar PDF.

## Passo a passo
1) Supabase → SQL Editor → cole `schema.sql` (v2 e v3 são compatíveis). Pegue **Project URL** e **anon key**.
2) `index.html` → substitua `SUPABASE_URL` e `SUPABASE_ANON_KEY`.
3) Publique em Netlify Drop / Vercel / GitHub Pages. No Horizons, aponte um botão para a URL.
4) Use no Galaxy S23 Ultra → aperte **“Baixar modelo”** para usar WebLLM (WebGPU).

## Notas
- Os dados de OFF/ON/wearing-off são salvos dentro de `neuro_exams.content` (JSONB), junto com `total`.
- O modo leitura rápida é heurístico a partir dos dados existentes; se quiser, posso adicionar um botão **“Gerar com LLM”** com prompt dedicado para highlights.
- Para gráficos, edite à vontade os rótulos ou exporte CSV se quiser levar para planilha.

— Build v3 gerado em 2025-09-21T00:20:56
