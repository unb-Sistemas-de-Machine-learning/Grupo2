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
A identificação de dados próximos é feita comparando vetores, que são representações numéricas do texto. Cada documento, frase ou trecho é transformado em um vetor que mostra o significado daquele conteúdo. Isso é feito por modelos chamados embeddings, que convertem o texto em números para que o sistema consiga medir o quanto dois conteúdos são parecidos.
</div>

---

#### Convertendo PDF em Vetor

<div align="justify">

&emsp;&emsp;
A conversão de arquivos PDF em vetores é uma etapa essencial no processo de indexação semântica. Primeiramente, o conteúdo textual é extraído do documento, removendo metadados, elementos gráficos e formatações desnecessárias. Em seguida, o texto é segmentado em blocos menores, como parágrafos ou frases, para otimizar o desempenho na recuperação de informações.

&emsp;&emsp;
Esses blocos são enviados a um modelo de embeddings, que cria um vetor numérico que representa o significado de cada trecho. Esses vetores são armazenados em um banco de dados vetorial (como o Qdrant), permitindo que o sistema faça buscas semânticas rápidas e precisas, com base na proximidade entre os vetores, e não apenas em correspondências exatas de palavras.
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