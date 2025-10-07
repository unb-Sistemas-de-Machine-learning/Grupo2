## 1. Introdução

Este documento tem como objetivo apresentar e detalhar os artefatos criados durante a fase inicial de concepção do projeto do Assistente Virtual para a FCTE-UnB. Esta etapa foi fundamental para transformar uma necessidade abstrata em um plano de projeto estruturado, com escopo, requisitos e tecnologias bem definidos.

## 2. Framework e Ferramentas Utilizadas

A metodologia de concepção foi apoiada pelo framework **PIM-Go (Product Integration Model)**, que oferece modelos e templates para guiar o processo de design de produto. Adicionalmente, foi utilizada uma ferramenta externa para detalhar os aspectos de Machine Learning.

As ferramentas específicas foram:
* **Framework PIM-Go:**
    * Design Thinking - Causas
    * Design Thinking - Ideias
    * Parking Lot de Ideias 
    * Filtro de Ideias
* **Ferramenta OWNML:**
    * Machine Learning Canvas

## 3. Detalhamento dos Artefatos

### 3.1. Artefato 1: Design Thinking - Causas Canvas

* **Descrição da Ferramenta:** Um modelo visual inspirado no Diagrama de Ishikawa (Espinha de Peixe), utilizado para explorar em profundidade as causas-raiz de um problema central a partir da perspectiva do usuário.
* **Aplicação no Projeto:** Foi utilizado para desconstruir a dificuldade geral de "acesso à informação na UnB", identificando os fatores que contribuem para essa percepção.
* **Principais Insights e Resultados:**
    * O problema central foi refinado para: **"Alto esforço para obter informações confiáveis"**.
    * As causas-raiz foram agrupadas em quatro categorias principais:
        1.  **Gestão da Informação:** Documentação espalhada e deprecada.
        2.  **Qualidade do Conteúdo:** Linguagem complexa e falta de padronização.
        3.  **Acessibilidade e UX:** Links quebrados e mecanismos de busca ineficientes.
        4.  **Processos Institucionais:** Demora no atendimento tradicional e burocracia.

<center>

**Figura 1**: Causes Canvas

</center>

<center>
    <img src="assets/DESIGN_THINKING_CAUSES_CANVAS.png" alt="Causes Canvas" style="width:100%; max-width: 800px;"/>
</center>

<center>

**Fonte**: Santos, Reis, Carvalho, Ginuino (2025).

</center>

### 3.2. Artefato 2: Design Thinking - Ideias Canvas

* **Descrição da Ferramenta:** Um canvas focado na ideação da solução, estruturando o conceito central do produto e suas principais funcionalidades ou capacidades.
* **Aplicação no Projeto:** Foi utilizado para traduzir o objetivo de "facilitar o acesso à documentação" em uma proposta de solução concreta.
* **Principais Insights e Resultados:**
    * A ideia central da solução foi definida como: **"Assistente de IA no Telegram para consulta inteligente de documentos da UnB"**.
    * As capacidades essenciais do sistema foram delineadas, incluindo: Interação via Chatbot, Coleta e Processamento de Dados (Agente de IA), Lógica de Recuperação da Informação (RAG) e Gerenciamento do Sistema.

<center>

**Figura 2**: Ideas Canvas

</center>

<center>
    <img src="assets/DESIGN_THINKING_ IDEAS_CANVAS.png" alt="Ideas Canvas" style="width:100%; max-width: 800px;"/>
</center>

<center>

**Fonte**: Santos, Reis, Carvalho, Ginuino (2025).

</center>

### 3.3. Artefato 3: Filtro de Ideias

* **Descrição da Ferramenta:** O Filtro de Ideias é uma matriz de priorização utilizada para classificar as ideias geradas com base em eixos como Relevância e Confiança, ajudando a equipe a decidir no que focar.
* **Aplicação no Projeto:** Foi utilizado para analisar as funcionalidades e componentes levantados no "Ideas Canvas", mapeando-os em quadrantes que indicam a estratégia a ser seguida (ex: implementar agora, pesquisar mais, descartar).
* **Principais Insights e Resultados:**
    * **Definição do MVP:** As ideias posicionadas no quadrante **"Sweet Spot"** (alta confiança, alta relevância) – `Agente de IA`, `Análise de Sites` e `Chat de Conversa` – foram validadas como o núcleo do Produto Mínimo Viável (MVP), pois representam a maior entrega de valor com menor risco.
    * **Mapeamento de Riscos Técnicos:** O `WebScraping` e a `Busca em Imagens` foram identificados como "Riscos Valiosos". Isso indica que, embora sejam muito relevantes para o projeto, eles apresentam desafios técnicos ou incertezas que exigirão mais pesquisa e planejamento para serem implementados com sucesso.
    * **Identificação de Componentes de Suporte:** Funcionalidades como `RAG` e `Criação de API` foram classificadas como "Business as Usual", demonstrando que são vistas como tecnologias de base ou componentes padrão necessários para a entrega do valor principal, e não como as funcionalidades de destaque do produto final.
    * **Visão de Futuro:** A `Autenticação` foi classificada como uma funcionalidade de baixa relevância para o momento inicial, validando a decisão de mantê-la fora do escopo do MVP, mas registrando-a como uma possibilidade futura.

