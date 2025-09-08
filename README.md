# 📊 Projeto de Ciência de Dados e Inteligência Artificial – Acidentes de Trânsito em Porto Alegre  

## 📌 Introdução  
Este projeto tem como objetivo aplicar conceitos de **Ciência de Dados** e **Inteligência Artificial** na análise de acidentes de trânsito em Porto Alegre.  

O trabalho foi dividido em duas fases:  
1. **Fase 1** – Seleção, exploração inicial e preparação do conjunto de dados.  
2. **Fase 2** – Aplicação de algoritmos de aprendizado de máquina e avaliação de desempenho.  

O dataset foi obtido do portal de [**Dados Abertos de Porto Alegre**](https://dadosabertos.poa.br/dataset/acidentes-de-transito-acidentes) e reúne informações temporais, geográficas e descritivas sobre os acidentes, incluindo a **UPS (Unidade Padrão de Severidade)**, utilizada como **atributo alvo**.  

---

## 📂 Conjunto de Dados  
- **Fonte**: [Dados Abertos de Porto Alegre](https://dadosabertos.poa.br/dataset/acidentes-de-transito-acidentes)  
- **Quantidade de registros**: 6.690 linhas  
- **Quantidade de atributos selecionados**: 10 colunas  
- **Formato disponível**: CSV  
- **Recorte aplicado**: acidentes ocorridos entre **01/01/2025 e 27/07/2025**, com remoção de linhas incompletas.  

---

## 📑 Colunas Selecionadas  

| Variável       | Descrição                               | Tipo       | Exemplo |
|----------------|-----------------------------------------|-----------|---------|
| **data**       | Data do acidente                        | Data      | 01/01/2025 |
| **tipo_acid**  | Tipo de acidente                        | Nominal   | Colisão, Atropelamento |
| **regiao**     | Região da cidade                        | Nominal   | Centro, Leste |
| **dia_sem**    | Dia da semana                           | Nominal   | Segunda, Quarta-feira |
| **feridos**    | Número de feridos leves                 | Numérico  | 0, 1, 2 |
| **feridos_gr** | Número de feridos graves                | Numérico  | 0, 1, 2 |
| **mortes**     | Número de vítimas fatais                | Numérico  | 0, 1 |
| **latitude**   | Coordenada geográfica                   | Numérico  | -30.0476 |
| **longitude**  | Coordenada geográfica                   | Numérico  | -51.183 |
| **UPS**        | Unidade Padrão de Severidade (**alvo**) | Numérico  | 1, 2, 13 |

---

## 🔎 Fase 1 – Exploração Inicial  
- Estatísticas descritivas das variáveis com **Feature Statistics**.  
- Verificação da distribuição da variável **UPS**.  
- Análises gráficas com **Scatter Plot** e **Correlations**, revelando que **feridos, feridos graves e mortes** possuem forte correlação positiva com a UPS.  

---

## 🤖 Fase 2 – Modelagem Preditiva  

### Algoritmos utilizados  
- **Linear Regression** – modelo simples, usado como linha de base.  
- **Random Forest** – robusto, captura relações não lineares e interações complexas.  
- **Gradient Boosting** – modelo avançado para casos de maior severidade.  

### Preparação dos dados  
- Conversão de variáveis categóricas com **One-Hot Encoding** (widget *Continuize*).  
- Divisão em treino (80%) e teste (20%) com **Data Sampler**.  

### Avaliação dos modelos  
Métricas utilizadas: **MAE, RMSE, MSE e R²**, com validação cruzada (10 folds).  

| Modelo            | MAE   | RMSE  | MSE   | R²    |
|-------------------|-------|-------|-------|-------|
| Random Forest     | 0.449 | 0.638 | 0.407 | 0.820 |
| Gradient Boosting | 0.457 | 0.647 | 0.418 | 0.815 |
| Linear Regression | 0.485 | 0.686 | 0.471 | 0.793 |

➡️ **Random Forest** apresentou o melhor desempenho, com **R² de 0.820** e **RMSE de 0.638**.  

---

## 🎯 Conclusões  
- Modelos mais complexos (Random Forest, Gradient Boosting) foram superiores à regressão linear, indicando que a severidade dos acidentes depende de relações **não lineares**.  
- A variável **UPS** se mostrou uma excelente escolha como alvo, permitindo capturar diferentes níveis de gravidade.  
- O projeto demonstra o potencial da ciência de dados para **transformar dados brutos em inteligência aplicada à segurança viária**, apoiando políticas públicas e estratégias de prevenção.  

---
