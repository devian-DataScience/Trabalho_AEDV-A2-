# Educação especial no Brasil (2015–2025)

Trabalho final de Análise Exploratória de Dados e Visualização da FGV EMAp. O projeto investiga a evolução das matrículas da educação especial em **2015, 2020 e 2025**. As sete perguntas passam pela participação no total da educação básica, pelo perfil das matrículas e pela distribuição por etapa de ensino e rede. A análise também compara a inclusão em classes comuns entre regiões e UFs e relaciona os indicadores de matrícula de 2025 aos percentuais de deficiência e diagnóstico de autismo do Censo Demográfico de 2022.

**Integrantes** — Ian Luca Marinho Aguiar, João Pedro Menezes Barros Dantas de Souza e Davi da Cunha Ribeiro.

- [Notebook final com as sete perguntas](Trabalho_A2%20-%20AEDV%20%283%29.ipynb)
- [Proposta do trabalho](Projeto%20e%20proposta/Proposta_Educacao_Especial_Brasil.pdf)
- [Enunciado do projeto](Projeto%20e%20proposta/AED20262_projeto.pdf)

## Fontes

- **Inep.** As Sinopses Estatísticas da Educação Básica de 2015, 2020 e 2025 fornecem os dados de matrículas. [Sinopses Estatísticas da Educação Básica](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/sinopses-estatisticas/educacao-basica)
- **IBGE.** A pergunta 6 usa os percentuais por UF da Tabela 3 (p. 35) e do Gráfico 18 (p. 67). [Censo Demográfico 2022 — Pessoas com deficiência e pessoas diagnosticadas com transtorno do espectro autista](https://www.ibge.gov.br/biblioteca/visualizacao/livros/liv102178.pdf)

## Como executar

Clone ou baixe o repositório e abra um terminal na pasta que contém o notebook final. Com Python 3.12, crie um ambiente virtual e instale as dependências.

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m jupyterlab
```

No Windows com PowerShell, use `.\.venv\Scripts\Activate.ps1` no lugar de `source .venv/bin/activate`.

Para as perguntas 1–3, extraia as três planilhas do Inep na pasta do notebook, com a grafia indicada no [guia de requisitos e dados](requirements.md). Os arquivos tratados das perguntas 4 e 5 estão na raiz do repositório. As perguntas 6 e 7 já contêm suas bases no notebook.

Abra o notebook no JupyterLab com o kernel Python 3. Clique com o botão direito no notebook e selecione **New Console for Notebook** para abrir um console que compartilha o mesmo kernel. No console, use **Shift+Enter** para executar cada comando abaixo. Volte ao notebook para executar as células de cada pergunta na ordem.

1. Execute a célula **IMPORTAÇÕES**. Com as três planilhas do Inep na pasta, execute também as perguntas 1–3. Para começar pela pergunta 4, siga após **IMPORTAÇÕES**, mesmo que apareça o aviso de falta dessas planilhas.
2. Antes da primeira célula da pergunta 4, informe no console o caminho que a seção espera.

   ```python
   caminho = "pergunta4_dados_limpos_inep.csv"
   ```

3. Antes da primeira célula da pergunta 5, recarregue a planilha no console. As seções anteriores reutilizam a variável `dados`.

   ```python
   dados = pd.read_excel(
       "base_limpa_pergunta5_inep_2015_2020_2025.xlsx",
       sheet_name="Base limpa",
       header=3,
   )
   ```

4. Execute a pergunta 6. Antes de executar a pergunta 7, importe NumPy no console.

   ```python
   import numpy as np
   ```
