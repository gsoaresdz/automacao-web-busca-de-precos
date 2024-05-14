<h1 align="center">Automação de Busca de Preços na Web</h1>
<p align="center">
  <img alt="Github top language" src="https://img.shields.io/github/languages/top/gsoaresdz/automacao-web-busca-de-precos?color=56BEB8">
  <img alt="Github language count" src="https://img.shields.io/github/languages/count/gsoaresdz/automacao-web-busca-de-precos?color=56BEB8">
  <img alt="Repository size" src="https://img.shields.io/github/repo-size/gsoaresdz/automacao-web-busca-de-precos?color=56BEB8">
  <!--<img alt="License" src="https://img.shields.io/github/license/gsoaresdz/automacao-web-busca-de-precos?color=56BEB8">-->
</p>
<p align="center">
  <a href="#dart-sobre">Sobre</a> &#xa0; | &#xa0; 
  <a href="#sparkles-features">Features</a> &#xa0; | &#xa0;
  <a href="#rocket-tecnologias">Tecnologias</a> &#xa0; | &#xa0;
  <a href="#white_check_mark-requerimentos">Requerimentos</a> &#xa0; | &#xa0;
  <a href="#checkered_flag-execucao">Execução</a> &#xa0; | &#xa0;
  <a href="#memo-licenca">Licença</a> &#xa0; | &#xa0;
  <a href="https://github.com/gsoaresdz" target="_blank">Autor</a>
</p>
<br>

## **:dart: Sobre**

Este projeto consiste em um script Python que automatiza a busca de preços na web e armazena os resultados em um arquivo Excel. O script utiliza as seguintes bibliotecas:

- **pandas:** para manipulação de dados.
- **selenium:** para controlar o navegador e realizar buscas na web.
- **openpyxl:** para trabalhar com arquivos Excel.

## **:memo: IDE e versão do Python**

O script foi desenvolvido no Jupyter Notebook com a versão 3.8 do Python.

## **:memo: Regra de negócio**

O script funciona da seguinte forma:

1. Importa o arquivo Excel com os produtos a serem pesquisados.
2. Abre o navegador e realiza buscas nos sites especificados.
3. Coleta os preços dos produtos e armazena os resultados em um arquivo Excel.

## **:memo: Passos executados no código**

O código é dividido em duas partes principais:

- Importação de Arquivo Excel
- Automação de Busca de Preços

## **:memo: Importação de Arquivo Excel**

A primeira parte do código importa o arquivo Excel com os produtos a serem pesquisados. O arquivo deve ter as seguintes colunas:

- **Produto:** nome do produto.
- **URL:** URL da página de busca do produto.

O código utiliza a biblioteca pandas para importar o arquivo Excel. O código a seguir mostra como importar o arquivo:

```python
python
produtos_df = pd.read_excel('buscas.xlsx')
```

## **:sparkles: Features**

A segunda parte do código automatiza a busca de preços para os produtos do arquivo Excel. O código funciona da seguinte forma:

:heavy_check_mark: **Feature 1**: Abre o navegador e acessa as URLs especificadas.

:heavy_check_mark: **Feature 2**: Coleta os preços dos produtos nas páginas acessadas.

:heavy_check_mark: **Feature 3**: Armazena os resultados em um arquivo Excel.\

O código a seguir mostra como realizar uma busca e coletar o preço:

```python
python
from selenium import webdriver
from selenium.webdriver.common.by import By
import pandas as pd

# Configurar o webdriver
navegador = webdriver.Chrome()

# Loop para acessar cada URL e coletar os preços
for i in range(len(produtos_df)):
    produto = produtos_df.loc[i, 'Produto']
    url = produtos_df.loc[i, 'URL']
    navegador.get(url)
    preco = navegador.find_element(By.CLASS_NAME, 'price').text  # Exemplo de classe de preço
    produtos_df.loc[i, 'Preco'] = preco

# Salvar os resultados em um novo arquivo Excel
produtos_df.to_excel('Ofertas.xlsx', index=False)
```

## **:rocket: Tecnologias**

As seguintes ferramentas foram usadas neste projeto:

- [Python](https://www.python.org/)
- [Jupyter](https://jupyter.org/)
- [Selenium](https://www.selenium.dev/)
- Pandas
- [Openpyxl](https://openpyxl.readthedocs.io/)

## **:white_check_mark: Requerimentos**

Antes de iniciar :checkered_flag:, você precisa ter [Git](https://git-scm.com/) e [Python](https://www.python.org/) instalados.

## **:checkered_flag: Execução**

```bash
bash
# Clone do projeto
$ git clone https://github.com/gsoaresdz/automacao-web-busca-de-precos.git

# Acesse o diretório do projeto
$ cd automacao-web-busca-de-precos

# Instale as dependências
$ pip install -r requirements.txt

# Execute o script
$ jupyter notebook main.ipynb
```

## **:memo: Observações**

- O script foi desenvolvido para fins educacionais. Não é recomendado o uso do script para fins comerciais sem autorização dos sites.
- O script pode ser modificado para atender a diferentes necessidades. Por exemplo, é possível alterar a classe de preço ou incluir novas funcionalidades.

## **:memo: Licença**

Este projeto está sob licença do MIT. Para obter mais detalhes, consulte o arquivo [LICENSE](LICENSE).

Feito com :heart: by <a href="https://github.com/gsoaresdz" target="_blank">gsoaresdz</a>

&#xa0;

<a href="#top">De volta ao topo</a>
