<center>

# Banco de Dados Vetorial

</center>

---

#### Utilidade do Banco de Dados em Vetores

<div align="justify">

&emsp;&emsp;
TRALALA
</div>

---

#### O Que é o Qdrant?

<div align="justify">

&emsp;&emsp;
TRALALA
</div>

---

#### Embeddings: O Que São?

<div align="justify">

&emsp;&emsp;
TRALALA
</div>

---

#### Como Identificar Dados Próximos?

<div align="justify">

&emsp;&emsp;
TRALALA
</div>

---

#### Convertendo PDF em Vetor

<div align="justify">

&emsp;&emsp;
TRALALA
</div>

---

#### Transformando Dados Não Estruturados em Números

<div align="justify">

&emsp;&emsp;
TRALALA
</div>

---

#### Criando Prompts com Dados de Vetores

<div align="justify">

&emsp;&emsp;
Após a transformação dos textos em vetores, o sistema utiliza mecanismos de busca semântica para encontrar os documentos mais relevantes a partir de uma consulta do usuário. Essa etapa é conhecida como <strong>retrieval</strong>, e seu resultado consiste nos vetores mais similares à pergunta feita.

&emsp;&emsp;
Em seguida, os textos originais correspondentes a esses vetores são reunidos e integrados em um prompt contextual, que é enviado ao modelo de linguagem. Esse prompt combina a pergunta do usuário com os dados recuperados, permitindo que o modelo forneça uma resposta mais precisa e fundamentada nas informações encontradas.
</div>

Por exemplo:

````txt
Você é um assistente virtual especializado em fornecer informações acadêmicas sobre a Universidade de Brasília (UnB). Utilize os documentos oficiais da UnB para responder às perguntas dos usuários de forma clara e objetiva.
Pergunta do Usuário: "Quais são os requisitos para me inscrever em um curso de pós-graduação na UnB?"
Documentos Relevantes Recuperados:
1. "Para se inscrever em um curso de pós-graduação na UnB....
2. "Os requisitos incluem ter um diploma de graduação reconhecido..."
3. "Além disso, é necessário apresentar um projeto de pesquisa..."
````

Sendo assim, o fluxo de dados pode ser resumido na seguinte sequência:
1. O usuário faz uma pergunta.
2. O sistema converte a pergunta em um vetor.
3. O sistema busca no banco de dados os vetores mais próximos.
4. O sistema recupera os textos originais associados a esses vetores.
5. O sistema cria um prompt que inclui a pergunta do usuário e os textos recuperados.
6. O prompt é enviado ao modelo de linguagem para gerar uma resposta.

---

<center>

## Histórico de Versão

</center>

<div style="margin: 0 auto; width: fit-content;">

| Data       | Versão | Descrição            | Autores                                                   |
|------------|--------|----------------------|-----------------------------------------------------------|
| 06/10/2025 | `1.0`  | Criação do documento | [Pablo Serra](https://github.com/Pabloserrapxx), [João Ginuino](https://github.com/i-JSS) |

</div>