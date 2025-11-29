# CORRELAÇÃO ENTRE PIB E FEMINICÍDIOS NO BRASIL 2011-2021

O presente trabalho tem como objetivo realizar um artigo para publicação na revista SENAI e apresentação durante o II Congresso UniSENAI SP.

Para execusão do trabalho foi necessário buscar os dados de violência contra mulher de 2011 a 2021, analisar pib dos estados e municípios de sp e realizar uma proporção utilizando dados do censo demográfico.

### 🔍 LINKS
Taxa de Homicídios Mulheres
[TAXA HOMICIDIOS MULHERES](https://www.ipea.gov.br/atlasviolencia/dados-series/52 )

Homicídios Mulheres
[HOMICIDIO MULHERES](https://www.ipea.gov.br/atlasviolencia/dados-series/40) 

Homicídios
[HOMICIDIOS](https://www.ipea.gov.br/atlasviolencia/dados-series/328 )

Projeções da População
[PROJECAO DA POPULACAO](https://www.ibge.gov.br/estatisticas/sociais/populacao/9109-projecao-da-populacao.html )

Seade Censo 2022
Dados senso de 2022
[SENSO 2022](https://repositorio.seade.gov.br/dataset/seade-censo-2022 )


População Brasileira
[POPULACAO BRASILEIRA](https://basedosdados.org/dataset/d30222ad-7a5c-4778-a1ec-f0785371d1ca?table=b99f0017-e587-477e-8cfb-05fb5d1005b8 )

Produto Interno Bruto dos Municípios
[PIP MUNICIPIOS](https://www.ibge.gov.br/estatisticas/economicas/contas-nacionais/9088-produto-interno-bruto-dos-municipios.html?=&t=resultados)

Utilizar base de dados do IPEA homicídios contra mulheres dos anos de 2011 a 2019, verificar a taxa de homicídios de mulheres dividindo a quantidade de homicídios de mulheres / quantidade de mulheres do estado nos respectivos anos e multiplicar por 100.000.

Após verificar a taxa de PIB, por população nos anos de análise.

verificar se quanto maior o pib menor é a taxa de homicídios?
verificar se quanto menor o pib maior a taxa de homicídios?


## CORRELAÇÃO ENTRE PIB E FEMINICÍDIOS NO BRASIL 2011-2021

### 📊 Desenvolvimento Econômico, Indústria e Violência de Gênero
Uma Análise da Correlação entre PIB e Feminicídios no Brasil (2011–2021)

### 📋 Sobre o Projeto
Este projeto foi desenvolvido para apresentação no II Congresso UniSENAI SP 2025. O estudo analisa a incidência do feminicídio no Brasil ao longo de uma década (2011-2021), investigando estatisticamente sua relação com o Produto Interno Bruto (PIB) estadual e indicadores de desemprego.
A hipótese central verificada foi a de que regiões com maior desenvolvimento econômico e industrial tendem a apresentar menores taxas proporcionais de violência letal contra mulheres.

### 👥 Autores
- Antonio Carlos Amador Junior

- Giovanna dos Santos Sousa

- Aruane Mello Pineda Pertinhez

### 🔍 Principais Descobertas
Com base no processamento de dados realizado, o estudo concluiu:
Disparidade Regional: Enquanto estados populosos (SP, MG) lideram em números absolutos, as maiores taxas por 100 mil habitantes concentram-se em regiões com menor PIB (ex: Ceará, Acre, Tocantins).
Correlação Negativa: Foi identificada uma correlação de Pearson de -0.57 (ano base 2021) entre o PIB estadual e a taxa de feminicídios, indicando uma tendência moderada onde maior riqueza econômica está associada a menores índices de violência.
Contexto Industrial: A análise sugere que a dinâmica econômica e a infraestrutura industrial podem atuar como fatores de proteção social indireta.

### 🛠️ Tecnologias e Bibliotecas
O projeto foi inteiramente desenvolvido em Python, utilizando o ambiente Google Colab.
pandas: Manipulação, limpeza e fusão (merge) de DataFrames.
matplotlib & seaborn: Visualização de dados (Gráficos de barras, linhas, boxplots e heatmaps).
numpy: Operações matemáticas e normalização de dados.

### 📂 Fontes de Dados
Os dados utilizados são públicos e foram obtidos através das seguintes fontes oficiais:
Atlas da Violência (IPEA): Dados brutos de homicídios de mulheres.
Acesse aqui
IBGE - Projeções de População: Utilizado para calcular a taxa proporcional (população feminina por estado).
Acesse aqui
IBGE - PIB dos Municípios/Estados: Dados econômicos para correlação.
Acesse aqui
IPEADATA: Taxas de desemprego desagregadas por gênero.
Acesse aqui

### ⚙️ Metodologia (Pipeline de Dados)
O script homicidiomulheres.py executa o seguinte fluxo de trabalho ETL (Extract, Transform, Load):
1. Coleta e Limpeza
Importação dos arquivos .csv e .xlsx.
Filtragem temporal: Recorte do período de estudo (2011 a 2021).
Padronização de colunas (Renomeação de UF, Período, Valor para consistência entre bases).
2. Feature Engineering (Criação de Variáveis)
Para comparar estados de tamanhos diferentes, não utilizamos apenas os números absolutos. Calculamos a taxa padronizada:
$$\text{Taxa} = \left( \frac{\text{Nº de Feminicídios}}{\text{População Feminina do Estado}} \right) \times 100.000$$
3. Fusão de Dados (Data Merging)
Unificação das bases de dados (Violência + População + Economia) utilizando a chave composta UF e ANO.
4. Análise Estatística
Matriz de Correlação: Cálculo do coeficiente de Pearson para validar a relação entre PIB e Violência.
Comparativo Absoluto vs. Relativo: Contrastar onde ocorrem mais mortes versus onde é mais perigoso viver.

### 📊 Visualizações Geradas
O código gera os seguintes gráficos para análise:

### Ranking por Estado: Gráficos de barras comparando os casos absolutos e as taxas proporcionais.
<img width="1590" height="789" alt="image" src="https://github.com/user-attachments/assets/e09db500-34aa-4922-b4d9-469777535b49" />

### Correlação (Heatmap): Mapa de calor evidenciando a correlação negativa entre PIB Total e Taxa de Feminicídio.
<img width="758" height="490" alt="image" src="https://github.com/user-attachments/assets/652a1a30-edfa-4f46-aebb-9b530ddecd90" />

### Análise de Casos Extremos: Destaque para os 3 estados com maiores e menores taxas em 2021.
<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/3811bf81-be91-4d64-9417-c6b772797a0d" />


### 🚀 Como Executar
Clone o repositório:
Bash
[https://github.com/Arzioti/correlacao-entre-pib-e-feminicidios-no-brasil-2011-2021/tree/main](https://github.com/Arzioti/correlacao-entre-pib-e-feminicidios-no-brasil-2011-2021/tree/main)


### Instale as dependências:
Bash
pip install pandas seaborn matplotlib numpy openpyxl


Ajuste os caminhos:
O script original utiliza caminhos do Google Drive (/content/drive/...). Para rodar localmente, baixe os arquivos e cole o caminho no campo escrito "COLE AQUI" no arquivo homicidiomulheres.py para apontar para a pasta onde você salvou os arquivos CSV/Excel.
Execute o script:
Você pode rodar o arquivo .py ou abrir em um Jupyter Notebook.



Este projeto foi desenvolvido como parte das atividades acadêmicas do curso de Análise e Desenvolvimento de Sistemas/Ciência de Dados.

