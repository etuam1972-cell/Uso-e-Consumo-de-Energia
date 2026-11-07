# ⚡ ANÁLISE DE CONSUMO ENERGÉTICO INDUSTRIAL
### 📊 Dados sintéticos | Regressão múltipla | Excel | Eficiência Energética

---

## 🎯 Objetivo do Projeto

**Quais fatores mais influenciam o uso e consumo de energia em uma linha industrial?**

Este projeto tem como objetivo aplicar técnicas de análise exploratória e estatística para avaliar fatores associados ao consumo energético de equipamentos industriais, utilizando uma base de dados sintética desenvolvida em Excel.

O estudo busca demonstrar diferentes abordagens para tratamento, interpretação e visualização de dados, com foco em eficiência energética, correlação entre variáveis e análise de desempenho operacional.

### 🏭 Variáveis utilizadas

- ⚙️ Máquinas
- 📅 Ano e data das medições
- 🔄 Turno de operação
- ⏱️ Horas de operação
- ⚡ Energia consumida (kWh)
- 🔨 Produção (golpes)
- 📈 Consumo específico (kWh/golpe)

**Base de dados:** `Banco_Energia_Producao`  
**Ferramenta principal:** Microsoft Excel

---

## 🔎 1. Gráfico de Dispersão – Máquina 01 | Centro de Usinagem U01

📌 **Objetivo:** avaliar a relação entre consumo energético e produção, comparando os dados de 2025 e 2026.

Foram desenvolvidas duas análises:

- 📉 **Dados originais:** energia e produção sem normalização.
- 📈 **Dados normalizados:** utilização de uma coluna sintética de `Producao_Golpe` ajustada para representar uma relação energética mais consistente com o objetivo didático do exercício.

### 📊 Resultados

| Indicador | Resultado |
|---|---:|
| R² – dados originais | 0,2924 |
| R² – dados normalizados | 0,8465 |
| Correlação de Pearson – normalizada | 0,920081 |

O modelo com dados originais apresentou baixo poder explicativo. Após a criação de uma variável sintética normalizada, foi obtido um R² de 0,8465, indicando maior proporção da variabilidade do consumo explicada pela relação linear representada no exercício.

A correlação de Pearson de 0,920081 demonstra uma forte associação linear positiva entre as variáveis analisadas.

🔄 **Simulação:** a planilha permite atualizar os valores normalizados por meio de **Dados → Atualizar Tudo**, possibilitando observar como alterações nos dados afetam os resultados estatísticos.

### 📐 Estatística descritiva

Foram aplicadas medidas de:

- Tendência central: média, mediana e moda.
- Dispersão: variância e desvio padrão.

### 🔮 Previsão de consumo – 2027

Foi desenvolvida uma tabela de projeção com quantidade de peças gerada aleatoriamente entre 300 e 420 unidades.

A estimativa de consumo utiliza a equação da linha de tendência obtida durante os testes:

`Y = 0,9987 + 8,0436`

Também foram aplicadas medidas estatísticas descritivas aos valores projetados.

---

## 📉 2. Regressão – Máquina 01 | Centro de Usinagem U01

📌 **Objetivo:** aprofundar a análise estatística utilizando a ferramenta **Análise de Dados → Regressão** do Excel.

Foram avaliados os mesmos parâmetros da análise anterior, acrescentando indicadores estatísticos que permitem investigar a qualidade do ajuste.

### 🧪 Indicadores avaliados

- 📊 Coeficiente de determinação (R²).
- 📌 Coeficientes da regressão.
- 🎯 Valor-p e significância estatística.
- 📉 Resíduos do modelo.
- 🔍 Diferença entre valores observados e previstos.

### ⚠️ Interpretação dos resultados

O modelo apresentou valor-p de aproximadamente 0,09 para o parâmetro avaliado.

Considerando nível de significância de 5%:

`Valor-p = 0,09 > α = 0,05`

Portanto, não se rejeita a hipótese nula para esse teste. Os dados não fornecem evidência estatística suficiente para considerar o parâmetro significativo ao nível de 5%.

A amostra utilizada contém apenas 43 observações, aspecto que deve ser considerado na interpretação dos resultados.

### 📍 Análise de resíduos

Resíduo = Valor observado − Valor previsto.

Os resíduos representam a parcela da variação que não foi explicada pelo modelo.

A análise permitiu identificar limitações no ajuste estatístico e reforçou a importância de avaliar a qualidade dos dados antes de utilizar uma regressão para previsões operacionais.

---

## 📋 3. Tabelas Dinâmicas

📌 **Objetivo:** demonstrar a utilização de tabelas dinâmicas para resumir e comparar indicadores operacionais.

Foram desenvolvidas duas análises:

**Tabela dinâmica 01**
- 🔨 Golpes produzidos.
- ⏱️ Horas de operação.
- 📅 Comparação entre 2025 e 2026.
- ⚙️ Filtro por máquina.

**Tabela dinâmica 02**
- ⚡ Média de consumo (kWh/golpe).
- 🔄 Filtro por turno.

As tabelas permitem segmentar os dados e identificar diferenças de desempenho entre máquinas, períodos e turnos.

---

## 🎯 4. Linha de Base Energética (LBE) – Máquinas 05 e 06

🏭 **Equipamentos:** Injetora I01 e Injetora I02.

📌 **Objetivo:** construir uma linha de base energética e estabelecer uma meta de melhoria utilizando os dados sintéticos de 2025.

Foram utilizados 12 meses de medições para desenvolver:

