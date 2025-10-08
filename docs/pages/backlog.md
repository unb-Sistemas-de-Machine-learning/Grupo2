## 1. Introdução

Este documento constitui o Product Backlog para o desenvolvimento do Produto Mínimo Viável (MVP) do Assistente Virtual. Ele é um artefato vivo que lista, descreve e prioriza todo o trabalho a ser realizado pela equipe de desenvolvimento.

O backlog foi construído a partir dos documentos de Histórias de Usuário e Requisitos (Produto e ML), garantindo que cada item de trabalho esteja vinculado a uma necessidade de usuário e a critérios técnicos claros.

## 2. Metodologia de Priorização

A priorização dos itens de backlog seguirá o método **MoSCoW**, para definir o que é crítico para o sucesso do MVP:

  * **M (Must-have):** Essencial. O MVP não pode ser lançado sem este item.
  * **S (Should-have):** Importante, mas não vital para o lançamento. Se não for incluído, haverá um impacto notável, mas o produto ainda funciona.
  * **C (Could-have):** Desejável, mas menos importante. Pequeno impacto se for deixado de fora.
  * **W (Won't-have this time):** Não será incluído nesta versão do produto, mas pode ser considerado para o futuro.

## 3. Épicos

As funcionalidades foram agrupadas nos seguintes épicos:

  * **Épico 1:** Interação Básica e Experiência do Usuário
  * **Épico 2:** Consulta Inteligente de Informações (Core RAG)
  * **Épico 3:** Coleta e Manutenção da Base de Conhecimento
  * **Épico 4:** Funcionalidades de Personalização

## 4. Backlog Detalhado

-----

### **Épico 1: Interação Básica e Experiência do Usuário**

| ID | Título | História de Usuário | Requisitos Vinculados | Critérios de Aceitação | Prioridade |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **US01** | **Primeira Interação com o Bot** | Como um aluno novo, eu quero receber uma mensagem de boas-vindas e instruções claras ao iniciar o chat, para que eu entenda imediatamente o propósito do bot e como fazer uma pergunta. | RF01, RF05 | 1. Ao clicar em "Começar" (/start) ou enviar "/ajuda", uma mensagem de boas-vindas é exibida. <br>2. A mensagem explica o escopo (FCTE) e inclui um exemplo de pergunta. | **Must-have** |
| **US02** | **Tratamento de Perguntas Fora de Escopo** | Como um usuário, eu quero ser informado de maneira amigável quando o bot não encontrar uma resposta, para que eu não fique frustrado e saiba que preciso procurar a informação em outro canal. | RF03, RF20 | 1. Se a busca RAG não retornar resultados, uma mensagem padrão de "não encontrei a resposta" é enviada. <br>2. Se a pergunta acionar o Guard Rail (ex: tema ofensivo, perigoso ou sensível), uma mensagem explicando que não pode responder sobre aquele tópico é exibida. | **Must-have** |
| **US03** | **Coleta de Feedback Imediato** | Como um aluno, eu quero poder avaliar cada resposta com um "gostei" ou "não gostei", para que eu possa ajudar a melhorar a precisão do sistema. | RF04 | 1. Abaixo de cada resposta, botões interativos "gostei" e "não gostei" são exibidos. <br>2. O clique é registrado no sistema para análise. | **Must-have** |
| **US10** | **Acesso a Perguntas Frequentes (FAQ)** | Como um usuário, eu quero ter acesso a uma lista de perguntas frequentes, para que eu possa rapidamente encontrar respostas para as dúvidas mais comuns sem precisar digitá-las. | RF06 | 1. Um comando (ex: `/faq`) ou um botão no menu inicial exibe uma lista de 3-5 perguntas pré-definidas. <br>2. Clicar em uma pergunta da lista a envia para o bot como se o usuário a tivesse digitado. | **Should-have** |

-----

### **Épico 2: Consulta Inteligente de Informações (Core RAG)**

| ID | Título | História de Usuário | Requisitos Vinculados | Critérios de Aceitação | Prioridade |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **US04** | **Realizar uma Pergunta Específica** | Como um aluno da FCTE, eu quero perguntar sobre as regras de Atividades Complementares do meu curso, para que eu possa planejar minhas atividades e garantir os créditos necessários. | RF09, RF10, RNF10 | 1. O usuário envia uma pergunta em texto livre. <br>2. O sistema interpreta a pergunta, busca na base de conhecimento e gera uma resposta coesa e em linguagem natural. | **Must-have** |
| **US05** | **Verificação da Fonte da Informação** | Como um professor, eu quero que toda resposta inclua um link para o documento oficial de origem, para que eu possa auditar a informação e ter 100% de confiança na resposta. | RF02, RNF13 | 1. Ao final de cada resposta, uma seção "Fonte(s)" é exibida. <br>2. A seção contém links clicáveis para os documentos/páginas web de origem. | **Must-have** |
| **US06** | **Busca em Documentos Escaneados (OCR)** | Como um aluno de pós-graduação, eu quero perguntar sobre uma resolução antiga que só está disponível como PDF escaneado, para que eu tenha acesso a regras que não estão em formato de texto pesquisável. | RF12, RF13, RNF16 | 1. O pipeline de dados processa arquivos PDF baseados em imagem usando OCR. <br>2. O texto extraído é indexado e se torna pesquisável pelo sistema RAG. | **Must-have** |

-----

### **Épico 3: Coleta e Manutenção da Base de Conhecimento**

| ID | Título | História de Usuário | Requisitos Vinculados | Critérios de Aceitação | Prioridade |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **US07** | **Carga Inicial de Documentos** | Como um mantenedor do sistema, eu quero que um agente de software (scraper) colete todos os documentos relevantes dos sites da FCTE, para que a base de conhecimento inicial do chatbot seja criada. | RF11, RF17, RNF12 | 1. O agente acessa uma lista pré-definida de URLs da FCTE. <br>2. Ele baixa os arquivos e conteúdos HTML e os armazena para processamento. | **Must-have** |
| **US08** | **Processamento e Indexação de Conteúdo** | Como um mantenedor do sistema, eu quero que os documentos coletados sejam processados automaticamente, para que as informações contidas neles se tornem pesquisáveis pelo sistema de RAG. | RF15, RF16, RF18, RNF15 | 1. O texto é extraído, limpo e segmentado em "chunks". <br>2. Cada chunk é convertido em um vetor e armazenado no banco de dados vetorial com seus metadados. | **Must-have** |
| **US09** | **Atualização Automática e Periódica** | Como um mantenedor do sistema, eu quero que o processo de coleta e atualização da base de dados rode automaticamente em um cronograma definido, para que o chatbot sempre tenha as informações mais recentes. | RF14, RNF14 | 1. O pipeline completo é executado sem gatilho manual (ex: diariamente). <br>2. O sistema identifica e processa documentos novos/atualizados. <br>3. Um log de execução é gerado. | **Must-have** |

-----

### **Épico 4: Funcionalidades de Personalização**

| ID | Título | História de Usuário | Requisitos Vinculados | Critérios de Aceitação | Prioridade |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **US11** | **Autenticação de Usuário** | Como um aluno da FCTE, eu quero poder me identificar com minha matrícula, para que eu possa futuramente receber informações personalizadas sobre meu curso ou minhas pendências. | RF19, RNF04 | 1. O bot oferece um comando `/login`. <br>2. O usuário insere sua matrícula. <br>3. O sistema valida a matrícula (simulação inicial, sem integração real). <br>4. O bot cumprimenta o usuário pelo nome (simulado). | **Should-have** |

---

<center>

## Histórico de Versão

</center>

<div style="margin: 0 auto; width: fit-content;">

| Data       | Versão | Descrição            | Autores                                   |
|------------|--------|----------------------|-------------------------------------------|
| 08/10/2025 | `1.0`  | Criação do documento | [Vinicius Santos](https://github.com/ViniciussdeOliveira) |

</div>

---