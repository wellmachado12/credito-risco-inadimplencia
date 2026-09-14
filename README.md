# Projeto de Inteligência de Dados: Prevenção de Churn e Inadimplência

> Projeto de Parceria Semantix — Solução End-to-End de Análise de Dados e Modelagem Preditiva

---

## 1. Dissertação sobre o Problema

### Descrição Detalhada do Problema

O cancelamento voluntário de clientes (*Churn Rate*) e a alta taxa de inadimplência (*Default*) representam dois dos maiores gargalos operacionais e financeiros em instituições que atuam nos setores financeiro, de telecomunicações e de serviços recorrentes (SaaS).

A perda de clientes e a falta de pagamento não ocorrem de forma aleatória: elas são o resultado final de uma série de atritos, mudanças de perfil socioeconômico e oscilações no engajamento com o produto ou serviço ao longo do tempo. Quando as empresas falham em identificar esses sinais prévios, a perda de receita exige um investimento contínuo e custoso na aquisição de novos clientes para repor a base (*efeito balde furado*).

### Importância e Relevância no Contexto Socioeconômico

Do ponto de vista mercadológico e econômico, manter um cliente atual custa entre **5 a 25 vezes menos** do que adquirir um novo cliente. Além disso, a redução da taxa de perda em apenas 5% pode impactar diretamente o lucro líquido da organização de 25% a 95%, dependendo do segmento de atuação.

No contexto atual de alta competitividade, volatilidade econômica e taxa de juros elevada:

* **Para as Empresas:** A previsibilidade de receita e a preservação do *Customer Lifetime Value* (LTV) garantem a saúde financeira e a capacidade de investimento da organização.
* **Para a Sociedade e Mercado:** A identificação precoce do risco de inadimplência permite renegociações antes do endividamento crítico, promovendo uma concessão de crédito e oferta de serviços mais sustentável.

### Como a Análise de Dados Ajuda a Solucionar ou Mitigar o Problema

A análise de dados atua transformando registros históricos dispersos em inteligência Preditiva e Prescritiva:

* **Identificação de Padrões Ocultos:** Por meio de algoritmos e técnicas estatísticas, é possível mapear quais comportamentos (ex.: queda na frequência de uso, alteração no meio de pagamento, chamados de suporte frequentes ou contratos de curto prazo) possuem alta correlação com o cancelamento ou a inadimplência.
* **Segmentação e Scoring de Risco:** A construção de modelos preditivos permite atribuir uma pontuação contínua de risco (*Credit / Churn Score*) para cada cliente em tempo real.
* **Ações Preventivas e Automatizadas:** Em vez de reagir após o cancelamento ou o atraso, a equipe de negócios passa a atuar de forma proativa, oferecendo incentivos de retenção, renegociações personalizadas e planos adequados ao perfil de cada segmento.

---

## 2. Levantamento das Fontes de Dados e Métodos de Coleta

Para garantir a viabilidade, reprodutibilidade e conformidade com as regras de privacidade e dados não confidenciais, este projeto utiliza fontes públicas de mercado consolidadas para análise de risco de crédito e comportamento de churn.

### Descrição das Fontes de Dados
* **Base de Concessão de Crédito e Inadimplência (Kaggle / Public Repositories):** Conjunto de dados histórico contendo registros transacionais, demográficos e operacionais de clientes.
* **Dados Demográficos e Operacionais:** Mapeamento do perfil dos clientes, incluindo tempo de relacionamento (*tenure*), tipo de contrato, métodos de pagamento e adesão a serviços adicionais.
* **Dados Financeiros:** Registros de receita mensal (*Monthly Charges*), total acumulado (*Total Charges*) e histórico de pagamentos/atrasos.

### Tipos de Dados Disponíveis
* **Estruturados:** Tabelas relacionais nos formatos `.csv` e `.parquet`, compostas por variáveis categóricas (ex.: tipo de contrato, status de churn, método de pagamento) e variáveis numéricas contínuas/discretas (ex.: valor cobrado, pontuação de score, meses de contrato).

### Métodos de Acesso e Coleta
* **Coleta via API / Download Direto:** Ingestão dos arquivos brutos diretamente de repositórios públicos via scripts em **Python**.
* **Pipeline de Ingestão:** Utilização das bibliotecas `Pandas` para estruturação inicial em memória e `PySpark` para leitura e processamento distribuído de volumes maiores de dados.
