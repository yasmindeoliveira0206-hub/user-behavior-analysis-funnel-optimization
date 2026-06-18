# TripleTen Sprint 10: Análise de Comportamento do Usuário e Otimização de Funil 🛒🚀

Este repositório contém o projeto final da décima sprint do curso de Análise de Dados da TripleTen. O foco deste projeto foi a **Análise de Comportamento do Usuário**, onde atuei como analista para uma startup que vende produtos alimentares. O objetivo foi entender a jornada do cliente, identificar gargalos no funil de vendas e avaliar os resultados de um experimento de design (Teste A/A/B).

## 📋 Contexto do Negócio
A startup quer melhorar sua taxa de conversão. Para isso, analisamos os logs de eventos dos usuários para construir um funil de vendas e entender em qual etapa os clientes desistem. Além disso, avaliamos um teste A/B realizado para testar uma nova fonte para o aplicativo, comparando-a com o design atual através de dois grupos de controle (A/A) e um grupo de teste (B).

## 🛠️ Tecnologias e Ferramentas
*   **Python 3.x**
*   **Pandas:** Limpeza, transformação e agregação de dados de eventos.
*   **Plotly:** Criação de gráficos interativos e visualização detalhada do funil de vendas.
*   **SciPy (stats):** Realização de testes de proporção (Z-test) para validar a significância estatística do teste A/A/B.

## 🚀 Desafios Técnicos Superados
Este projeto envolveu uma análise profunda de eventos e rigor estatístico:
*   **Processamento de Dados de Eventos:**
    *   Tratamento de tipos de dados e extração de datas e horas dos logs.
    *   Filtragem de dados incompletos para garantir uma análise justa (período estável).
*   **Análise do Funil de Vendas:**
    *   Identificação da sequência de eventos: `MainScreenAppear` -> `OffersScreenAppear` -> `CartScreenAppear` -> `PaymentScreenSuccessful`.
    *   Cálculo da taxa de retenção entre cada etapa e identificação do ponto de maior perda de usuários (da tela principal para a tela de ofertas).
*   **Análise de Teste A/A/B:**
    *   Validação do teste A/A para garantir que os grupos de controle são estatisticamente idênticos.
    *   Comparação de cada grupo de controle individualmente com o grupo de teste e, posteriormente, do grupo de controle combinado com o grupo de teste.
    *   Aplicação da **Correção de Bonferroni** para lidar com o problema das múltiplas comparações e evitar falsos positivos.

## 📊 Principais Insights
*   Descoberta de que apenas 47% dos usuários que chegam à tela principal avançam para ver as ofertas.
*   Confirmação de que, uma vez que o usuário chega à tela de pagamento, a taxa de sucesso é altíssima (mais de 95%).
*   Resultado do Experimento: A mudança na fonte não alterou significativamente o comportamento dos usuários, permitindo que a equipe de design tome uma decisão segura sobre a implementação ou não da alteração.

## 📁 Estrutura do Repositório
*   `notebook.ipynb`: O notebook Jupyter com todo o processo de limpeza, análise de funil e testes estatísticos.
*   `README.md`: Este arquivo com a apresentação do projeto.

---
*Este projeto faz parte da minha formação como Analista de Dados na TripleTen Brasil.*
