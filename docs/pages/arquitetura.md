<center>

# Arquitetura do Projeto

</center>

---


<div align="justify">

&emsp;&emsp;
A arquitetura segue o modelo RAG, Retrieval-Augmented Generation, que combina recuperação de informações com geração de texto para fornecer respostas precisas e contextuais. Sendo assim, podemos dividir a aplicação em três componentes principais: o banco de dados vetorial, os modelos de machine learning e a API, conforme ilustrado na Figura 1 desta página.
</div>


<center>

**Figura 1**: Representação arquitetural do sistema.

</center>

<center>
    <img src="assets/arquitetura.png" alt="Arquitetura" style="width:100%; max-width: 800px;"/>
</center>

<center>

**Fonte**: Carvalho, Ginuino (2025).

</center>

---

## Tecnologias Utilizadas

* **Banco de Dados Vetorial**: Qdrant
* **Modelos de Machine Learning**: Gemini Pro - Google Cloud
* **API**: Telegram Bot API - Python
* **Web Scraper**: BeautifulSoup - Python

---

<center>

## Histórico de Versão

</center>

<div style="margin: 0 auto; width: fit-content;">

| Data       | Versão | Descrição            | Autores                                   |
|------------|--------|----------------------|-------------------------------------------|
| 06/10/2025 | `1.0`  | Criação do documento | [João Ginuino](https://github.com/i-JSS) |

</div>