# Requisitos e dados

## Ambiente Python

Use Python 3.12 e instale os pacotes listados em [requirements.txt](requirements.txt) com `python -m pip install -r requirements.txt`. O [README](README.md) descreve a ordem de execução no JupyterLab.

| Pacote | Uso no trabalho |
| --- | --- |
| JupyterLab e IPython | Execução interativa e exibição de tabelas |
| pandas | Leitura, tratamento e agregação das bases |
| openpyxl | Leitura de arquivos `.xlsx` pelo pandas |
| Plotly e Matplotlib | Visualizações |
| NumPy | Ajuste da reta na dispersão da pergunta 7 |

## Planilhas originais do Inep

Na página das [Sinopses Estatísticas da Educação Básica](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/sinopses-estatisticas/educacao-basica), baixe os arquivos indicados abaixo e extraia a planilha `.xlsx` de cada ZIP. Coloque as três na mesma pasta do notebook final. Se necessário, renomeie cada uma conforme a tabela e preserve os nomes das abas.

| Edição | Nome esperado pelo notebook | Abas lidas nas perguntas 1–3 |
| --- | --- | --- |
| [2015 — ZIP](https://download.inep.gov.br/informacoes_estatisticas/sinopses_estatisticas/sinopses_educacao_basica/sinopse_estatistica_da_educacao_basica_2015.zip) | `Sinopse_Estatistica_da_Educação_Basica_2015.xlsx` | `Educação Básica 1.1`, `Educação Especial 1.38`, `1.43`, `1.49` |
| [2020 — ZIP, edição de 08/03/2021](https://download.inep.gov.br/dados_abertos/sinopses_estatisticas/sinopses_estatisticas_censo_escolar_2020.zip) | `Sinopse_Estatistica_da_Educação_Basica_2020.xlsx` | `Educação Básica 1.1`, `Educação Especial 1.38`, `1.43`, `1.49` |
| [2025 — ZIP, versão 2](https://download.inep.gov.br/dados_abertos/sinopses_estatisticas/sinopse_estatistica_censo_escolar_2025.zip) | `Sinopse_Estatistica_da_Educação_Basica_2025_V2.xlsx` | `Educação Básica 1.1`, `Educação Especial 1.55`, `1.58` |

## Bases tratadas

| Pergunta | Arquivo ou origem dos dados |
| --- | --- |
| 4 | [pergunta4_dados_limpos_inep.csv](pergunta4_dados_limpos_inep.csv). As seis linhas reproduzem a tabela exibida no [notebook avulso da pergunta 4](Perguntas%20Avulsas/pergunta4_notebook_revisado.ipynb). As referências são as tabelas 1.40 e 1.46 do Inep em 2015 e 2020, e 1.61 e 1.68 em 2025. |
| 5 | [base_limpa_pergunta5_inep_2015_2020_2025.xlsx](base_limpa_pergunta5_inep_2015_2020_2025.xlsx). A aba `Base limpa` foi recomposta com os totais e as matrículas em classes comuns por UF da pergunta 7. Os totais nacionais vêm da soma das UFs e as matrículas em classes exclusivas vêm da diferença entre total e classes comuns. O cabeçalho fica na quarta linha. |
| 6 | CSV incorporado no notebook. Usa matrículas do Inep de 2025 (tabelas 1.1 e 1.55) e percentuais preliminares por UF de deficiência e diagnóstico de autismo (Tabela 3 e Gráfico 18). [IBGE — Censo Demográfico 2022](https://www.ibge.gov.br/biblioteca/visualizacao/livros/liv102178.pdf) |
| 7 | CSV incorporado no notebook. A análise usa as tabelas 1.38 e 1.39 de 2015 e 2020 e a tabela 1.55 de 2025 do Inep. |
