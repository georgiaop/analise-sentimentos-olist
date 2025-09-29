#  🧠Análise de Sentimentos em Avaliações da Olist

Este projeto realiza uma análise de sentimentos dos comentários dos clientes da Olist com base nas avaliações dos pedidos realizados na plataforma. A abordagem combina **NLP(Processamento de Linguagem Natural)** com **Machine Learning** para classificar automaticamente as avaliações como **positivas** ou **negativas**.

---

## 📁 Estrutura do Projeto

── dados/

│ └── olist_order_reviews_dataset.csv

├── img/

│ └── wordclouds_sentimento_olist.png

├── notebooks/

│ └── analise_sentimentos.ipynb

├── requirements.txt

└── README.md


---

## 📊 Objetivo

- Classificar automaticamente os comentários dos clientes com base nas avaliações (review_score).
- Identificar padrões de linguagem em reviews positivas e negativas.
- Gerar insights que possam auxiliar o time de **SAC, logística e marketing**.

---

## ⚙️ Tecnologias e Bibliotecas Usadas

- `pandas`, `numpy` – manipulação de dados
- `nltk`, `re`, `SnowballStemmer` – NLP
- `scikit-learn` – modelos de machine learning
- `matplotlib`, `seaborn` – visualização
- `wordcloud` – geração de nuvem de palavras

---

## 🧪 Modelos 

| Modelo                 | Acurácia | F1-Score (positiva) |
|------------------------|----------|----------------------|
| Logistic Regression    | 0.92     | 0.95                 |
| Naive Bayes            | 0.90     | 0.93                 |
| Random Forest          | 0.75     | 0.85                 |

> 🔎 **Melhor modelo:** `Logistic Regression`, com excelente equilíbrio entre precisão e interpretabilidade.

---

## 🧹 Pré-processamento

- Remoção de pontuações, números e acentos
- Transformação para minúsculas
- Stopwords removidas (usando NLTK)
- Stemmer (Snowball) aplicado em português
- Vetorização com TF-IDF (`max_features=3000`)

---

## ☁️ Nuvem de Palavras (WordCloud)

<img src="img/wordclouds_sentimento_olist.png" alt="WordClouds" width="100%"/>

- **💚 Positivas**: destaque para "ótimo", "excelente", "rápido", "parabéns"
- **💔 Negativas**: destaque para "produto", "problema", "não recebi", "atraso", "reclamei"

---

## 📌 Insights Extras

### Palavras mais comuns:

**🔹 Positivas**:
- ótimo, excelente, recomendo, entrega rápida, produto bom

**🔸 Negativas**:
- não recebi, produto errado, cancelado, péssimo, atraso

---
## 🔮 Conclusão

A regressão logística se mostrou o modelo mais eficaz para prever o sentimento.
A análise de sentimentos pode ajudar a empresa a identificar pontos fortes e fracos da experiência do cliente.
Insights podem ser utilizados para melhorar os serviços de entrega, atendimento e qualidade do produto.

---
## 📦 Como rodar o projeto

```bash
1. Clone o repositório:

git clone https://github.com/georgiaop/analise-sentimentos-olist.git
cd analise-sentimentos-olist

2. Instale as dependências:
pip install -r requirements.txt

3. Execute o notebook:
Abra o arquivo notebooks/analise_sentimentos_olist.ipynb em seu Jupyter Notebook ou Google Colab.


📌 Requisitos
Arquivo requirements.txt gerado com:
pip freeze > requirements.txt


 ✍️ Autor

Desenvolvido por [Georgia Oliveira Paixão Duarte ] 👨‍💻
Contato: georgiaop@outlook.com.br

GitHub: https://github.com/georgiaop
