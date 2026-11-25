# Requisitos e dados

## Bibliotecas

Usamos pandas para ler e organizar as tabelas, Plotly e Matplotlib para fazer os gráficos e IPython para exibir as tabelas no notebook. O pandas usa openpyxl para abrir os arquivos `.xlsx`. Na pergunta 7, usamos NumPy para calcular a reta do gráfico de dispersão.

As bibliotecas e o JupyterLab estão no [requirements.txt](requirements.txt). O [README](README.md) mostra como instalar e rodar o notebook.

## Planilhas do Inep

As perguntas 1 a 3 leem as três planilhas abaixo. Baixe o ZIP de cada ano e coloque o arquivo `.xlsx` na mesma pasta do notebook. O notebook procura os arquivos pelos nomes da tabela. [Sinopses Estatísticas da Educação Básica](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/sinopses-estatisticas/educacao-basica)

| Ano | Nome do arquivo que o notebook procura | Abas usadas |
| --- | --- | --- |
| [2015](https://download.inep.gov.br/informacoes_estatisticas/sinopses_estatisticas/sinopses_educacao_basica/sinopse_estatistica_da_educacao_basica_2015.zip) | `Sinopse_Estatistica_da_Educação_Basica_2015.xlsx` | `Educação Básica 1.1`, `Educação Especial 1.38`, `1.43` e `1.49` |
| [2020, edição de 08/03/2021](https://download.inep.gov.br/dados_abertos/sinopses_estatisticas/sinopses_estatisticas_censo_escolar_2020.zip) | `Sinopse_Estatistica_da_Educação_Basica_2020.xlsx` | `Educação Básica 1.1`, `Educação Especial 1.38`, `1.43` e `1.49` |
| [2025, versão 2](https://download.inep.gov.br/dados_abertos/sinopses_estatisticas/sinopse_estatistica_censo_escolar_2025.zip) | `Sinopse_Estatistica_da_Educação_Basica_2025_V2.xlsx` | `Educação Básica 1.1`, `Educação Especial 1.55` e `1.58` |

## Dados das perguntas 4 a 7

- **Pergunta 4.** O CSV tem as matrículas em classes comuns e exclusivas por rede de ensino. Os valores vêm da tabela exibida no [notebook avulso da pergunta 4](Perguntas%20Avulsas/pergunta4_notebook_revisado.ipynb). A análise usa as tabelas 1.40 e 1.46 do Inep em 2015 e 2020 e as tabelas 1.61 e 1.68 em 2025. [Arquivo da pergunta 4](pergunta4_dados_limpos_inep.csv)
- **Pergunta 5.** A aba `Base limpa` reúne os dados das 27 UFs e do Brasil nos três anos. Usamos os totais e as matrículas em classes comuns que já aparecem na pergunta 7. Somamos as UFs para obter os totais do Brasil e subtraímos as matrículas em classes comuns do total para obter as de classes exclusivas. [Arquivo da pergunta 5](base_limpa_pergunta5_inep_2015_2020_2025.xlsx)
- **Pergunta 6.** O notebook já traz as matrículas de 2025 (tabelas 1.1 e 1.55 do Inep) e os percentuais por UF de deficiência e diagnóstico de autismo (Tabela 3 e Gráfico 18). [Censo Demográfico 2022 — IBGE](https://www.ibge.gov.br/biblioteca/visualizacao/livros/liv102178.pdf)
- **Pergunta 7.** Os dados estão no notebook. Usamos as tabelas 1.38 e 1.39 do Inep em 2015 e 2020 e a tabela 1.55 em 2025.
