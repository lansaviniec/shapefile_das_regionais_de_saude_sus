## Shapefile contendo o mapa das Regionais de Saúde do SUS

O território brasileiro possui representações cartográficas em vários níveis: regiões, estados, municípios, etc. Sendo o município a unidade territorial mínima. Para facilitar a administração do Sistema Único de Saúde (SUS), o Ministério da Saúde instituiu a divisão do território brasileiro em Regionais de Saúde. As Regionais de Saúde são espaços geográficos constituídos por agrupamentos de municípios, que visam facilitar o planejamento, a execução e a disseminação dos serviços de saúde entre os municípios. Ao todo, os 5570 municípios brasileiros são agrupados em 450 Regionais de Saúde.

Neste repositório, disponibilizamos um arquivo CSV contento a distribuição territorial brasileira e dois shapefiles contendo o mapeamento das Regionais de Saúde. Os arquivos são baseados em dados do IBGE e do SUS.


### Conteúdo do repositório

Arquivo DTB.csv: Contém a distribuição territorial brasileira (2019), mostrando o relacionamento entre Regiões, Estados, Regionais de Saúde, e Municípios. Os dados foram extraídos do IBGE [1] e do DATASUS [2]. Obs: a geocodificação apresentada neste arquivo segue os códigos do IBGE. O campo "municipio_id_sdv" é o código do município sem o dígito verificador. Algumas bases do DATASUS usam esse código ao invés do código completo.

Arquivo br_regionais.zip: Contém o shapefile das Regionais de Saúde geradas a partir do shapefile de Municípios (2019) disponibilizado pelo IBGE [3]. Os polígonos deste shapefile representam fielmente os contornos dos municípios descritos na malha 2019 do IBGE. Este arquivo é demasiado grande em quantidade de MegaBytes, aproximadamente 75 MB. Faça o download em [4]. 
 
Arquivo br_regionais_simplificado.zip: É uma simplificação da malha anterior usando um algoritmo de simplificação de polígonos [5]. Isto introduz alguns "gaps" entre os polígonos e pode ser observado aumentando-se o zoom nas fronteiras dos polígonos. Entretanto, este arquivo possui apenas 2 MB e é ideal para a produção de mapas e dashboards, devido seu tamanho reduzido.

BR_Regionais_Simplificado.geojson: Arquivo JSON do shapefile simplificado. Este arquivo possui 3 MB.


### Como os shapefiles foram gerados

Os shapefiles foram gerados a partir do shapefile de municípios do IBGE usando a API PyQGIS [6], disponível no Software QGIS.


### Referências

[1] https://www.ibge.gov.br/geociencias/organizacao-do-territorio/divisao-regional/23701-divisao-territorial-brasileira.html?=&t=downloads

[2] http://www2.datasus.gov.br/DATASUS/index.php?area=060206

[3] https://www.ibge.gov.br/geociencias/organizacao-do-territorio/malhas-territoriais/15774-malhas.html?=&t=downloads

[4] https://drive.google.com/file/d/1loReIPMSJHz9EdQgB78qoI7HVZQIhJjP/view?usp=sharing

[5] https://en.wikipedia.org/wiki/Ramer%E2%80%93Douglas%E2%80%93Peucker_algorithm

[6] https://qgis.org/pyqgis/

---

### Autores:

Dr. Landir Saviniec (UFPR - Campus de Jandaia do Sul)

Dra. Alexsandra Bezerra da Rocha (UFCG - Campus Cajazeiras)

### Como citar esses dados:

SAVINIEC, Landir; ROCHA, Alexsandra Bezerra da. Shape das Regiões de Saúde do Brasil. 13 de jul. de 2020. Disponível em: <https://github.com/lansaviniec/shapefile_das_regionais_de_saude_sus>

