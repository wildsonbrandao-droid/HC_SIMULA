# HC_SIMULA — Guia interativo de Exame Físico + Radiologia

Site single-page (GitHub Pages). Navegação por âncoras no menu superior:
Pulmonar · Síndromes pulmonares · Cardiovascular · Sons & sopros · Cardiopatias · Questões ENAMED · **Radiologia (HC3)**.

## Estrutura
- `index.html` — app principal (~248 KB, sem base64).
- `hc3-radiologia.html` — versão standalone do HC3 (tela cheia), imagens externalizadas.
- `img/` — figuras do exame físico/cardiopatias (Porto) + `img/hc3/` (94 imagens da Radiologia).
- `audio/` — 11 áudios de ausculta (bulhas, sopros, galopes).
- `.nojekyll` — evita processamento Jekyll no GitHub Pages.

## Integração do HC3 (aba Radiologia)
Feita como sub-aba interna (não iframe):
- 94 imagens base64 extraídas para `img/hc3/hc3-001..094.jpg`.
- CSS do HC3 reescopado sob `.hc3-app` (sem colisão com o HC_SIMULA).
- Tema escuro do HC3 remapeado para o tema claro do HC_SIMULA.
- Sidebar off-canvas convertida em sub-navegação inline (17 seções).
- JS do HC3 isolado em IIFE; seletores globais (`main section`, `nav button`) reescopados para `#hc3-app`.
