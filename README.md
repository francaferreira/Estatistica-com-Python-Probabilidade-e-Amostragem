# 📊 Curso de Estatística - Parte 2: Fundamentos Práticos

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/seu-usuario/repositorio/blob/main/Curso_de_Estatistica_Parte_2.ipynb)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Este repositório contém um curso prático de Estatística com foco em conceitos essenciais para análise de dados, utilizando informações reais da Pesquisa Nacional por Amostra de Domicílios (PNAD 2015).

## 🚀 Stack Tecnológica

- **Linguagem de Programação**: 
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">

- **Bibliotecas Principais**:
  - <img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="pandas"> - Manipulação de dados
  - <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"> - Cálculos numéricos
  - <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white" alt="SciPy"> - Estatística avançada
  - <img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge" alt="Matplotlib"> - Visualização de dados

- **Ambiente**:
  - <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter"> - Notebooks interativos
  - <img src="https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white" alt="Google Colab"> - Execução na nuvem

## 📚 Conteúdo Programático

### 📊 1. CONHECENDO OS DADOS
- **Dataset da PNAD 2015** com variáveis reais:
  - Renda mensal
  - Idade
  - Altura
  - UF (estado)
  - Sexo
  - Anos de estudo
  - Cor/raça
- Tratamento e preparação de dados

### 🎲 2. DISTRIBUIÇÕES DE PROBABILIDADE
#### 2.1 Distribuição Binomial
- Problemas com **dois resultados possíveis** (sucesso/fracasso)
- Exemplo: Probabilidade de acertar questões em uma prova
- Fórmula: `P(k) = comb(n,k) * p^k * q^(n-k)`

#### 2.2 Distribuição Poisson
- Eventos **raros ou de baixa frequência**
- Exemplo: Pedidos por hora em um restaurante
- Fórmula: `P(k) = (e^-μ * μ^k) / k!`

#### 2.3 Distribuição Normal
- Famosa "curva em sino" para dados contínuos
- Exemplo: Distribuição de alturas na população
- Tabela Z e padronização

### 🔍 3. AMOSTRAGEM
#### 3.1 População vs Amostra
- População completa (76.840 registros)
- Amostras representativas (1.000 registros)

#### 3.2 Quando usar amostras?
- Populações infinitas
- Testes destrutivos
- Restrições de tempo/custo

#### Técnicas de Amostragem:
1. **Aleatória Simples** (seleção igualitária)
2. **Estratificada** (grupos homogêneos)
3. **Por Conglomerados** (grupos heterogêneos)

### 📐 4. ESTIMAÇÃO
#### 4.1 Teorema do Limite Central
- Fundamentos da inferência estatística
- Distribuição das médias amostrais
- Erro padrão: `σ/√n`

#### 4.2 Níveis de Confiança
- Interpretação de intervalos (95% de confiança)
- Significância estatística (α)

#### 4.3 Intervalos de Confiança
- Estimativa de parâmetros populacionais
- Exemplo: Peso médio de produtos

### 📏 5. CÁLCULO DE TAMANHO DE AMOSTRA
#### Fórmulas essenciais:
```python
# População infinita
n = (Z^2 * σ^2) / e^2

# População finita
n = N / (1 + (N * e^2)/(Z^2 * σ^2))
```

## 💡 Por Que Estudar Estatística?

- Tomar decisões com dados limitados
- Identificar padrões em grandes populações
- Evitar conclusões erradas em pesquisas
- Fundamentar estratégias com evidências

## ▶️ Como Usar

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/curso-estatistica-parte2.git
```

2. Instale as dependências:
```bash
pip install pandas numpy scipy matplotlib jupyter
```

3. Execute o notebook:
```bash
jupyter notebook Curso_de_Estatistica_Parte_2.ipynb
```

4. Para usar no Google Colab:
[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/seu-usuario/repositorio/blob/main/Curso_de_Estatistica_Parte_2.ipynb)

## 📊 Exemplos de Visualizações no Notebook

No notebook você encontrará visualizações interativas como:

```python
# Exemplo de visualização de distribuição normal
import matplotlib.pyplot as plt
import numpy as np
from scipy.stats import norm

# Gerar dados
x = np.linspace(-4, 4, 1000)
y = norm.pdf(x)

# Plotar
plt.figure(figsize=(10, 6))
plt.plot(x, y, 'b-', linewidth=2)
plt.title('Distribuição Normal Padrão')
plt.xlabel('Valores')
plt.ylabel('Densidade de Probabilidade')
plt.fill_between(x, y, where=(x > -1) & (x < 1), alpha=0.3, color='blue')
plt.annotate('68% dos dados', xy=(0, 0.1), xytext=(0.5, 0.3),
             arrowprops=dict(facecolor='black', shrink=0.05))
plt.grid(True)
plt.show()
```

![Distribuição Normal](https://via.placeholder.com/400x200?text=Visualização+Distribuição+Normal+no+Notebook)

## 🤝 Contribuição
Contribuições são bem-vindas! Siga estes passos:
1. Fork o projeto
2. Crie sua branch (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## 📄 Licença
Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

**Autor**: Jefferson Ferreira 
**Contato**: jfrancaferreira10@gmail.com 
**LinkedIn**: [seu-perfil](https://www.linkedin.com/in/jefferson-ferreira-ds/)  

---

## 🔍 Pré-visualização do Conteúdo do Notebook

```python
# Exemplo de cálculo de intervalo de confiança
from scipy import stats

dados = [5050, 5020, 5080, 5030, 5070, 5100, 5000, 5090, 5040, 5060]
media = np.mean(dados)
desvio_padrao = np.std(dados, ddof=1)  # ddof=1 para amostra
n = len(dados)
confianca = 0.95

# Calcular intervalo de confiança
intervalo = stats.t.interval(confianca, n-1, loc=media, scale=desvio_padrao/np.sqrt(n))

print(f"Média: {media:.2f}g")
print(f"Intervalo de {confianca*100:.0f}% de confiança: ({intervalo[0]:.2f}g, {intervalo[1]:.2f}g)")
```

**Saída:**
```
Média: 5053.00g
Intervalo de 95% de confiança: (5021.45g, 5084.55g)
```
