## 1. Introdução

Este documento detalha as Histórias de Usuário (User Stories) que guiarão o desenvolvimento do Produto Mínimo Viável (MVP) do Assistente Virtual. As histórias estão escritas sob a perspectiva dos usuários finais e descrevem funcionalidades que entregam valor direto.

Cada história segue o formato:
**Como um** `<tipo de usuário>`, **eu quero** `<fazer uma ação>` **para que** `<eu possa alcançar um objetivo>`.

Para garantir a clareza, cada história é acompanhada de Critérios de Aceitação, que definem as condições para que a funcionalidade seja considerada "concluída".

## 2. Personas (Tipos de Usuário)

* **Aluno da FCTE:** O principal usuário do sistema. Busca informações acadêmicas e administrativas de forma rápida e confiável para progredir em seu curso.
* **Professor/Pesquisador da FCTE:** Utiliza o sistema para consultar regulamentos, normas e procedimentos, tanto para suas próprias atividades quanto para orientar alunos.
* **Mantenedor do Sistema:** O desenvolvedor ou equipe técnica responsável por garantir que o sistema funcione corretamente e que sua base de conhecimento esteja atualizada.

## 3. Épicos e Histórias de Usuário

As histórias estão agrupadas em Épicos, que representam grandes áreas de funcionalidade do produto.

---

### **Épico 1: Interação Básica e Experiência do Usuário**

*Este épico cobre a interface fundamental e as interações que garantem uma experiência de uso clara e útil.*

**US01: Primeira Interação com o Bot**
* **Como um** aluno novo, **eu quero** receber uma mensagem de boas-vindas e instruções claras ao iniciar o chat, **para que** eu entenda imediatamente o propósito do bot e como fazer uma pergunta.
* **Critérios de Aceitação:**
    1.  Ao clicar em "Começar" (/start) no Telegram, uma mensagem de boas-vindas é exibida.
    2.  A mensagem explica que o bot responde a perguntas sobre documentos da FCTE.
    3.  A mensagem inclui pelo menos um exemplo de pergunta.

**US02: Tratamento de Perguntas Fora de Escopo**
* **Como um** usuário, **eu quero** ser informado de maneira amigável quando o bot não encontrar uma resposta, **para que** eu não fique frustrado e saiba que preciso procurar a informação em outro canal.
* **Critérios de Aceitação:**
    1.  Se o sistema não encontrar trechos relevantes na base de conhecimento, ele não deve inventar uma resposta.
    2.  Uma mensagem padrão, como "Desculpe, não consegui encontrar uma resposta para sua pergunta nos documentos da FCTE", é enviada ao usuário.
    3.  Se a pergunta ultrapassar o guard rail, deve ser exibida uma mensagem explicando o motivo de não poder responder.

**US03: Coleta de Feedback Imediato**
* **Como um** aluno, **eu quero** poder avaliar cada resposta com um "gostei" ou "não gostei", **para que** eu possa ajudar a melhorar a precisão do sistema.
* **Critérios de Aceitação:**
    1.  Abaixo de cada resposta gerada, são exibidos dois botões interativos "gostei" e "não gostei".
    2.  Ao clicar em um dos botões, o feedback é registrado no sistema para análise posterior.
    3.  O botão clicado pode ser visualmente atualizado para indicar que o feedback foi recebido.

---

### **Épico 2: Consulta Inteligente de Informações (Core RAG)**

*Este épico descreve a funcionalidade central do produto: responder perguntas com base nos documentos da FCTE.*

**US04: Realizar uma Pergunta Específica**
* **Como um** aluno da FCTE, **eu quero** perguntar sobre as regras de Atividades Complementares do meu curso, **para que** eu possa planejar minhas atividades e garantir os créditos necessários.
* **Critérios de Aceitação:**
    1.  O usuário pode enviar uma pergunta em texto livre.
    2.  O sistema identifica a intenção e busca na base de dados por informações relevantes.
    3.  A resposta gerada é coesa, em linguagem natural, e baseada no conteúdo do(s) documento(s) encontrado(s).

**US05: Verificação da Fonte da Informação**
* **Como um** professor, **eu quero** que toda resposta inclua um link para o documento oficial de origem, **para que** eu possa auditar a informação e ter 100% de confiança na resposta antes de passá-la a um orientado.
* **Critérios de Aceitação:**
    1.  Ao final de cada resposta, uma seção "Fonte(s)" é exibida.
    2.  Esta seção contém um ou mais links clicáveis que levam diretamente aos documentos PDF ou páginas web utilizadas para gerar a resposta.

**US06: Busca de Informações em Documentos Escaneados**
* **Como um** aluno de pós-graduação, **eu quero** perguntar sobre uma resolução antiga que só está disponível como PDF escaneado, **para que** eu tenha acesso a regras que não estão em formato de texto pesquisável.
* **Critérios de Aceitação:**
    1.  O sistema deve ser capaz de processar arquivos PDF baseados em imagem.
    2.  O conteúdo textual destes arquivos é extraído via OCR e indexado na base de conhecimento.
    3.  As buscas conseguem retornar resultados baseados nesses documentos.

---

### **Épico 3: Coleta e Manutenção da Base de Conhecimento**

*Estas histórias são focadas no "Mantenedor do Sistema" e garantem que a inteligência do bot seja alimentada e mantida.*

**US07: Carga Inicial de Documentos**
* **Como um** mantenedor do sistema, **eu quero** que um agente de software (scraper) colete todos os documentos relevantes dos sites da FCTE, **para que** a base de conhecimento inicial do chatbot seja criada.
* **Critérios de Aceitação:**
    1.  O agente acessa uma lista pré-definida de URLs da FCTE.
    2.  Ele identifica e baixa arquivos (PDF, DOCX) e o conteúdo de páginas HTML.
    3.  Os arquivos coletados são armazenados em um local para processamento.

**US08: Processamento e Indexação de Conteúdo**
* **Como um** mantenedor do sistema, **eu quero** que os documentos coletados sejam processados automaticamente, **para que** as informações contidas neles se tornem pesquisáveis pelo sistema de RAG.
* **Critérios de Aceitação:**
    1.  O texto é extraído de cada documento.
    2.  O texto é limpo e segmentado em "chunks".
    3.  Cada chunk é convertido em um vetor (embedding) e armazenado no banco de dados vetorial com seus metadados.

**US09: Atualização Automática e Periódica**
* **Como um** mantenedor do sistema, **eu quero** que o processo de coleta e atualização da base de conhecimento seja executado automaticamente em um cronograma definido (ex: diariamente), **para que** o chatbot sempre tenha as informações mais recentes sem intervenção manual.
* **Critérios de Aceitação:**
    1.  O pipeline completo (coleta e processamento) é executado sem necessidade de gatilho manual.
    2.  O sistema consegue identificar documentos novos ou atualizados e os adiciona à base de conhecimento.
    3.  Um log de execução é gerado ao final de cada ciclo automático.

## Histórico de Versão

</center>

<div style="margin: 0 auto; width: fit-content;">

| Data       | Versão | Descrição            | Autores                                   |
|------------|--------|----------------------|-------------------------------------------|
| 07/10/2025 | `1.0`  | Criação do documento | [Vinicius Santos](https://github.com/ViniciussdeOliveira) |

</div>