Projeto acadêmico 

ANÁLISE DE CONSUMO ENERGÉTICO INDUSTRIAL
Dados sintéticos | Regressão múltipla | Excel 

Quais fatores mais influenciam o consumo de energia?

Utilizei um banco de dados em Excel para análise de fatores associados ao consumo energético de uma linha industrial - Banco Energia Producao.

Foram utilizadas variáveis como:
•	Máquinas; 
•	Ano; 
•	Data; 
•	Turno; 
•	Horas de Operação; 
•	Energia_kWh; 
•	Produção_Golpe; 
•	Consumo_kWh_por_Golpe. 

O objetivo foi aplicar regressão múltipla para identificar quais variáveis apresentam maior associação com o consumo energético. 

Não foram feitas várias análises iguais para várias máquinas, mas diferentes modelos de análises em máquinas diferentes a fim de demonstrar domínio e conhecimento de diferentes técnicas.

Partindo de uma planilha chamada Medicoes_Energia_Producao fizemos:

•	Nova planilha chamada Gráfico Dispersão Máq 01 - nessa planilha criamos um gráfico de dispersão (regressão linear) comparativo entre kWh x Golpes entre 2025 e 2026 com um ponto fundamental
(utilizamos a energia 2025 + 2026 da Máquina 01 não normalizada e comparamos com a energia 2025 + 2026 da Máquina 01 normalizada).

Isso foi feito porque, como os números vinham de uma base sintética de dados, o R² ficou bastante ruim (0,2924) quando comparamos dados não normalizados. Como o objetivo é demonstrar e avaliar 
correlação optei por criar uma coluna de Producao_Golpe normalizada. Um R² baixo significa que o modelo de regressão explica apenas uma pequena proporção da variação da variável dependente em 
relação à variabilidade total dos dados.

Para que isso ficasse adequado criamos uma coluna nova com dados também sintéticos, mas conexos com a realidade energética proposta pelo exercício. Com isso, conseguimos um 
R² de 0,8465, o que indica que o modelo de regressão explica quase toda a variação observada na variável dependente a partir das variáveis independentes incluídas no modelo.
Nessa planilha também fizemos a correlação de Pearson normalizada e obtivemos um valor de 0,920081 , o que indica uma forte relação linear entre as variáveis avaliadas.

Como se tratam de variáveis quantitativas contínuas, nessa mesma planilha aplicamos medidas descritivas, incluindo medidas de tendência central (média, mediana, moda) e de 
dispersão (variância e desvio padrão).

Para fazer previsão de consumo energético para 2027 criamos ainda nova tabela dentro dessa mesma planilha e usando fórmula aleatório entre 300 e 420 para produzir quantidade de peças aleatória, 
calculamos energia a ser consumida usando linha de tendência (Y=0,9987 + 8,0436) obtida durante testes nessa planilha. Aplicamos medidas descritivas para essa tabela também.

•	Nova planilha chamada Regressão MAQ 01 (Centro de Usinagem U01)onde utilizamos ferramenta de análise de dados para avaliar através da regressão os mesmos parâmetros verificados anteriormente 
sem uso dessa ferramenta. 

Através dessa ferramenta podemos analisar valor-p (probabilidade de observar um resultado tão extremo quanto o obtido, assumindo que a hipótese nula seja verdadeira; ele é usado para decidir se 
rejeitamos H₀ quando comparado a um nível de significância como 0,05), resíduos (análise de resíduos é o processo de examinar as diferenças entre valores observados e valores previstos por um 
modelo estatístico, usado para avaliar se o modelo se ajusta bem aos dados), além do R² e coeficientes que gerariam a linha de tendência para cálculos preditivos.

Como valor p ≥ α (0,09 >=0,05): não se rejeita H₀; os dados não fornecem evidência suficiente para rejeitá-la. 

O valor p depende fortemente do tamanho da amostra e nossa amostra nesse caso é de apenas 43 observações.

Resíduo = valor observado – valor previsto. Representa a parte dos dados que o modelo não explicou.

Resíduos próximos de zero indicam bom ajuste; resíduos grandes sugerem erro ou inadequação do modelo. O resíduo do nosso modelo é bastante significativo, o que explica que ele está ainda "sujo", 
não conseguindo nos dar um modelo preditivo totalmente "adequado". A análise de resíduos garante que o modelo estatístico seja confiável, evitando conclusões erradas e orientando ajustes, como 
transformar variáveis ou escolher outro tipo de modelo.

•	Nova planilha chamada Tabelas Dinâmicas onde utilizamos tabela dinâmica para avaliar Golpes/Horas Operação entre 2025 e 2026 com filtro por máquina e outra tabela dinâmica para avaliar Média de
Consumo_kWh_por_Golpe com filtro por turno. Não construí gráficos dinâmicos, mas poderiam facilmente ser gerados a partir desses dados. Outras tabelas também poderiam ser geradas a partir desses
dados, porém o objetivo era de mostrar várias maneiras de tratar os dados gerados sinteticamente. 

•	Modificando um pouco a tratativa dos dados foi criada nova planilha chamada LBE Maq 05 e 06 (Injetora I01 e Injetora I02) para criar uma linha de base e meta baseado nos dados sintéticos dessas 
máquinas em 2025. Usando 12 meses como base para essa avaliação, criamos IDE, LBE e Meta. Como parâmetro definimos que a meta seria 5% abaixo da LBE calculada e baseada em 2025. Criamos um gráfico
combinado de linhas e colinas para demonstrar dados também.

•	Criei nova planilha chamada LUCE (Lista de Usos e Consumos de Energia) baseada nos nossos dados sintéticos. Fiz formatação condicional com Escalas de Cor na coluna Soma de Energia_kWh e formatação
Barras de Dados na coluna Soma de Uso_kWh_por_Golpe. Classifiquei máquinas do Menor para o Maior na coluna TOP Consumidor.

•	Criei nova planilha dinâmica chamada TOP 5 baseada na planilha LUCE (Lista de Usos e Consumos de Energia) e nela separei os TOP 5 consumidores. Fiz gráfico dinâmico de pizza baseado nesse TOP 5 com
filtro para ano.

•	Criei nova planilha Gráficos Dinâmicos onde foram criados 3 gráficos dinâmicos combinados (linha e coluna) - kWh/golpe máquinas + Prensas ( Horas Operação x Produção_Golpes) com filtro por máquina, anos
e meses + Injetoras ( Produção_Golpes x Média de Consumo_kWh_por_ Golpe) com filtros por turno e por máquina.

•	Nova planilha chamada Gráfico Dispersão Máq 10 e 11 (Prensa P01 e Prensa P02)  - nessa planilha criamos um gráfico de dispersão (regressão linear) comparativo entre kWh x Golpes entre 2025 e 2026 sem 
normalizar. Sem normalizar os números da base sintética de dados, os R² das duas máquinas ficaram muito ruins. Como o objetivo é demonstrar e avaliar resultados em base não normalizada, conseguimos perceber
que o R² baixo demonstra que o modelo de regressão não explica o consumo pela produção.
Como se tratam de variáveis quantitativas contínuas, nessa mesma planilha aplicamos medidas descritivas, incluindo medidas de tendência central (média) e de dispersão (variância e desvio padrão).


