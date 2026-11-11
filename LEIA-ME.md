# ENADE Computação – Banco de Questões e Simulado

## Como usar
- Abra `index.html` no navegador (precisa de internet só para Tailwind, Font Awesome e a fonte Inter).
- Mantenha as pastas `provas/` e `gabaritos/` ao lado do `index.html`: cada questão tem um link para a página do caderno original.
- Para publicar: GitHub Pages / Netlify / Vercel (é só subir a pasta inteira).
- `questoes.json` é o mesmo banco que está embutido no HTML (campos: id, ano, curso, componente, numero, assunto, tipo, enunciado, opcoes, correta, anulada, gabarito_oficial, explicacao, padrao_resposta, figura, opcoes_na_imagem, transcricao_ocr, fonte{prova,pagina}).

## O que tem
- 210 itens: 188 objetivas + 22 discursivas, das provas 2011, 2014, 2017, 2019 e 2023 (Formação Geral + Componente Específico).
- 23 assuntos (programação, POO/padrões, linguagens/compiladores, ED, TC, BD, ES, redes, SO, arquitetura, digitais, embarcados, eletrônica, sinais/controle, IA, segurança, sistemas distribuídos, grafos/PO, computação gráfica/IHC, matemática/física, materiais/ambiente/gestão, ética/legislação e Formação Geral).
- Gabaritos: definitivos do INEP para 2014, 2017, 2019 e 2023 (PDFs em `gabaritos/`). 4 questões anuladas. 2011: sem gabarito oficial nos arquivos; 12 questões têm resolução própria (marcadas) e as demais ficam sem gabarito.
- Da prova de 2011 foram deixadas de fora as questões 31 a 35 (Licenciatura em Computação, conteúdo pedagógico).

## Limitações conhecidas
- 2014 e 2017 são PDFs com fonte corrompida: o texto vem de OCR. 37 questões têm as alternativas só em figura (aparecem como "Alternativa A–E" + link para a página).
- Fórmulas, circuitos e gráficos não foram transcritos: as questões marcadas "Depende de figura" exigem abrir o caderno.
- Explicações comentadas: 35 questões (foco em programação/CS). As demais mostram só o gabarito.
- Discursivas: resumo do padrão INEP só para 2014 (D3–D5) e 2017 (D3–D5).

## Sugestões de melhoria
1. Recortar cada figura do PDF e embutir na questão (hoje é só link para a página).
2. MathJax/KaTeX para fórmulas e highlight.js/Prism para código (e preservar indentação de Python).
3. Completar gabarito de 2011 (INEP) e escrever explicações para as demais questões.
4. Autoavaliação das discursivas (checklist do padrão de resposta + nota).
5. Revisão espaçada: reaparecer as questões erradas após 1, 3 e 7 dias.
6. Atalhos de teclado (1–5 marca alternativa, setas navegam) e modo escuro.
7. Layout mobile com filtros em gaveta; PWA para funcionar offline.
8. Mapear cada questão ao conteúdo programático das diretrizes do INEP e acompanhar a cobertura.
9. Separar dados em `questoes.json` carregado por fetch + teste automático de integridade (ids únicos, 5 alternativas, gabarito válido).
10. Sincronizar progresso entre dispositivos (Supabase/Firebase) se quiser conta de usuário.
11. Incluir novas edições (2021 não teve a área; acompanhar as próximas).
12. Manter a fonte (INEP/MEC) citada no rodapé e usar o site só para estudo.
