# 🎮 Dashboard de Vendas e Assinaturas – Xbox Game Pass (Excel)

Projeto desenvolvido como entrega de desafio prático de análise e visualização de dados no Microsoft Excel. O objetivo é transformar dados brutos de assinaturas em um painel gerencial claro, dinâmico e orientado à tomada de decisão.

![Preview do Dashboard](<img width="1254" height="443" alt="dashxbox" src="https://github.com/user-attachments/assets/c1c04212-a0b8-4295-81c5-adeccd948de3" />)
![Preview do Dashboard](<img width="1318" height="257" alt="image" src="https://github.com/user-attachments/assets/08051a8a-2fae-497f-a25e-1d203660f071" />)

---

## 🎯 Objetivo do Projeto

Organizar uma base de vendas de assinaturas do Xbox Game Pass e construir um dashboard interativo no Excel capaz de responder a perguntas-chave de negócio sobre:

- Evolução mensal de aquisição de assinantes e receita;
- Desempenho financeiro por plano (`Ultimate`, `Standard` e `Core`);
- Peso dos add-ons (`EA Play Season Pass` e `Minecraft Season Pass`) na receita;
- Impacto dos cupons de desconto sobre a receita bruta;
- Taxa de renovação automática por modalidade de cobrança (`Mensal`, `Trimestral` e `Anual`).

---

## 📊 Base de Dados Utilizada

Os dados estão estruturados na aba **`Bases`** em formato de Tabela do Excel (`Tabela1`), contendo **295 registros de assinantes** no período de **01/01/2024 a 16/12/2024** *(dezembro parcial)*.

| Coluna | Descrição |
| :--- | :--- |
| `Subscriber ID` | Identificador único do assinante |
| `Name` | Nome do cliente |
| `Plan` | Plano contratado (`Core`, `Standard` ou `Ultimate`) |
| `Start Date` | Data de início da assinatura |
| `Auto Renewal` | Indica se a renovação automática está ativa (`Yes` / `No`) |
| `Subscription Price` | Valor base do plano (Core: R$ 5, Standard: R$ 10, Ultimate: R$ 15) |
| `Subscription Type` | Periodicidade da cobrança (`Monthly`, `Quarterly`, `Annual`) |
| `EA Play Season Pass` / `Price` | Adesão e valor do add-on EA Play (R$ 30) |
| `Minecraft Season Pass` / `Price` | Adesão e valor do add-on Minecraft (R$ 20) |
| `Coupon Value` | Valor do desconto aplicado via cupom |
| `Total Value` | Receita líquida final da assinatura |

---

## 🗂️ Estrutura da Planilha (`dashboard_xbox.xlsx`)

1. **`Assets`**: Paleta de cores inspirada na identidade visual do Xbox (`#9BC848`, `#22C55E`, `#2AE6B1`, `#5BF6A8`, `#E8E6E9`) e elementos gráficos utilizados no layout.
2. **`Bases`**: Base bruta formatada como tabela estruturada (`Tabela1`), garantindo atualização automática de todas as fórmulas ao inserir novos registros.
3. **`Cálculos`**: Memória de cálculo totalmente dinâmica com `SUMIFS`, `COUNTIFS`, `AVERAGEIFS`, `INDEX/MATCH` e conciliação automática da receita, dividida em:
   - KPIs principais;
   - Evolução mensal (novos assinantes, receita líquida, acumulada e ticket médio);
   - Desempenho por plano;
   - Tipo de assinatura x renovação automática;
   - Composição da receita bruta e líquida;
   - Textos de insights gerados dinamicamente por fórmulas.
4. **`Dashboard`**: Painel executivo com 6 cartões de KPIs, painel de insights automáticos e 5 gráficos:
   - *Evolução Mensal – Novos Assinantes x Receita Líquida*
   - *Receita Líquida por Plano*
   - *Composição da Receita Bruta (R$)*
   - *Assinantes por Tipo x Renovação Automática*
   - *Receita Líquida x Descontos em Cupons por Plano*

---

## 📈 Principais KPIs e Insights

| Indicador | Resultado |
| :--- | :---: |
| **Total de Assinantes** | 295 |
| **Receita Bruta** | R$ 9.755 |
| **Descontos em Cupons** | R$ 2.122 (21,8% da receita bruta) |
| **Receita Líquida** | R$ 7.633 |
| **Ticket Médio** | R$ 25,87 |
| **Taxa de Renovação Automática** | 50,2% |
| **Participação de Add-ons na Receita Bruta** | 69,9% |

**Destaques da análise:**
- **Liderança de receita no Ultimate:** Apesar de os três planos terem volumes semelhantes de clientes (Ultimate: 98, Standard: 96, Core: 101), o **Ultimate gera 70,6% da receita líquida (R$ 5.388)**, com ticket médio de **R$ 54,98** — 12,5x maior que o Core (R$ 4,40).
- **Força dos Add-ons:** `Minecraft Season Pass` (39,8%) e `EA Play Season Pass` (30,1%) representam **69,9% da receita bruta**, pois acompanham a estrutura dos planos superiores.
- **Atenção aos cupons no Standard:** 83% da base utilizou cupom, mas o plano **Standard perde 37,5% de sua receita bruta em descontos** (R$ 1.079), indicando espaço para revisão da política promocional.
- **Risco de churn no plano Mensal:** A modalidade mensal concentra **47,1% dos assinantes**, porém apresenta apenas **20,1% de renovação automática**, contra **70,6% no Trimestral** e **84,5% no Anual**.

---

## 🚀 Como Reproduzir / Utilizar

1. Faça o download do arquivo [`dashboard_xbox.xlsx`](./dashboard_xbox.xlsx) ou clone este repositório:
   ```bash
   git clone [https://github.com/SEU-USUARIO/dashboard-vendas-xbox-excel.git](https://github.com/SEU-USUARIO/dashboard-vendas-xbox-excel.git)
