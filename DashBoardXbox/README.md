# 🎮 Dashboard de Vendas - Gaming Subscriptions

## 📋 Sobre o Projeto
Este repositório contém os dados e a estrutura analítica para um **Dashboard de Vendas de Assinaturas de Jogos**. O objetivo é analisar a performance financeira de diferentes planos de assinatura e serviços adicionais (Add-ons), permitindo a tomada de decisão baseada em dados sobre renovações e upsell.

## 🎯 Perguntas de Negócio (KPIs)
O painel foi projetado para responder às seguintes questões estratégicas:
1. **Performance Anual:** Qual o faturamento total consolidado dos planos anuais?
2. **Retenção:** Qual a proporção de receita vinda de renovações automáticas (*Auto Renewal*) vs. manuais?
3. **Add-ons (EA Play):** Qual o volume financeiro gerado especificamente pelo *Season Pass* da EA Play?
4. **Add-ons (Minecraft):** Qual o volume financeiro gerado pelo *Season Pass* do Minecraft?

## 📊 Estrutura dos Dados
A análise baseia-se em uma tabela fato contendo as seguintes dimensões principais:

| Campo | Descrição |
| :--- | :--- |
| `Subscriber ID` | Identificador único do cliente |
| `Plan` | Categoria da assinatura (*Ultimate, Standard, Core*) |
| `Subscription Type` | Periodicidade (*Monthly, Quarterly, Annual*) |
| `Auto Renewal` | Status da renovação automática (*Yes/No*) |
| `Total Value` | Receita final calculada (Assinatura + Add-ons - Descontos) |

> **Fórmula de Receita:**
> `Total Value` = `Subscription Price` + `EA Play Price` + `Minecraft Price` - `Coupon Value`

## 🎨 Identidade Visual & Design
O dashboard segue uma paleta de cores temática "Gamer/Xbox" para imersão e clareza:

* **Cores Principais:**
    * 🟩 `#9BC848` (Destaque Primário)
    * 🟩 `#22C55E` (Ações Positivas)
* **Interface:**
    * ❇️ `#2AE6B1` & `#5BF6A8` (Menus e Detalhes)
* **Fundo/Neutro:**
    * ⬜ `#E8E6E9` (Área de "Respiro")

## 🚀 Como Reproduzir
1. **Carregar Dados:** Importe o arquivo `Bases.csv` para sua ferramenta de BI (Excel, Power BI, Tableau).
2. **Tratamento:** Assegure que a coluna `Start Date` esteja formatada como data.
3. **Cálculos:** Crie medidas para somar o `Total Value` segmentado por `Auto Renewal` e `Subscription Type`.
4. **Visualização:** Utilize Gráficos de Rosca para proporção de renovação e Barras para comparação de Add-ons.

---
*Projeto desenvolvido para análise de performance de vendas no setor de games.*
