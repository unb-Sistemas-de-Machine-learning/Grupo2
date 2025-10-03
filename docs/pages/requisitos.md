### **Requisitos Funcionais (RF)**

Os requisitos funcionais descrevem **o que o sistema deve fazer**, ou seja, suas funcionalidades e comportamentos específicos.

- **RF01: Conexão com a Plataforma Telegram**: O sistema deve se integrar com a API do Telegram para receber mensagens de usuários e enviar respostas.

- **RF02: Processamento de Linguagem Natural (PLN)**: O sistema deve ser capaz de receber e interpretar perguntas escritas em linguagem natural em português do Brasil.

- **RF03: Geração de Respostas com RAG (Retrieval-Augmented Generation)**: O sistema deve gerar respostas baseando-se em um contexto extraído de uma base de conhecimento vetorial, garantindo que as informações sejam fiéis aos documentos de origem.

- **RF04: Citação de Fontes**: Para cada resposta fornecida, o sistema deve incluir uma referência ou link direto para o(s) documento(s) oficial(is) de onde a informação foi extraída.

- **RF05: Coleta Automatizada de Dados (Web Scraping)**: O sistema deve possuir um agente autônomo capaz de varrer periodicamente os sites pré-definidos da UnB para coletar documentos e informações.

- **RF06: Extração de Conteúdo de Arquivos**: O sistema deve ser capaz de extrair texto de múltiplos formatos de arquivo, principalmente PDF (texto nativo) e DOCX.

- **RF07: Reconhecimento Óptico de Caracteres (OCR)**: O sistema deve conseguir extrair texto de documentos que são imagens ou PDFs escaneados, onde o texto não é selecionável.

- **RF08: Atualização da Base de Conhecimento**: O sistema deve ter um processo automatizado para segmentar, vetorizar e indexar novos conteúdos coletados, mantendo a base de conhecimento atualizada.

- **RF09: Tratamento de Perguntas Fora de Escopo**: Quando uma pergunta não puder ser respondida com as informações disponíveis, o sistema deve retornar uma mensagem clara e amigável informando que não encontrou a resposta.

- **RF10: Coleta de Feedback do Usuário**: O sistema deve apresentar ao usuário uma forma de avaliar a qualidade da resposta, como botões de "gostei" e "não gostei".

- **RF11: Comando de Ajuda e Boas-Vindas**: O sistema deve responder a um comando /start ou /ajuda com uma mensagem de boas-vindas que explique seu propósito e como utilizá-lo.

---

### **Requisitos Não Funcionais (RNF)**

Os requisitos não funcionais descrevem **como o sistema deve ser**, definindo suas qualidades, restrições e características de operação.

- **RNF01: Desempenho (Latência)**: O tempo de resposta para uma pergunta do usuário, desde o envio até o recebimento da resposta completa, não deve exceder 15 segundos em 90% das requisições.

- **RNF02: Disponibilidade**: O serviço do chatbot deve estar disponível para os usuários 99,5% do tempo, excluindo janelas de manutenção planejadas.

- **RNF03: Confiabilidade (Fidelidade da Resposta)**: As respostas geradas pelo sistema devem ser estritamente baseadas no conteúdo dos documentos oficiais recuperados. O sistema não deve "alucinar" ou inventar informações.

- **RNF04: Usabilidade**: A linguagem utilizada nas respostas do bot deve ser clara, objetiva e de fácil compreensão para o público-alvo (estudantes), evitando jargões excessivamente técnicos ou burocráticos.

- **RNF05: Segurança**: Toda a comunicação e dados armazenados devem seguir as melhores práticas de segurança. Nenhuma informação pessoal sensível dos usuários deve ser solicitada ou armazenada.

- **RNF06: Privacidade**: O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados (LGPD). Os logs de conversas, se armazenados para análise, devem ser anonimizados.

- **RNF07: Escalabilidade**: A arquitetura do sistema deve ser capaz de suportar um aumento de 10x no número de usuários simultâneos e no volume da base de documentos sem a necessidade de uma reengenharia completa.

- **RNF08: Manutenibilidade**: O processo para adicionar um novo site da UnB como fonte de dados deve ser simples e bem documentado, não exigindo mais do que algumas horas de trabalho de um desenvolvedor.

- **RNF09: Compatibilidade**: O chatbot deve funcionar corretamente nas versões mais recentes dos clientes oficiais do Telegram para Desktop, Web, Android e iOS.

- **RNF10: Eficiência de Recursos**: O sistema deve ser otimizado para minimizar custos, especialmente no que tange ao número de chamadas para as APIs de modelos de linguagem (LLM) e ao uso de recursos de computação em nuvem.

- **RNF11: Ética no Scraping**: O agente de coleta de dados deve respeitar as diretivas dos sites da UnB e operar de forma a não sobrecarregar ou prejudicar a performance dos servidores da universidade.

---

<center>

## Histórico de Versão

</center>

<div style="margin: 0 auto; width: fit-content;">

| Data       | Versão | Descrição            | Autores                                   |
|------------|--------|----------------------|-------------------------------------------|
| 24/09/2025 | `1.0`  | Criação do documento | [Cássio Reis](https://github.com/csreis72) |

</div>

---