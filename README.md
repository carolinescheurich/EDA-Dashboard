# 📊 Análise Operacional do CallMeMaybe (Churn de Chamadas / Calls Lost)

## Contexto do Projeto
Este projeto realiza uma Análise Exploratória de Dados (EDA) e um estudo operacional sobre o serviço de telefonia virtual CallMeMaybe.

O objetivo principal é entender padrões de uso, gargalos operacionais e comportamentos de atendimento, identificando oportunidades para otimização da operação e redução de chamadas perdidas.

Além da análise exploratória, foi estruturado um Dashboard de performance operacional, permitindo monitoramento contínuo e tomada de decisão baseada em dados.


## 🎯 Objetivos da análise
1. Identificar padrões de volume, eficiência e perdas no atendimento.
2. Avaliar o impacto da carga de trabalho na taxa de chamadas perdidas.
3. Segmentar operadores com base em indicadores operacionais (clustering).
4. Apoiar recomendações práticas para planejamento de capacidade e redistribuição de chamadas.
5. Disponibilizar uma visualização executiva via dashboard.

## 📂 Estrutura dos Dados
O dataset utilizado contém informações operacionais por operador, incluindo:

- Volume de chamadas atendidas
- Taxa de chamadas perdidas
- Indicadores de eficiência de atendimento
- Métricas de qualidade e desempenho

## ⚙️ Metodologia

### 1. **Preparação e limpeza dos dados**
- Importação do dataset
- Verificação de consistência e valores nulos
- Padronização de colunas e tipos de dados
- Construção de métricas derivadas (indicadores operacionais)

### 2. **Análise Exploratória (EDA)**
- Distribuição de volume de chamadas entre operadores
- Distribuição de perdas e eficiência
- Identificação de operadores em risco (alto volume + alta perda)

### 3. **Análises de Relação entre Métricas**
- Avaliação da correlação entre eficiência e taxa de perda
- Análise do impacto do volume de chamadas sobre o desempenho
- Detecção de um possível “ponto de ruptura”, quando o volume começa a degradar os indicadores da operação

### 4. **Segmentação com Clusterização**
- Segmentação de operadores com comportamento operacional semelhante (ex: KMeans)
- Comparação entre clusters quanto a:
  - Eficiência média
  - Variabilidade de desempenho
  - Volume de chamadas
  - Risco operacional

### 5. **Dashboard**
Foi criado um dashboard com indicadores operacionais para apoiar:
- Monitoramento automatizado
- Tomada de decisão gerencial
- Identificação rápida de gargalos


## 📈 Principais Insights e Conclusões

### ✅ Visão geral
A análise confirma que a carga de trabalho é o principal fator de ineficiência operacional, e não a qualidade individual dos operadores.

Quando o volume cresce, a taxa de perda dispara — evidência direta de subdimensionamento e má distribuição de carga.

### 🔎 Achados relevantes
- Existe uma relação linear negativa entre eficiência e taxa de perda: quanto maior a eficiência, menor a perda.
- Muitos operadores estão abaixo da “zona ideal”, indicando que não conseguem atender ao volume imposto.
- O clustering revelou perfis extremizados: sobrecarga não significa incompetência, e sim falta de capacidade.
- O cluster de maior risco recebe até 3× mais chamadas, concentrando operadores sobrecarregados.
- Tendência forte: mais volume → mais perda.
- Operadores com volume alto e perdas acima de 70% exigem intervenção imediata.
- Um corte/redistribuição da carga nos 20% operadores mais sobrecarregados aumentaria a eficiência geral automaticamente.

### 🧾 Conclusão final
📌 O problema é estrutural, não humano:
- A operação está subdimensionada
- A carga não está bem distribuída
- A performance melhora ao otimizar capacidade, sem necessidade de substituição de operadores


## ✅ Recomendações de Negócio
- Redistribuição e balanceamento de volume
- Ampliar capacidade/canalidade em horários críticos
- Treinamento direcionado para redução do Tempo Médio de Atendimento (TMA)
- Monitoramento automatizado via dashboard

📌 Estamos perdendo clientes por gargalos operacionais, não por falhas individuais.
Melhorar a distribuição de carga tende a trazer retorno rápido e significativo sem aumento proporcional de custos.


## 🛠️ Tecnologias e Bibliotecas Utilizadas
O projeto foi desenvolvido em Python, com foco em análise e visualização:

- **Pandas / NumPy** → manipulação e análise de dados
- **Matplotlib / Seaborn / Plotly** → visualizações e análises
- **Scikit-learn** → clusterização e modelos auxiliares
- **Jupyter Notebook** → ambiente de análise
- **Dashboard (Tableau)** → visualização operacional
