# O cenário nacional da educação especial no Brasil (2015–2025)

Neste trabalho, comparamos as matrículas da educação especial em **2015, 2020 e 2025**. Primeiro, olhamos a participação no total da educação básica e como as matrículas se dividem por categoria, etapa de ensino e rede. Depois, comparamos a inclusão em classes comuns entre as regiões e os estados. Também comparamos a participação da educação especial nas matrículas de 2025 com os percentuais de deficiência e diagnóstico de autismo do Censo Demográfico de 2022.

**Alunos** — Ian Luca Marinho Aguiar, João Pedro Menezes Barros Dantas de Souza e Davi da Cunha Ribeiro.

- [Notebook final com as sete perguntas](Trabalho_A2%20-%20AEDV%20%283%29.ipynb)
- [Proposta do trabalho](Projeto%20e%20proposta/Proposta_Educacao_Especial_Brasil.pdf)
- [Enunciado do projeto](Projeto%20e%20proposta/AED20262_projeto.pdf)

## Fontes

- Usamos as três edições do Inep para comparar as matrículas. [Sinopses Estatísticas da Educação Básica de 2015, 2020 e 2025](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/sinopses-estatisticas/educacao-basica)
- Na pergunta 6, usamos os percentuais por estado da Tabela 3 (p. 35) e do Gráfico 18 (p. 67). [Censo Demográfico 2022 — IBGE](https://www.ibge.gov.br/biblioteca/visualizacao/livros/liv102178.pdf)

## Como rodar o notebook

1. Abra o terminal na pasta do notebook. Com Python 3.12, rode os comandos abaixo para instalar as bibliotecas e abrir o JupyterLab.

   ```sh
   python -m pip install -r requirements.txt
   python -m jupyterlab
   ```

2. Para rodar as perguntas 1 a 3, baixe as três planilhas do Inep e coloque-as na pasta do notebook. O [guia de requisitos e dados](requirements.md) mostra o nome de cada arquivo.
3. Abra o notebook no JupyterLab e execute a célula **IMPORTAÇÕES**. Depois, rode as células de cada pergunta na ordem. Se você quiser começar pela pergunta 4, pode seguir para ela mesmo que apareça o aviso sobre as planilhas das perguntas 1 a 3.

Antes das perguntas 4, 5 e 7, precisamos rodar um comando separado. Clique com o botão direito no notebook e escolha **New Console for Notebook**. Esse console usa as mesmas variáveis do notebook. Rode cada comando com **Shift+Enter** e volte ao notebook para executar as células da pergunta.

**Pergunta 4.** Colocamos o nome do arquivo em `caminho`, que é a variável usada na leitura do CSV.

```python
caminho = "pergunta4_dados_limpos_inep.csv"
```

**Pergunta 5.** Carregamos a planilha de novo porque as perguntas anteriores já usaram a variável `dados`.

```python
arquivo = pd.ExcelFile("base_limpa_pergunta5_inep_2015_2020_2025.xlsx")
dados = pd.read_excel(arquivo, sheet_name="Base limpa", header=3)
```

**Pergunta 7.** Importamos o NumPy como `np` para calcular a reta do gráfico de dispersão.

```python
import numpy as np
```
