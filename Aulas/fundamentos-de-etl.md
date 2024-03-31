# Fundamentos Teóricos de ETL

## ETL
Extrair, transformar e carregar (ETL) é o processo que as organizações orientadas a dados usam para coletar dados de várias fontes e reuni-los para dar suporte à descoberta, à geração de relatórios, à análise e à tomada de decisões.

![ETL](https://rivery.io/wp-content/uploads/2021/07/ETL-Process-1.png)

### Extrair (Extract)
Durante a extração, o ETL identifica os dados e os copia de onde estão guardados para outro lugar onde serão armazenados. Os dados podem vir de fontes estruturadas ou não estruturadas, como documentos, emails, bancos de dados, sensores, entre outros.

### Transformar (Transform)
Os dados extraídos são "cruos" e precisam ser organizados e modificados para que possam ser armazenados corretamente. Durante a transformação, o ETL verifica, confirma, remove duplicatas e/ou combina os dados de maneiras que os tornem úteis e confiáveis para consultas futuras.

### Carregar (Load)
O ETL move os dados transformados para o lugar onde serão armazenados definitivamente. Isso pode envolver transferir todos os dados de uma vez ou apenas as mudanças feitas desde a última transferência. Podendo fazer isso em tempo real ou em lotes programados.

## ELT
![ELT](https://assets-global.website-files.com/6130fa1501794e37c21867cf/6335c7ccc0eafe4a770c4077_4vDEfd5ZlHp75WTdQfzi-10kQAtfeZRJDSDdlV7rKEwe_5XvxRxkKTjmTHLEOARrs7EgUAgsSm-XPFm9QH61uSc1PVSGhpdatlWuWXFiH5bZxjwrIjMU0WP0bbqpUr_OVEiaLQ2yqh49vaYqyPAnScad8gPL_xJF6354k5BhwEzJJPLGqnF7vJMWaw.png)

### Vantagens
- Otimização de tempo (carregamento, transformação e manutenção)
- Eficiência na implementação de projeto
- Menos dependência de TI
- Usabilidade
- Limitação de dados

## Diferenças entre ETL e ELT
 ![ETLxELT](https://miro.medium.com/v2/resize:fit:1400/0*rUQ1XTQz_OHKL4fY.png)

- A etapa de transformação é a mais complexa no processo ETL.
- ETL e ELT diferem em dois aspectos principais:
  - Quando a transformação ocorre:
    - No ETL, a transformação acontece antes do carregamento dos dados no destino.
    - No ELT, a transformação ocorre após o carregamento dos dados no destino.
  - Local da transformação:
    - No ETL, as transformações ocorrem antes do carregamento no data warehouse.
    - No ELT, as transformações são realizadas no próprio data warehouse após o carregamento dos dados.
- Tradicionalmente, a transformação ocorre antes do carregamento dos dados em um data warehouse.
- Com a evolução das tecnologias de armazenamento e processamento de dados, as transformações podem ser feitas no sistema de destino.
- No ETL, as áreas de preparação estão nas ferramentas entre o sistema de origem e o data warehouse.
- No ELT, a área de preparação está no data warehouse, e as transformações são realizadas pelo mecanismo de banco de dados.