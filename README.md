# Simulado ETEC 2027

Single Page Application (SPA) desenvolvida em Vanilla JavaScript para preparação de vestibulandos da ETEC. O projeto combina banco de questões próprio, controle de estado local e persistência de dados no navegador.

> **Deploy:** [Insira o link do GitHub Pages ou Netlify aqui]

---

## Funcionalidades

- **Simulado Geral (90 questões):** Seleção randômica de itens cobrindo toda a base curricular.
- **Treino Modular:** Filtros por disciplina (Linguagens, Exatas, Humanas e Biológicas) e níveis de dificuldade (Fácil, Médio e Difícil).
- **Embaralhamento Dinâmico:** Algoritmo de Fisher-Yates para reordenar alternativas a cada execução, evitando vício por posição.
- **Persistência de Sessão:** Uso de `localStorage` para salvar o progresso do simulado geral, permitindo pausar e retomar sem perda de respostas.
- **Relatório de Desempenho:** Cálculo de acertos/erros, tempo de resposta, gabarito com resolução comentada e filtro exclusivo para revisão de erros.

---

## Decisões Técnicas

- **Arquitetura SPA sem Frameworks:** A renderização das telas (Home, Perfil, Quiz e Resultado) é feita via manipulação direta do DOM (`innerHTML`) gerenciada por um objeto de estado global (`st`).
- **Zero Dependências:** Código puro (HTML5, CSS3 e ES6+), garantindo carregamento instantâneo sem necessidade de bundlers (Webpack/Vite) ou bibliotecas externas.
- **Armazenamento no Client-side:** Dados de resposta mantidos isolados na Web Storage API do navegador do usuário, garantindo privacidade e execução offline.

---

## Estrutura do Projeto

```text
├── index.html       # Estrutura HTML, estilos e lógica de execução
├── perfil.jpg       # Assets visuais da interface
└── *.png            # Ícones das disciplinas