<center>

**Figura 3**: Idea Filter Canvas

</center>

<center>
    <img src="assets/DESIGN_ THINKING_IDEA_FILTER_CANVAS.png" alt="Idea Filter Canvas" style="width:100%; max-width: 800px;"/>
</center>

<center>

**Fonte**: Santos, Reis, Carvalho, Ginuino (2025).

</center>

### 3.4. Artefato 4: Parking Lot

* **Descrição da Ferramenta:** Uma técnica de brainstorming para capturar todas as ideias relacionadas ao projeto em um único local, antes de qualquer filtro ou priorização.
* **Aplicação no Projeto:** O artefato **"Design Thinking - Ideas Canvas"** serviu como o Parking Lot do projeto. Ele funcionou como o repositório central para todas as funcionalidades, componentes e conceitos que formam a visão completa da solução.
* **Principais Insights e Resultados:**
    * **Visão Arquitetural:** O canvas consolidou uma visão de alto nível da arquitetura do sistema, listando todos os componentes necessários, desde a coleta de dados (`WebScraping`, `Análise de sites`) até o processamento (`Agente de IA`, `RAG`) e a entrega ao usuário (`Chat`, `API`).
    * **Escopo Abrangente:** Serviu para registrar tanto as ideias essenciais para o MVP quanto as visões de longo prazo, como a `Autenticação (matrícula)`, que sugere uma futura personalização da experiência do usuário.
    * **Base para Priorização:** O conjunto de ideias capturadas neste canvas foi o insumo direto para a atividade do "Filtro de Ideias", permitindo que a equipe tivesse uma visão completa antes de tomar decisões estratégicas sobre o foco do desenvolvimento.

<center>

**Figura 4**: Parking Lot of Ideas Canvas

</center>

<center>
    <img src="assets/PARKING_LOT_OF_ IDEAS_CANVAS.png" alt="Parking Lot of Ideas Canvas" style="width:100%; max-width: 800px;"/>
</center>

<center>

**Fonte**: Santos, Reis, Carvalho, Ginuino (2025).

</center>

### 3.5. Artefato 5: Machine Learning Canvas

* **Descrição da Ferramenta:** Um canvas estratégico que estrutura um projeto sob a ótica de Machine Learning. Ele força a reflexão sobre a proposta de valor, os dados, as features, a modelagem e a avaliação do sistema de IA.
* **Aplicação no Projeto:** Foi utilizado para detalhar os aspectos técnicos e de negócio do núcleo de IA do chatbot, adaptando os conceitos para um sistema baseado em RAG.
* **Principais Insights e Resultados:**
    * **Validação da Proposta de Valor:** O canvas conectou claramente a tecnologia de IA (`Geração de respostas com RAG`) ao benefício final do usuário (`reduz o tempo e esforço`), validando o porquê de se usar ML no projeto.
    * **Identificação do Risco Crítico:** A seção "Impact Simulation" destacou que **"Alucinações e gerações de dados falsos são inaceitáveis"**, pois podem levar à perda de prazos pelos alunos. Isso solidificou a **confiabilidade** como o requisito não funcional mais importante do sistema de IA.
    * **Clareza sobre o Processo RAG:** As seções "Features" e "Building Models" demonstraram um entendimento claro do fluxo técnico do RAG: o texto é extraído, dividido em "chunks" e transformado em embeddings vetoriais, e o "modelo" de produção é a combinação do banco de dados vetorial com um LLM.
    * **Estratégia de Monitoramento Focada no Usuário:** A definição das métricas de monitoramento (`Feedback do usuário`, `Número de usuários ativos`, `Engajamento`) revelou um foco em medir o sucesso do produto pelo valor gerado para o usuário, e não apenas por métricas técnicas offline.

<center>

**Figura 5**: ML Canvas

</center>

<center>
    <img src="assets/ML_CANVAS.png" alt="ML Canva" style="width:100%; max-width: 800px;"/>
</center>

<center>

**Fonte**: Santos, Reis, Carvalho, Ginuino (2025).

</center>

## 4. Conclusão

A utilização sistemática destes artefatos permitiu uma transição clara e bem documentada da fase de problema para a de solução. O processo resultou em uma compreensão profunda das necessidades do usuário, um escopo de projeto bem definido (piloto na FCTE), requisitos detalhados e um plano claro para o desenvolvimento técnico do sistema de IA. Esta base sólida é essencial para guiar os próximos passos na construção do MVP.

