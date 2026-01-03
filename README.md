# 🔍 Semantic Search em Documentos PDF com NLP e Transformers

Este projeto implementa um sistema completo de **busca semântica** aplicado a
documentos em formato **PDF**, utilizando técnicas modernas de
**Processamento de Linguagem Natural (NLP)** e **modelos de linguagem
pré-treinados**, sem o uso de APIs pagas.

---

## 📌 Objetivo
Desenvolver uma solução capaz de recuperar trechos relevantes de um documento
com base no **significado da consulta do usuário**, e não apenas por
correspondência literal de palavras-chave.

---

## 🧠 O que é Busca Semântica?
Busca semântica representa textos como **vetores numéricos (embeddings)** em um
espaço semântico, permitindo identificar conteúdos conceitualmente relacionados,
mesmo quando não compartilham as mesmas palavras.

---

## 📚 Fonte dos Dados
Como exemplo prático, este projeto utiliza o livro **_Deuses Americanos_**, de
**Neil Gaiman**, fornecido em formato **PDF**.

⚠️ **Observação importante:**  
Por questões de **direitos autorais**, arquivos PDF/EPUB **não são incluídos neste
repositório**.

A pipeline foi projetada de forma **genérica**, podendo ser aplicada a qualquer
arquivo PDF que contenha texto extraível, como:

- Livros
- Artigos científicos
- Relatórios
- Documentação técnica

---

## 🧩 Pipeline do Projeto
O sistema segue as seguintes etapas:

1. Extração de texto do PDF  
2. Limpeza e normalização do texto  
3. Segmentação em blocos (chunks)  
4. Geração de embeddings semânticos  
5. Indexação vetorial com FAISS  
6. Busca semântica por similaridade de cosseno  

---

## 🧠 Modelo Utilizado
- **Sentence Transformer:** `all-MiniLM-L6-v2`
- Embeddings de 384 dimensões
- Execução local (CPU)
- Sem necessidade de treinamento adicional

---

## ⚡ Busca Vetorial
A busca é realizada com **FAISS (Facebook AI Similarity Search)**, utilizando
similaridade por cosseno (via inner product com vetores normalizados), garantindo
alta eficiência mesmo para grandes volumes de texto.

---

## 📁 Estrutura do Projeto

```text
semantic-search-nlp/
│
├── semantic_search.ipynb
│
├── data/
│   └── documents/
│       └── deuses_americanos.pdf
│
├── requirements.txt
└── README.md

Para executar o projeto, basta adicionar um PDF na pasta:

```text
data/documents/
