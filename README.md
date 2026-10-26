# VisioIndústria (protótipo experimental)

Tecnologia assistiva experimental: câmera + detecção de objetos + avisos de áudio em português. **Não substitui bengala, cão-guia, treinamento de orientação e mobilidade nem medidas de segurança.** Ausência de detecção nunca significa caminho livre.

## Executar
Abra `index.html` por `https` ou `localhost` (a câmera exige contexto seguro) e use o navegador com internet na 1ª vez (modelo baixado do CDN). Exemplo: `python3 -m http.server 8000` na pasta e acesse `http://localhost:8000`.

## Testes (Node ≥ 18, sem dependências)
`npm test` (ou `node --test visioindustria.test.js avaliacao/avaliacao.test.js`). Os testes são **simulados**: validam a lógica, não a precisão do modelo.

## Diagnóstico
No `index.html`, abra **Diagnóstico**: caixas com estado e motivo, tempo de inferência, idade dos dados, registro de metadados (só com consentimento; nunca imagens), marcação de falso positivo/negativo e exportação JSON/CSV. API: `VisioIndustria.configurar({...})`, `configuracao()`, `exportarDiagnostico()`.

## Avaliação com imagens reais
Ver `docs/TREINAMENTO.md` e `avaliacao/avaliar.js`. Documentos: `docs/DIAGNOSTICO.md` (auditoria e limitações), `docs/VALIDACAO_MANUAL.md`.
