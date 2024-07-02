# # Bicicletas Compartilhadas em Iowa - Análise Power BI

## Visão Geral
Este repositório apresenta um projeto de análise em Power BI focado no uso de bicicletas compartilhadas em Iowa. Os dados utilizados nesta análise foram obtidos do Google BigQuery, especificamente do conjunto de dados `bigquery-public-data.austin_bikeshare.bikeshare_trips`. O objetivo deste projeto é analisar os padrões de uso, durações das viagens e tipos de assinantes do sistema de bicicletas compartilhadas em Iowa.

## Extração de Dados
Os dados foram extraídos do Google BigQuery utilizando a seguinte consulta SQL:

```sql
SELECT  
    start_station_id, 
    bike_id,
    trip_id,
    start_time,
    bike_type,
    duration_minutes,
    subscriber_type
FROM 
    `bigquery-public-data.austin_bikeshare.bikeshare_trips`
WHERE
    EXTRACT(Year FROM start_time) > 2018
```

   ## Campos de Dados:
- **start_station_id**: ID da estação onde a viagem começou
- **bike_id**: Identificador único da bicicleta utilizada
- **trip_id**: Identificador único da viagem
- **start_time**: Timestamp do início da viagem
- **bike_type**: Tipo de bicicleta utilizada (ex.: padrão, elétrica)
- **duration_minutes**: Duração da viagem em minutos
- **subscriber_type**: Tipo de assinante (ex.: membro, casual)

## Etapas do Projeto

### 1. Preparação dos Dados
Os dados foram limpos e transformados para garantir precisão e consistência. Isso envolveu o tratamento de valores ausentes, correção de tipos de dados e criação de colunas calculadas adicionais quando necessário.

### 2. Análise de Dados
Usando o Power BI, várias visualizações e análises foram realizadas para descobrir insights sobre o sistema de bicicletas compartilhadas. As principais áreas de foco incluíram:
- Análise da duração das viagens
- Padrões de uso das bicicletas
- Distribuição dos tipos de assinantes
- Análise temporal das viagens (tendências diárias, mensais, anuais)

### 3. Criação do Dashboard
Um dashboard abrangente em Power BI foi criado para visualizar os achados. O dashboard inclui gráficos interativos, mapas e filtros que permitem aos usuários explorar os dados em detalhes. Principais características do dashboard:
- Visão geral das viagens totais e bicicletas únicas utilizadas
- Desagregação das viagens por estação de início e tipo de bicicleta
- Análise dos tipos de assinantes
- Tendências temporais no uso das bicicletas

### 4. Insights e Conclusões
A análise proporcionou vários insights chave:
- Horários de pico para o uso do sistema de bicicletas compartilhadas
- Estações de início e rotas populares
- Diferenças na duração das viagens entre tipos de bicicletas
- Comportamento e preferências dos assinantes

## Dashboard Power BI
[Link para o Dashboard](https://app.powerbi.com/view?r=eyJrIjoiODZjMDM1ZmMtMTQxYy00MDU4LTgyNjAtMzIzZWRjZjQ2NTBhIiwidCI6ImFjOThjM2Q5LWM5ZGQtNDM0MC1iM2YzLTQxOWEwOTAxMjdjZiJ9
)

## Conteúdo do Repositório
- **Consulta SQL**: `data_extraction.sql` - A consulta SQL utilizada para a extração dos dados.
- **Arquivo Power BI**: `bikeshare_analysis.pbix` - O arquivo Power BI contendo a análise e visualizações.
- **README.md**: Este arquivo, fornecendo uma visão geral do projeto.

## Conclusão
Este projeto demonstra o poder da análise de dados e visualização na compreensão e melhoria dos sistemas de bicicletas compartilhadas. Ao analisar os dados, podemos identificar tendências e padrões que podem informar decisões para melhorar a experiência do usuário e a eficiência operacional dos programas de bicicletas compartilhadas.

## Contato
Para qualquer dúvida ou feedback, por favor entre em contato via [LinkedIn](#) ou [email](mailto:#).
