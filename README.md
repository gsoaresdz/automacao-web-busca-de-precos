# **Automação de Busca de Preços no Google Shopping e Buscapé**

O projeto é orientado para simular uma situação em que um profissional da área de compras de uma empresa precisa automatizar a busca por informações de fornecedores e produtos em plataformas online. A automação visa agilizar o processo de coleta de dados, tornando-o mais eficiente.

### **Funcionamento**

1. **Definição de Critérios:**
    - Estabeleça um preço limite para cada produto que deseja monitorar. Esse preço servirá como referência para determinar se um produto está em promoção ou não.
2. **Automação de Busca:**
    - Usando a biblioteca Selenium, o código buscará automaticamente os preços dos produtos selecionados em plataformas online como Google Shopping e Buscapé.
    - Durante a busca, o programa irá filtrar e coletar apenas aqueles produtos que estão dentro de um determinado intervalo de preço (preço máximo e mínimo). O preço mínimo é útil para descartar ofertas que pareçam "boas demais para ser verdade" ou produtos errôneos.
3. **Atualização de Dados:**
    - Os preços coletados e os produtos correspondentes serão então organizados e atualizados em uma planilha para fácil visualização.
4. **Notificação por E-mail:**
    - Se algum produto estiver sendo oferecido por um preço abaixo do limite estabelecido, o programa enviará automaticamente um e-mail com uma lista desses produtos, seus preços e links para compra.
    - No contexto deste projeto, usarei um e-mail para execução, no código escolher o seu para devida utilidade. No entanto, recomenda-se que os usuários configurem sua própria conta de e-mail para testes.

### **Alternativas**

Embora a automação web seja uma solução robusta, outra abordagem seria o uso de APIs (Application Programming Interfaces), se disponível, das plataformas de compras. As APIs podem oferecer uma maneira mais direta e eficiente de acessar os dados desejados sem a necessidade de automação web.

### **Recursos Fornecidos**

Este projeto oferece uma **Planilha de Buscas**, que contém:

- Nomes dos produtos.
- Preço máximo e mínimo para cada produto.
- Termos que devem ser evitados durante a busca. Esses termos ajudam a refinar os resultados, garantindo que você obtenha informações precisas e relevantes.

### **Tarefas a Serem Executadas**

1. Automatizar a busca por cada produto listado na planilha no Google Shopping.
2. Repetir o processo para o Buscapé.
3. Se os produtos dentro dos critérios forem encontrados, enviar um e-mail contendo uma lista dos itens, seus preços e links de compra.

Ao finalizar todas as etapas, você terá um sistema que facilitará significativamente o processo de monitoramento e compra de produtos, permitindo que você reaja rapidamente a promoções e obtenha os melhores negócios disponíveis.

## **Bibliotecas Utilizadas**

- Selenium: Para automação web e interação com os sites.
- Pandas: Para manipulação e análise dos dados coletados.
- re: Para expressões regulares.
- time: Para gerenciar o tempo de espera durante a automação.
- smtplib: Para envio de emails.
- MIME: Para formatar emails.

## **Pré-requisitos**

### **Instalando o Python**

O Python é uma linguagem de programação interpretada, de alto nível e propósito geral.

1. Acesse o **[site oficial do Python](https://www.python.org/downloads/)**.
2. Baixe a versão mais recente do Python para o seu sistema operacional.
3. Execute o instalador e siga as instruções na tela. Certifique-se de marcar a opção "Add Python to PATH" durante a instalação.

### **Instalando o Jupyter Notebook**

O Jupyter Notebook é uma aplicação web open-source que permite criar e compartilhar documentos contendo código ativo, equações, visualizações e texto narrativo.

1. Instale o Jupyter usando pip:

```bash
pip install notebook
```

1. Para iniciar o Jupyter Notebook, abra o terminal ou prompt de comando e digite:

```bash
jupyter notebook
```

Isso abrirá uma nova aba no seu navegador padrão com a interface do Jupyter Notebook.

### **Configuração**

1. Certifique-se de ter o ChromeDriver instalado e configurado em seu PATH para que o Selenium funcione corretamente com o navegador Chrome.
2. Instale todas as bibliotecas mencionadas acima usando pip.

## **Como usar**

Execute o arquivo **`main.ipynb`** em um ambiente Jupyter Notebook.
