# Análise de Vendas e Desempenho Gerencial

Análise de vendas de produtos tecnológicos por loja e região, comparando o faturamento mensal de cada loja com a meta do respectivo gerente. Projeto em Python (pandas) desenvolvido em Jupyter Notebook.

## Objetivo

O notebook responde a três perguntas de negócio:

1. Qual região teve o maior faturamento?
2. Cada gerente atingiu a meta mensal da loja sob sua responsabilidade?
3. Qual foi o produto mais vendido (em unidades) em cada região?

## Principais resultados

| Região   | Faturamento total   |
| -------- | ------------------- |
| Sudeste  | R$ 126.100.300,00   |
| Nordeste | R$ 84.491.000,00    |
| Sul      | R$ 82.800.180,00    |

- **Maior faturamento:** Sudeste. As vendas online ficaram fora do ranking, já que não representam uma região geográfica.
- **Metas dos gerentes:** os 7 gerentes atingiram a meta em todos os 24 meses analisados (168 de 168 combinações gerente-mês).
- **Produto mais vendido por região (unidades):**
  - Nordeste: Notebook HP (5.436)
  - Sudeste: Monitor 27" (8.219)
  - Sul: Teclado Mecânico (5.340)

## Dados

| Arquivo               | Conteúdo                                                                 |
| --------------------- | ------------------------------------------------------------------------ |
| `vendas_tech.csv`     | Registros de vendas: pedido, data, loja, produto, preço unitário, quantidade e cliente (100.100 linhas brutas, 100.000 após a limpeza) |
| `gerentes_lojas.xlsx` | Cadastro de gerentes: loja, gerente e meta mensal de faturamento (7 lojas) |

Valores ausentes na coluna `Loja` correspondem a vendas online, conforme orientação recebida da equipe.

## Tratamento dos dados

- Conversão da coluna `Data` para `datetime`.
- Padronização dos nomes das lojas (espaços e maiúsculas/minúsculas) e preenchimento dos valores ausentes com `Online`.
- Remoção da coluna `Data_Base`, que tinha 99,999% de valores nulos e não era necessária para a análise.
- Remoção de 100 registros duplicados (critério: repetição de `ID_Pedido` + `Cliente`).
- Criação de colunas derivadas: `Faturamento` (`Preco_Unitario * Qtd`), `Regiao` (a partir da loja) e `Forma_de_venda` (Online ou Presencial).

## Ferramentas

Python, pandas, NumPy, openpyxl e Jupyter Notebook.

## Como rodar

```bash
git clone https://github.com/Nanashbom/Sales-management-analysis.git
cd Sales-management-analysis
pip install -r requirements.txt
jupyter notebook
```

Abra o notebook em `notebooks/` e execute as células na ordem (**Kernel → Restart & Run All**). Os arquivos de dados precisam estar na pasta indicada na primeira célula do notebook.

## Estrutura do repositório

```
├── notebooks/       # notebook da análise
├── data/            # vendas_tech.csv e gerentes_lojas.xlsx
├── resultados/      # tabelas exportadas (.csv)
├── requirements.txt
└── README.md
```

## Arquivos gerados

- `faturamento_por_regiao.csv`
- `resultado_metas_gerentes_mensal.csv` e `resumo_metas_gerentes.csv`
- `resultado_produto_mais_vendido_por_regiao.csv`

## Autor

**Robert Nathan**, [github.com/Nanashbom](https://github.com/Nanashbom)