# Análise de Preços de Combustíveis em 2023

**Autor**: Ana Júlia dos Reis Siqueira  
**Data**: 29 de Janeiro de 2025  

## Objetivo

O objetivo deste trabalho é realizar uma análise detalhada dos preços de combustíveis no Brasil, com base em dados coletados ao longo de 2023. A análise foca em entender as variáveis que influenciam a variação de preços, identificando padrões e tendências regionais, estaduais, e por tipo de combustível, além de examinar as relações entre o valor de venda e outras variáveis categóricas como bandeira dos postos e produto.

## Tratamento de Dados

O conjunto de dados apresenta variáveis cruciais para a análise, como tipo de combustível, estado, município, preço de venda e compra, e outros dados relevantes das revendas de combustíveis. A seguir, descrevem-se as variáveis e o processo de limpeza e tratamento realizado.

### Variáveis
- **Região**: Sigla da região geográfica
- **Estado**: Sigla do estado
- **Município**: Nome do município
- **Revenda**: Nome da revenda de combustível
- **CNPJ da Revenda**: CNPJ da revenda
- **Nome da Rua**: Nome da rua
- **Número Rua**: Número da rua
- **Complemento**: Complemento do endereço
- **Bairro**: Bairro da revenda
- **Cep**: Código postal
- **Produto**: Tipo de combustível
- **Data da Coleta**: Data de coleta dos dados
- **Valor de Venda**: Preço de venda do combustível
- **Valor de Compra**: Preço de compra do combustível
- **Unidade de Medida**: Unidade de medida utilizada (R$/litro ou R$/m3)
- **Bandeira**: Bandeira do posto de combustível

### Tratamento de Valores Faltantes

Durante a exploração dos dados, observamos que algumas variáveis apresentaram valores ausentes, como mostrado na tabela abaixo:

| Coluna            | Valores Faltantes | Percentual Faltante (%) |
|-------------------|-------------------|-------------------------|
| Complemento       | 695,579           | 76.94                   |
| Valor de Compra   | 904,000           | 100.00                  |
| Número Rua        | 247               | 0.03                    |
| Bairro            | 1,682             | 0.19                    |

- A variável **"Complemento"** foi excluída devido ao elevado percentual de dados ausentes (76,94%).
- A variável **"Valor de Compra"** foi removida devido à ausência total de dados.
- Para as variáveis **"Número Rua"** e **"Bairro"**, que apresentaram pequenas proporções de dados ausentes (0,03% e 0,19%, respectivamente), os valores faltantes foram preenchidos com **"Desconhecido"**.

### Conversão de Unidade de Medida

Observou-se que a coluna **"Unidade de Medida"** possuía valores tanto em **R$/litro** quanto em **R$/m³**. Para garantir consistência nas comparações dos preços, todos os valores em **R$/m³** foram convertidos para **R$/litro** (dividindo os valores por 1000). 

Além disso, as colunas **"Região - Sigla"** e **"Estado - Sigla"** foram renomeadas para **"Região"** e **"Estado"**, respectivamente.

## Análise Exploratória

### Variáveis Categóricas

A análise exploratória das variáveis categóricas visa entender a distribuição dos dados e identificar padrões relevantes.

#### Região

A região **Sudeste (SE)** apresenta a maior concentração de dados, o que pode ser atribuído à maior densidade de postos de combustíveis ou à intensidade de coleta de dados nessa área. As regiões **Norte (N)** e **Centro-Oeste (CO)** têm menor representatividade.

#### Estado

Os estados da **Região Sudeste** dominam a distribuição, com **São Paulo (SP)** liderando, seguido por **Minas Gerais (MG)** e **Rio de Janeiro (RJ)**. Em contraste, estados da **Região Norte** e **Centro-Oeste**, como **Roraima (RR)** e **Mato Grosso (MT)**, possuem menos registros.

#### Produto

A **Gasolina** é o combustível mais comum, seguido pelo **Etanol** e **Gasolina Aditivada**. O **GNV** apresenta a menor representatividade no conjunto de dados.

#### Bandeira

A **Bandeira Branca (postos independentes)** domina o mercado, seguida pelas grandes redes **Ipiranga** e **Raízen**. Outras bandeiras como **Vibra Energia** também têm uma participação relevante, mas em menor escala.

### Valor de Venda

O valor de venda apresenta uma distribuição com um valor mínimo de **2,39** e um valor máximo de **9,79**, com a mediana de **5,49** e a média de **5,30**, sugerindo uma leve assimetria à esquerda. A maior parte dos valores está entre **4,84** (Q1) e **5,94** (Q3).

#### Relação com Estado

A maioria dos estados apresenta preços concentrados entre **5 e 6 reais**, com exceção de **Acre (AC)**, cujos preços são mais elevados. A variação dos preços é mais significativa em estados como **Goiás (GO)** e **Mato Grosso (MT)**.

#### Relação com Região

As regiões **Sul** e **Norte** exibem diferentes padrões. A região **Norte** apresenta preços mais elevados e com menos variação, enquanto a **Sul** tem uma maior dispersão, com muitos outliers.

#### Relação com Produto

Os preços do **Etanol** são os mais acessíveis, com a mediana mais baixa. Já a **Gasolina** e a **Gasolina Aditivada** apresentam preços mais elevados, com uma maior estabilidade nos valores. O **Diesel** e **Diesel S10** têm maior volatilidade.

#### Relação com Bandeira

A mediana dos preços varia entre **5,34** e **6,19**, com algumas bandeiras apresentando maior dispersão nos preços, como **Ipiranga** e **Vibra Energia**. Outras, como **Atem's**, apresentam preços mais estáveis.

## Conclusão

O tratamento adequado dos dados e a análise exploratória forneceram uma visão detalhada sobre os preços de combustíveis em diferentes regiões e estados do Brasil. A variabilidade dos preços é influenciada por diversos fatores, como a região, o tipo de combustível, e a bandeira dos postos, e os resultados indicam a necessidade de considerar essas variáveis ao realizar comparações e previsões sobre o mercado de combustíveis.
