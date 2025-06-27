# Projeto: Análise de Evasão de Clientes - Telecom X

## 📊 Visão Geral do Projeto

Este projeto tem como objetivo principal analisar e compreender os fatores que contribuem para a evasão de clientes (Churn) na **Telecom X**, uma empresa fictícia do setor de telecomunicações. A evasão de clientes é um desafio crítico para empresas de serviços, impactando diretamente a receita e a sustentabilidade do negócio.

Através de um processo completo de **ETL (Extração, Transformação e Carga)** e **Análise Exploratória de Dados (EDA)**, buscamos identificar padrões, perfis de clientes de risco e insights acionáveis que possam embasar estratégias para reduzir a taxa de churn.

## 🎯 Objetivo da Análise

  * **Identificar:** Quais são as características e o comportamento dos clientes que tendem a cancelar os serviços.
  * **Quantificar:** A proporção de clientes que evadem da Telecom X.
  * **Propor:** Recomendações baseadas em dados para ajudar a equipe de Data Science a desenvolver modelos preditivos e a área de negócios a criar estratégias de retenção eficazes.

## ⚙️ Estrutura do Projeto

O projeto está organizado em um pipeline de análise de dados, conforme as etapas de ETL e EDA:

1.  **Extração de Dados:** Obtenção dos dados brutos de uma API.
2.  **Limpeza e Transformação de Dados:** Tratamento de inconsistências, padronização, criação de novas variáveis e preparação do dataset.
3.  **Análise Exploratória de Dados (EDA):** Análise descritiva e visualização para identificar padrões e insights.
4.  **Conclusões e Recomendações:** Consolidação dos achados e sugestões para ações futuras.

## 🛠️ Tecnologias e Dependências

Este projeto foi desenvolvido utilizando **Python** e as seguintes bibliotecas:

  * **`pandas`**: Para manipulação e análise de dados tabulares (DataFrames).
  * **`numpy`**: Para operações numéricas e tratamento de valores especiais (NaN).
  * **`requests`**: Para fazer requisições HTTP e extrair dados da API.
  * **`matplotlib`**: Para a criação de visualizações estáticas.
  * **`seaborn`**: Para a criação de visualizações estatísticas mais atraentes e informativas.

## 🚀 Como Executar o Projeto

O projeto foi desenvolvido em um ambiente de notebook (preferencialmente Google Colab ou Jupyter Notebook) para facilitar a execução sequencial das etapas e a visualização dos resultados.

1.  **Clone este repositório** (se aplicável, ou faça o download dos arquivos do projeto).
2.  **Abra o notebook** (`.ipynb`) em seu ambiente Python preferido (Google Colab, Jupyter Notebook, VS Code).
3.  **Execute as células em ordem.** O notebook está estruturado para seguir o fluxo ETL e EDA:
      * **Célula de Importação:** Carrega as bibliotecas necessárias e define a URL da API.
      * **Célula de Extração e Achatamento:** Realiza a requisição à API e transforma os dados JSON aninhados em um DataFrame tabular (esse é um passo crucial para evitar erros de tipo).
      * **Células de Limpeza e Transformação:** Aplicam todas as etapas de tratamento de dados (conversão de tipos, padronização de valores, renomeamento de colunas, criação da coluna `Cobrancas_Diarias`, remoção de duplicatas).
      * **Células de Análise Descritiva e Visualizações:** Geram as estatísticas e os gráficos para a EDA.
      * **Célula de Relatório Final:** Contém este resumo das análises e conclusões.

## 📂 Dados

Os dados utilizados neste projeto são obtidos de uma API disponível no GitHub:
`https://raw.githubusercontent.com/alura-cursos/challenge2-data-science/main/TelecomX_Data.json`

O dataset contém informações sobre clientes de uma empresa de telecomunicações, incluindo detalhes do serviço, cobranças, informações demográficas e, crucialmente, se o cliente "evadiu" (`Churn`).

## 📈 Análise Exploratória de Dados (EDA) - Principais Insights

A EDA revelou padrões significativos sobre o comportamento de evasão:

  * **Taxa de Evasão:** A Telecom X enfrenta uma taxa de churn considerável, evidenciando a necessidade urgente de estratégias de retenção.
  * **Contratos de Curto Prazo:** Clientes com contratos mensais são o segmento de maior risco, apresentando uma taxa de evasão significativamente mais alta em comparação com aqueles que possuem contratos anuais ou bienais.
  * **Serviços de Internet (Fibra Óptica):** Clientes com serviço de fibra óptica parecem ter uma taxa de evasão mais elevada. Isso sugere a importância de investigar a qualidade ou o custo percebido desse serviço.
  * **Impacto de Serviços Adicionais:** A ausência de serviços adicionais como segurança online e suporte técnico está correlacionada com uma maior propensão à evasão, indicando que esses serviços contribuem para a satisfação e a "adesão" do cliente.
  * **Métodos de Pagamento:** Clientes que utilizam "cheque eletrônico" como método de pagamento demonstram uma taxa de evasão superior, o que pode indicar atritos no processo de pagamento ou um perfil de cliente de maior risco.
  * **Meses de Contrato (Tenure):** Os clientes com menor tempo de contrato são os mais vulneráveis ao churn. Os primeiros meses são um período crítico para a retenção.
  * **Cobrancas Mensais e Totais:** Tanto clientes com baixas cobranças mensais (que podem não ver valor nos serviços básicos) quanto aqueles com cobranças mais altas (potencialmente sensíveis ao preço) podem apresentar maior taxa de evasão.

## 💡 Conclusões e Recomendações

A análise demonstra que a evasão de clientes na Telecom X é um problema multifacetado, influenciado por fatores contratuais, de serviço, de pagamento e de tempo de permanência.

**Recomendações para Redução da Evasão:**

1.  **Foco nos Primeiros Meses:** Implementar programas de *onboarding* e acompanhamento proativos para novos clientes, especialmente nos primeiros 3 a 6 meses de contrato, oferecendo suporte e incentivando a exploração dos serviços.
2.  **Incentivos para Contratos Mais Longos:** Desenvolver ofertas e benefícios atraentes para clientes que optam por migrar de contratos mensais para planos anuais ou bienais.
3.  **Melhoria e Comunicação do Serviço de Fibra Óptica:** Investigar as razões da insatisfação dos clientes de fibra óptica e otimizar a experiência ou a comunicação de valor para este segmento.
4.  **Promoção de Serviços Agregadores:** Criar campanhas direcionadas para promover os benefícios da segurança online, backup e suporte técnico, mostrando como esses serviços melhoram a experiência do cliente.
5.  **Otimização de Métodos de Pagamento:** Analisar e aprimorar a experiência de pagamento via cheque eletrônico. Considerar incentivar o uso de métodos de pagamento mais automatizados e de menor atrito.
6.  **Segmentação para Campanhas de Retenção:** Utilizar o perfil de cliente de alto risco identificado (e.g., contrato mensal, fibra óptica, sem adicionais, cheque eletrônico, poucos meses de contrato) para criar campanhas de retenção altamente personalizadas.
