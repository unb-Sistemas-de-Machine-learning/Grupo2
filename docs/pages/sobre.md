# **Sobre**

Nesse primeiro módulo o foco do projeto está nas definições básicas de tecnologia, requisitos, modelos e escopo.

Para a realização de cada tema, foram utilizados Brainstorming, técnicas de elicitação e priorização de requisitos para construir uma base sólida para as próximas fases de desenvolvimento. As seções a seguir detalham as principais decisões e artefatos gerados nesta etapa inicial.

## **1. Objetivo do Projeto**

Desenvolver um assistente virtual inteligente, via Telegram, para a comunidade acadêmica da Universidade de Brasília (UnB). O objetivo é centralizar e simplificar o acesso a informações contidas em documentos oficiais, resoluções e páginas da web da instituição, fornecendo respostas rápidas e confiáveis em linguagem natural.

## **2. O Problema**

A comunidade acadêmica enfrenta um **alto esforço para obter informações confiáveis** sobre os procedimentos e regulamentos da UnB. A documentação oficial é complexa, descentralizada e, muitas vezes, de difícil acesso, resultando em perda de tempo, frustração e risco de desinformação.

## **3. Solução Proposta**

A solução consiste em um **Chatbot baseado no padrão RAG (Retrieval-Augmented Generation)**. Um agente de Inteligência Artificial será responsável por coletar e processar continuamente os documentos de fontes oficiais da UnB. As informações serão indexadas em uma base de conhecimento vetorial, permitindo que o chatbot encontre os trechos mais relevantes para a pergunta de um usuário e utilize um Modelo de Linguagem Grande (LLM) para gerar uma resposta coesa, precisa e com a citação das fontes originais.

## **4. Escopo do Módulo 1**

Para garantir um desenvolvimento focado e iterativo, o escopo deste módulo inicial está definido como:

### **Escopo do Projeto:**
Para garantir a viabilidade, a qualidade dos dados e a entrega de valor de forma ágil, a fase inicial do projeto será implementada como um piloto focado exclusivamente no âmbito da Faculdade de Ciências e Tecnologias em Engenharia (FCTE).

Esta abordagem permite criar uma base de conhecimento altamente relevante e precisa para um público-alvo bem definido, servindo como um modelo validado para futuras expansões para outras unidades da UnB.

#### **Dentro do Escopo:**
* Definição da arquitetura de referência (RAG + Agente de Coleta).
* Mapeamento das principais fontes de dados (portais SAA, DEG, etc.).
* Levantamento dos requisitos funcionais e não funcionais essenciais (MVP).
* Seleção e recomendação de modelos de LLM e bancos de dados vetoriais.
* Criação dos artefatos de design do produto (ML Canvas, Design Thinking Canvas).
* Desenvolvimento de uma Prova de Conceito (PoC) do fluxo principal.

#### **Fora do Escopo:**
* Integração com outras plataformas além do Telegram (ex: WhatsApp).
* Um painel de administração (dashboard) completo.

## **5. Tecnologias Mapeadas**

* **Plataforma de Interação:** Telegram
* **Linguagem de Programação:** Python
* **Arquitetura de IA:** RAG (Retrieval-Augmented Generation)
* **Modelos de LLM:** A ser decidido...
* **Banco de Dados Vetorial:** A ser decidido...
* **Infraestrutura (Cloud):** A ser decidido...

## **6. Metodologia e Ferramentas**

Para a concepção do projeto, foram aplicadas as seguintes ferramentas e frameworks de design de produto e engenharia de software:

* **Design Thinking Causes Canvas:** Para mapear o problema e suas causas-raiz.
* **Parking Lot of Ideas:** Para brainstorming de funcionalidades futuras.
* **The Machine Learning Canvas:** Para estruturar a solução sob a ótica de um produto de IA.
* **Levantamento de Requisitos:** Definição de Requisitos Funcionais e Não Funcionais para guiar o desenvolvimento.

## **7. Próximos Passos**

Com a conclusão deste módulo de concepção, o próximo passo é iniciar o **desenvolvimento do Produto Mínimo Viável (MVP)**. As atividades prioritárias incluem a configuração da infraestrutura, a implementação do agente de coleta de dados para as fontes prioritárias e o desenvolvimento do fluxo de conversação básico no Telegram.


## Histórico de Versão

<div style="margin: 0 auto; width: fit-content;">

| Data       | Versão | Descrição            | Autores                                   |
|------------|--------|----------------------|-------------------------------------------|
| 02/10/2025 | `1.0`  | Criação do documento | [Vinicius Santos](https://github.com/csreis72) |

</div>