- 📊 IDE – Indicador de Desempenho Energético.
- 📈 LBE – Linha de Base Energética.
- 🎯 Meta de desempenho energético.

### Meta estabelecida

Foi adotada uma meta de redução de **5% em relação à LBE calculada para 2025**.

Também foi desenvolvido um gráfico combinado de linhas e colunas para facilitar a comparação entre o desempenho observado, a linha de base e a meta.

---

## ⚡ 5. LUCE – Lista de Usos e Consumos de Energia

📌 **Objetivo:** identificar e classificar os principais consumidores de energia da operação.

A planilha consolida os dados por máquina e permite visualizar os indicadores de consumo.

### Recursos aplicados

- 🎨 Escalas de cores na coluna `Soma de Energia_kWh`.
- 📊 Barras de dados na coluna `Soma de Uso_kWh_por_Golpe`.
- 🔢 Classificação das máquinas do menor para o maior consumo.
- 🏆 Identificação dos principais consumidores de energia.

A LUCE permite direcionar a atenção para equipamentos com maior participação no consumo energético e apoiar a priorização de oportunidades de melhoria.

---

## 🏆 6. TOP 5 – Maiores Consumidores de Energia

📌 **Objetivo:** destacar os cinco equipamentos com maior consumo energético.

A planilha foi desenvolvida a partir da LUCE, utilizando os dados consolidados para identificar os principais consumidores.

### Recursos aplicados

- 🥇 Ranking dos cinco maiores consumidores.
- 🥧 Gráfico dinâmico de participação no consumo.
- 📅 Filtro por ano.

A análise facilita a identificação dos equipamentos prioritários para investigação e possíveis ações de eficiência energética.

---

## 📊 7. Gráficos Dinâmicos – Análise Operacional e Energética

📌 **Objetivo:** integrar indicadores de produção, horas de operação e consumo específico em visualizações interativas.

Foram desenvolvidos três gráficos dinâmicos combinados, utilizando linhas e colunas.

### 🔩 Análise 01 – Consumo específico por máquina

- Indicador: kWh/golpe.
- Comparação entre máquinas.
- Filtros por máquina, ano e mês.

### 🏭 Análise 02 – Prensas

- Horas de operação.
- Produção em golpes.
- Filtros por máquina, ano e mês.

### 💉 Análise 03 – Injetoras

- Produção em golpes.
- Média de consumo (kWh/golpe).
- Filtros por turno e máquina.

As visualizações permitem explorar diferentes relações entre produção e consumo energético, facilitando a interpretação dos indicadores operacionais.

---

## 📉 8. Gráfico de Dispersão – Máquinas 10 e 11 | Prensas P01 e P02

📌 **Objetivo:** avaliar a relação entre consumo energético e produção utilizando os dados originais, sem normalização.

Foram desenvolvidos gráficos de dispersão para as duas prensas, considerando os dados de 2025 e 2026.

### 🔍 Análise realizada

- ⚡ Energia consumida (kWh).
- 🔨 Produção (golpes).
- 📈 Linha de tendência linear.
- 📊 Coeficiente de determinação (R²).
- 📐 Média, variância e desvio padrão.

Os resultados apresentaram baixos valores de R², indicando que a produção, isoladamente, não explica adequadamente a variação do consumo energético dessas máquinas na base sintética utilizada.

Essa análise demonstra a importância de investigar outros fatores que podem influenciar o consumo, como horas de operação, regime de funcionamento, tempo ocioso, características do processo e condições operacionais.

---

## 🧠 Principais conhecimentos aplicados

| Área | Técnicas e ferramentas |
|---|---|
| 📊 Análise de dados | Tratamento e organização de bases |
| 📈 Estatística | Média, mediana, moda, variância e desvio padrão |
| 🔗 Correlação | Correlação de Pearson |
| 🧮 Modelagem | Regressão linear e múltipla |
| 🧪 Validação | Valor-p e análise de resíduos |
| ⚡ Gestão energética | IDE, LBE e metas |
| 📋 Excel | Tabelas dinâmicas e formatação condicional |
| 📊 Visualização | Gráficos de dispersão, combinados e dinâmicos |

---

## 💡 Conclusão

O projeto demonstra diferentes formas de analisar dados industriais utilizando o Microsoft Excel, explorando técnicas estatísticas e recursos de visualização para investigar relações entre consumo energético e produção.

Um dos principais aprendizados foi compreender que **correlação não significa causalidade** e que um R² elevado, por si só, não garante um modelo preditivo confiável.

A qualidade dos dados, a seleção das variáveis, a representatividade da amostra e a análise dos resíduos são fundamentais para construir modelos estatísticos consistentes.

A proposta é demonstrar como ferramentas de análise de dados podem contribuir para a gestão energética industrial, identificação de oportunidades de melhoria e suporte à tomada de decisão.

---

## ⚠️ Observação sobre os dados

Este projeto utiliza **dados sintéticos**, desenvolvidos exclusivamente para fins acadêmicos e demonstração técnica.

Os valores normalizados e as projeções não representam medições reais de equipamentos industriais. Os resultados estatísticos devem ser interpretados dentro das premissas e limitações dessa base.

---

## 🛠️ Ferramentas utilizadas

- 🟩 Microsoft Excel
- 📊 Ferramenta Análise de Dados (Analysis ToolPak)
- 📈 Gráficos de dispersão e gráficos dinâmicos
- 🧮 Fórmulas estatísticas e regressão linear

**Projeto acadêmico | Análise de Dados aplicada à Eficiência Energética Industrial**
