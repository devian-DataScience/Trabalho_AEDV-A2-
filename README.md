# O cenário nacional da educação especial no Brasil (2015–2025)

Neste trabalho, comparamos as matrículas da educação especial em **2015, 2020 e 2025**. Primeiro, olhamos a participação no total da educação básica e como as matrículas se dividem por categoria, etapa de ensino e rede. Depois, comparamos a inclusão em classes comuns entre as regiões e os estados. Também comparamos a participação da educação especial nas matrículas de 2025 com os percentuais de deficiência e diagnóstico de autismo do Censo Demográfico de 2022.

**Alunos** — Ian Luca Marinho Aguiar, João Pedro Menezes Barros Dantas de Souza e Davi da Cunha Ribeiro.

## Arquivos do trabalho

- [Notebook final com as sete perguntas](Trabalho_A2%20-%20AEDV%20%283%29.ipynb)
- [Declaração de contribuições](CONTRIBUICOES.md)
- [Proposta do trabalho](Projeto%20e%20proposta/Proposta_Educacao_Especial_Brasil.pdf)
- [Enunciado do projeto](Projeto%20e%20proposta/AED20262_projeto.pdf)
- [Perguntas avulsas como material complementar](Perguntas%20Avulsas/)

## Como rodar o notebook

1. Abra o terminal na pasta do notebook. Com Python 3.12, rode os comandos abaixo para instalar as bibliotecas e abrir o JupyterLab.

   ```sh
   python -m pip install -r requirements.txt
   python -m jupyterlab
   ```

2. Baixe e extraia as três planilhas do Inep. Coloque os arquivos `.xlsx` na mesma pasta do notebook, com os nomes indicados no guia. [Requisitos e dados](exp-requisitos.md)
3. Abra o notebook final no JupyterLab. No menu **Kernel**, escolha **Restart Kernel and Run All Cells** para rodar as sete perguntas em ordem.

Para rodar apenas as perguntas 4 a 7, execute a célula **IMPORTAÇÕES** e siga a partir da pergunta 4. O CSV e a planilha usados nas perguntas 4 e 5 já estão no repositório. As perguntas 6 e 7 trazem os dados no próprio notebook.

## Fontes

- Comparamos os dados de matrícula das três edições do Inep. [Sinopses Estatísticas da Educação Básica de 2015, 2020 e 2025](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/sinopses-estatisticas/educacao-basica)
- Na pergunta 6, usamos os percentuais por estado da Tabela 3 (p. 35) e do Gráfico 18 (p. 67). [Censo Demográfico 2022 — IBGE](https://www.ibge.gov.br/biblioteca/visualizacao/livros/liv102178.pdf)
