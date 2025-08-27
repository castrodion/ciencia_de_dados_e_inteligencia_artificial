# 📊 Projeto de Ciência de Dados e Inteligência Artificial – Fase 1
### Análise de Acidentes de Trânsito em Porto Alegre  

## 📌 Introdução  
O objetivo desta primeira fase do projeto é selecionar um conjunto de dados relevante, realizar uma exploração inicial com a ferramenta **Orange Data Mining** e identificar oportunidades de aplicação em ciência de dados e inteligência artificial.  

O dataset escolhido refere-se aos **acidentes de trânsito registrados no município de Porto Alegre**, disponibilizado no portal de dados abertos da cidade. Esse conjunto reúne informações temporais, geográficas e descritivas sobre os acidentes, incluindo a gravidade de cada evento.  

Entre as variáveis selecionadas destacam-se: tipo de acidente, região, dia da semana, número de feridos, feridos graves, mortes, localização geográfica (latitude e longitude), data da ocorrência e a **UPS (Unidade Padrão de Severidade)**, que será utilizada como atributo alvo do projeto.  

Esse conjunto de dados é particularmente interessante por possibilitar análises estatísticas e geográficas que podem auxiliar na **prevenção de acidentes** e na formulação de **políticas públicas de segurança viária**.  

---

## 📂 Conjunto de Dados  
- **Fonte**: [Dados Abertos de Porto Alegre](https://dadosabertos.poa.br/dataset/acidentes-de-transito-acidentes)  
- **Quantidade de registros**: 6.690 linhas  
- **Quantidade de atributos selecionados**: 10 colunas  
- **Formato disponível**: CSV  
- **Recorte aplicado**: apenas acidentes ocorridos entre **01/01/2025 e 27/07/2025**, com exclusão de linhas vazias.  

---

## 📑 Colunas Selecionadas  

| Variável     | O que representa                         | Tipo de dado | Exemplos de valores |
|--------------|------------------------------------------|--------------|---------------------|
| **data**     | Data do acidente                         | Data         | 01/01/2025 |
| **tipo_acid**| Tipo de acidente                         | Nominal      | Colisão, Atropelamento |
| **regiao**   | Região da cidade                         | Nominal      | Centro, Leste |
| **dia_sem**  | Dia da semana                            | Nominal      | Segunda, Quarta-feira |
| **feridos**  | Número de feridos leves                  | Numérico     | 0, 1, 2, ... |
| **feridos_gr** | Número de feridos graves               | Numérico     | 0, 1, 2, ... |
| **mortes**   | Número de vítimas fatais                 | Numérico     | 0, 1 |
| **latitude** | Coordenada geográfica                    | Numérico     | -30.0476 |
| **longitude**| Coordenada geográfica                    | Numérico     | -51.183 |
| **UPS**      | Unidade Padrão de Severidade (**alvo**)  | Numérico     | 1, 2, 13 |

---

## 🎯 Atributo Alvo e Oportunidades  
O atributo **UPS (Unidade Padrão de Severidade)** representa a gravidade dos acidentes com base em pesos atribuídos aos danos. Ele será utilizado como **variável alvo** em modelos de aprendizado de máquina.  

### Possíveis aplicações:  
- **Classificação ou regressão** da severidade dos acidentes com base em variáveis temporais, espaciais e descritivas.  
- **Análise preditiva de risco**, identificando padrões que levam a acidentes mais graves.  
- **Subsídio a políticas públicas**, orientando campanhas educativas e intervenções em pontos críticos.  
- **Gestão da mobilidade urbana**, priorizando ações que reduzam acidentes fatais e graves.  

---

## 🚀 Conclusão  
Esta fase inicial permitiu compreender a estrutura do dataset e preparar os dados para futuras análises. O uso da variável **UPS** como alvo abre espaço para aplicações práticas em **classificação de severidade, previsão de riscos e formulação de políticas de segurança viária**, transformando dados históricos em conhecimento útil para a sociedade.  

---
