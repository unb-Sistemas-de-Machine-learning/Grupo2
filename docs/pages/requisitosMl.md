### **Introdução**

Este documento detalha os requisitos técnicos e de qualidade para o motor de Inteligência Artificial (IA) que constitui o núcleo do Assistente Virtual. Diferente dos requisitos de produto, o foco aqui é o ciclo de vida dos dados e o comportamento do modelo de Machine Learning. Os requisitos a seguir especificam como os dados devem ser coletados, processados e transformados em conhecimento, além de definir os critérios de performance, confiabilidade e auditabilidade para a geração de respostas. O objetivo é garantir que o "cérebro" do sistema seja preciso, eficiente e fiel às fontes de informação.

#### **Requisitos Funcionais (RF)**

* **RF09: Processamento de Linguagem Natural (PLN)**: O sistema deve ser capaz de interpretar a intenção e as entidades principais em perguntas escritas em português.

* **RF10: Geração de Respostas com RAG**: O sistema deve gerar respostas baseando-se em um contexto extraído de uma base de conhecimento vetorial.
* **RF11: Coleta Automatizada de Dados (Web Scraping)**: O sistema deve possuir um agente autônomo capaz de varrer periodicamente os sites pré-definidos.
* **RF12: Extração de Conteúdo de Arquivos**: O sistema deve ser capaz de extrair texto de múltiplos formatos de arquivo (PDF, DOCX).
* **RF13: Reconhecimento Óptico de Caracteres (OCR)**: O sistema deve conseguir extrair texto de documentos que são imagens ou PDFs escaneados.
* **RF14: Atualização da Base de Conhecimento**: O sistema deve ter um processo automatizado para segmentar, vetorizar e indexar novos conteúdos.
* **RF15: Logging de Inferência**: Para cada resposta gerada, o sistema deve registrar (em log) a pergunta original, os trechos de contexto recuperados e a resposta final para fins de auditoria e depuração.
* **RF16: Estratégias de Chunking Configuráveis**: O sistema deve permitir a configuração de diferentes estratégias de segmentação de texto (ex: por parágrafo, por tamanho fixo com sobreposição).
* **RF17: Blacklist de Fontes**: O sistema deve permitir que um administrador configure uma lista de URLs ou documentos que devem ser ignorados pelo processo de coleta de dados.
* **RF18: Detecção de Duplicatas**: O pipeline de processamento de dados deve ser capaz de identificar e descartar documentos duplicados para manter a base de conhecimento limpa.
* **RF20: Guard Rail**: O sistema deve ser capaz de identificar perguntas fora do escopo ao qual foi definido e retornar uma mensagem avisando que não pode responder a pergunta.


#### **Requisitos Não Funcionais (RNF)**

* **RNF10: Confiabilidade (Fidelidade da Resposta)**: As respostas geradas devem ser estritamente baseadas no conteúdo recuperado, com um índice de alucinação próximo de zero, a ser validado por testes.

* **RNF11: Eficiência de Recursos**: O sistema deve otimizar o número e o tamanho das chamadas às APIs de LLM para controlar os custos operacionais.
* **RNF12: Ética no Scraping**: O agente de coleta de dados deve operar de forma a não sobrecarregar os servidores da universidade.
* **RNF13: Auditabilidade**: Deve ser possível rastrear uma resposta gerada até os "chunks" de texto específicos que foram usados como contexto para sua criação.
* **RNF14: Atualidade dos Dados (Freshness)**: A informação na base de conhecimento não deve ter mais de 7 dias de defasagem em relação às fontes de dados online.
* **RNF15: Reprodutibilidade do Pipeline**: O pipeline de processamento de dados deve ser determinístico; o mesmo documento de entrada deve sempre gerar os mesmos vetores de saída.
* **RNF16: Robustez a Ruído**: O processo de extração de texto deve ser robusto a pequenas falhas de formatação nos documentos de origem (ex: quebras de linha indevidas, cabeçalhos e rodapés).

---

<center>

## Histórico de Versão

</center>

<div style="margin: 0 auto; width: fit-content;">

| Data       | Versão | Descrição            | Autores                                   |
|------------|--------|----------------------|-------------------------------------------|
| 07/10/2025 | `1.0`  | Criação do documento | [Vinicius Santos](https://github.com/ViniciussdeOliveira) |

</div>

---