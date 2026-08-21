# 🚔 Data Analytics & EDA - Acidentes PRF 2025

**Autor:** José Guilherme Teixeira Nunes  
**Disciplina:** Análise Exploratória de Dados (EDA) e Analytics  
**Base de Dados:** `dados_abertos_prf-datatran2025.csv` (Polícia Rodoviária Federal)

---

## 📌 Visão Geral do Projeto

O desenvolvimento foi realizado inteiramente por meio de planilhas eletrônicas (Google Sheets), utilizando Tabelas Dinâmicas, Fórmulas e Campos Calculados para extrair insights acionáveis sem a necessidade de linguagens de programação.

---

## 🧠 Processo de Escolha e Evolução dos KPIs

A fase inicial da análise consistiu em calcular métricas descritivas (ex: volume de acidentes por estado, por clima, por tipo). Embora úteis para entender o cenário geral, essas métricas apresentavam limitações na tomada de decisão. 

Para transformar **métricas descritivas** em **KPIs Estratégicos (Key Performance Indicators)**, adotou-se o seguinte raciocínio:

1. **Foco na Severidade (Taxa de Letalidade):** Em vez de olhar apenas para volumes absolutos, cruzamos o total de acidentes com a quantidade de acidentes fatais. O objetivo foi descobrir "onde a chance de óbito é desproporcionalmente maior".
2. **Filtro de Relevância Estatística:** Na análise de causas, aplicamos um limite mínimo de ocorrências (ex: > 100 acidentes) para eliminar ruídos estatísticos e isolar os padrões reais de comportamento letal.
3. **Acionabilidade:** Todo KPI foi desenhado com o critério SMART em mente, garantindo que a elevação ou queda do indicador possa ser diretamente ligada a uma ação de campo da PRF (patrulhamento, educação ou engenharia).

---

## 📊 Os 5 KPIs Estratégicos Desenvolvidos

Abaixo estão detalhados os 5 indicadores principais que compõem o *Dashboard Executivo*, suas justificativas analíticas e as recomendações práticas derivadas de cada um.

### 1. Índice de Severidade em Pistas Simples (ISPS)
* **Conceito:** Mede a diferença de letalidade entre tipos de traçado viário.
* **Justificativa Analítica:** A análise comprovou que a letalidade em acidentes nas pistas simples (9,86%) é praticamente o dobro da registrada nas pistas duplas (4,88%).

### 2. Fator de Letalidade Noturna (FLN)
* **Conceito:** Avalia o salto de risco associado à condução em horários de baixa luminosidade natural.
* **Justificativa Analítica:** Enquanto o pleno dia apresenta 5,07% de letalidade, a plena noite (10,18%) e o amanhecer (11,20%) dobram esse risco. Um *drill-down* geográfico revelou extremos críticos: em estados como Maranhão e Alagoas, a letalidade noturna ultrapassa os 24%, triplicando o risco diurno.

### 3. Taxa de Risco de Condutas Letais (TRCL)
* **Conceito:** Identifica as infrações de trânsito que possuem a maior conversão em óbitos, independentemente da sua frequência total.
* **Justificativa Analítica:** Condutas específicas mostraram taxas alarmantes. "Transitar na contramão" converte 29,74% de suas ocorrências em acidentes fatais (quase 1 em cada 3), seguido por ultrapassagens indevidas (17,06%).

### 4. Taxa de Letalidade de Usuários Vulneráveis (TLUV)
* **Conceito:** Mensura o impacto dos acidentes envolvendo pedestres nas rodovias.
* **Justificativa Analítica:** Os dados mostraram que o evento "Pedestre andava na pista" possui a taxa de letalidade mais drástica (excluindo suicídios presumidos), atingindo 41,25% (250 óbitos em 606 ocorrências).

### 5. Alerta de Risco Climático (Nevoeiro/Neblina)
* **Conceito:** Relativiza o volume de acidentes pela condição meteorológica adversa.
* **Justificativa Analítica:** A chuva é a condição adversa mais comum, mas tem letalidade de 6,24%. O nevoeiro/neblina, embora menos frequente, impõe um risco severo com taxa de fatalidade de 10,85%, demonstrando a criticidade da perda total de visibilidade em velocidade rodoviária.
---

## 🛠️ Ferramentas e Técnicas
* **Google Sheets**
* Tabelas Dinâmicas (Cruzamento de Dimensões Temporais, Espaciais e Operacionais).
* Campos Calculados e Fórmulas Lógicas (Estruturação da _flag_ de acidentes fatais).
* Filtros de Valor (Isolamento de amostras com relevância estatística, ex: > 100).
