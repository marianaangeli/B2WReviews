# 📊 Análise de Reviews de E-commerce com IA

> **Projeto desenvolvido durante o curso "Trilha para Elas - Introdução à Inteligência Artificial" do Instituto Eldorado**

## 🎯 Sobre o Projeto

Este projeto combina análise exploratória de dados (EDA) com modelos de Inteligência Artificial para extrair insights valiosos de reviews de e-commerce. Utilizando o dataset B2W Reviews, exploramos padrões de comportamento do consumidor e aplicamos modelos de linguagem para tarefas automatizadas.

## 📊 Dataset

**B2W Reviews - Avaliações Americanas.com**
- Dataset aberto de avaliação de produtos e-commerce
- **130.000+** avaliações de produtos vendidos pela Americanas.com
- **Período**: Janeiro a Maio de 2018
- **Fonte**: Disponível na plataforma Hugging Face (`ruanchaves/b2w-reviews01`)
- **Campos**: 14 variáveis incluindo notas, texto da review, dados demográficos e geolocalização

## 🤖 Tecnologias e Modelos Utilizados

- **Análise de Dados**: pandas, matplotlib, seaborn
- **Visualização**: WordCloud para análise de sentimentos
- **IA Generativa**: Llama-3.2-1B-Instruct (Hugging Face Transformers)
- **Processamento**: 132.373 avaliações após limpeza e deduplicação

## 📈 Principais Análises Realizadas

### 🔍 Análise Exploratória
- **Distribuição de Notas**: Padrão em U típico de e-commerce (polarização 1⭐ vs 4-5⭐)
- **Demografia**: Análise por gênero, faixa etária e localização geográfica
- **Categorias**: Top 10 produtos mais avaliados e satisfação por categoria
- **Correlação**: Forte relação entre nota e recomendação para amigos

### 🧠 Aplicações de IA

#### 1. **Análise de Sentimento Preditiva**
```python
# Modelo prevê se cliente recomendaria produto baseado na review
messages = [{"role": "user", "content": "Análise: produto não chegou no prazo..."}]
# ➜ Modelo analisa contexto e gera explicação estruturada
```

#### 2. **Geração Automática de Descrições**
```python
# Criação de descrições personalizadas por público-alvo
# ➜ Jovens gamers vs Adultos 40+ = descrições completamente diferentes
```

#### 3. **Sumarização Inteligente (RAG-like)**
```python
# Resumo automático de múltiplas reviews do mesmo produto
# ➜ Extração de pontos positivos/negativos + conclusão
```

## 🎯 Principais Descobertas

### 📊 Insights de Negócio
- Produtos com maior negatividade precisam de ação imediata
- **Eletrônicos** dominam o engajamento (smartphones = 790+ reviews)
- **Forte correlação** satisfação → recomendação (r > 0.8)

## 🚀 Como Executar

```bash
# 1. Clone o repositório
git clone [seu-repo]

# 2. Instale dependências
pip install datasets transformers matplotlib seaborn wordcloud pandas

# 3. Execute o notebook
jupyter notebook Encontro_1_TrilhaParaElasIA.ipynb
```

## 💡 Aplicações Práticas

- **E-commerce**: Monitoramento automático de satisfação
- **Marketing**: Geração de conteúdo personalizado
- **Atendimento**: Triagem inteligente de reclamações
- **Produto**: Identificação proativa de problemas

## 🎓 Aprendizados do Curso

Este projeto demonstra conceitos fundamentais abordados na **Trilha para Elas - IA**:
- Integração de modelos pré-treinados via Hugging Face
- Prompting eficaz para tarefas específicas
- Combinação de análise tradicional com IA generativa
- Aplicação prática de LLMs em problemas reais
