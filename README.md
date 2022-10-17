# Fundamentos-DS
Repositório para a disciplina de fundamentos de ciência de dados

### Professores:

Sergio Serra                  | Jorge Zavaleta
------------------------------|--------------------------------|
[serra@pet-si.ufrrj.br](mailto:serra@pet-si.ufrrj.br) | [zavaleta@pet-si.ufrrj.br](zavaleta@pet-si.ufrrj.br)

### Alunos:

- [Alex Santos](https://github.com/AlexSantoss)
- [Anderson Neto](https://github.com/AndersonNetoSilva)
- [Douglas Castro](https://github.com/DouglasRenatoUFRJ)

## Dependências

#### É necessário a instação das bibliotecas Python listadas abaixo

- pip install pandas
- pip install numpy
- pip install matplotlib
- pip install folium
- pip install seaborn
- pip install prov
- pip install pydot
- pip install kaleido
- pip install pygrib ou conda install -c conda-forge pygrib
- pip install cartopy
- pip install plotly

## Como executar

### Passo 1: Fonte de dados

É necessário usar os dados escontrados no ["Banco de Dados Meteorológicos"](https://portal.inmet.gov.br/dadoshistoricos) do INMET, disponibilizados como um arquivo compactado .rar por ano, contendo todas as estações operantes nesse período. Após baixado os arquivos dos anos que deseja fazer a análise, basta descompactar em uma pasta chamada "inmet" dentro da pasta datasets. Nesse repositório estamos disponibilizando o arquivo referente ao ano de 2019.  

Nesse trabalho, estamos usando apenas as estações de código A709, A721, A743, A759, S701, S706, S710, S712 e S716, todas localizadas no Mato Grosso do Sul.  

### Passo 2: Análise dos dados e padronização

Para isso basta executar o notebook python "AvaliaçãoDados.ipynb" para fazer a limpeça, união das planilhas de uma mesma estação (se houverem dois ou mais anos sendo analisados), agregação para dados diários e união para um arquivo consolidado. O resultado de cada etapa irá para uma pasta ou arquivo específico e pode ser usada idependentemente.  

### Passo 3: Geração de gráficos

Dentro da pasta "Estudo" existe uma série de notebooks com visualizações dos dados disponíveis resultantes do passo anterior e de outras fontes testadas.

- Interpolacao.ipynb: Visualização de mapa usando geopandas e tentativa de interpolar os dados existes para o Brasil. Necessita dos dados diários.
- Plotando mapa.ipynb: Visualização dos mapas filtrados para o nosso escopo usando folium. Necessita dos dados consolidados
- Mapas Meteorológicos.ipynb: Experimentos para visualizar mapas usando pygrib.
- Graficos.ipynb: Notebook para testes de visualização. Necessita dos dados consolidados
- ValidacaoDados.ipynb: Notebook para visualização de algumas variaveis do dataset do INMET. Necessita dos dados consolidados

### Passo 4: KcDual

Na pasta principal existe um notebook chamado "KcDual-py.ipynb". Ele executa as simulações usando o arquivo "consolidado.csv" originário do Passo 1. Executando ele, o retorno será um gráfico para cada estação presente nesse arquivo, com simulações referentes ao risco atrelado ao plantar soja em nove períodos diferentes.

## Cite as

---
> Alex Santos, Anderson Neto, Douglas Castro. (2022). alexsantoss/Fundamentos-DS: Repository using KcDual and datasets from INMET

