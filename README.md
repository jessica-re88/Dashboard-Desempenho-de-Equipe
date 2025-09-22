README.md

## Painel de Desempenho de Equipe - Power BI

Visão Geral do Projeto

Este projeto transforma dados brutos de uma empresa fictícia em um painel de controle interativo e estratégico usando o Power BI. O objetivo principal é fornecer uma visão clara e detalhada do desempenho da equipe, da produtividade e da estrutura organizacional, facilitando a tomada de decisões baseadas em dados.

## Fontes de Dados

O projeto utilizou seis tabelas como fontes de dados, cada uma representando uma parte da organização:

    employee: Informações detalhadas de funcionários (Ssn, salário, sexo, etc.).

    departament: Dados sobre os departamentos da empresa.

    dept_locations: Localizações físicas de cada departamento.

    works_on: Registro das horas que cada funcionário trabalhou em projetos.

    dependent: Informações sobre os dependentes dos funcionários.

    project: Dados sobre os projetos.

## Etapas de Transformação (Power Query)

Para preparar os dados para análise, as seguintes transformações foram realizadas:

    Limpeza e Tipagem de Dados: Os cabeçalhos e os tipos de dados foram padronizados em todas as tabelas, garantindo a integridade dos dados.

    Enriquecimento de Dados: Colunas de nomes (Fname, Minit, Lname) foram combinadas em uma única coluna Full Name.

    Agrupamento e Resumo: Uma tabela de resumo (employee (3)) foi criada para contar o número de funcionários por gerente, fornecendo uma visão agregada da estrutura de equipe.

    Remoção de Colunas: Colunas que não seriam usadas no relatório final, como Address e Bdate da tabela employee, foram removidas para simplificar o modelo.

## Modelo de Dados (Power BI)

As tabelas foram relacionadas para criar um modelo de dados coerente, permitindo que as visualizações interajam dinamicamente. As relações foram estabelecidas com base nas chaves primárias e estrangeiras:

    employee <-- works_on (Chaves: Ssn e Essn).

    employee <-- dependent (Chaves: Ssn e Essn).

    employee <-- departament (Chaves: Dno e Dnumber).

    works_on <-- project (Chaves: Pno e Project Quantity).

    departament <-- dept_locations (Chaves: Dnumber e Department Quantity).

    Relação de Hierarquia: A tabela employee foi relacionada a si mesma (Chaves: Ssn e Manager) para mapear a hierarquia de gerência.

## Visualizações e Análise do Dashboard

O Painel de Desempenho de Equipe foi projetado com as seguintes visualizações para fornecer insights acionáveis:

    KPIs: Cartões de destaque mostrando o Total de Funcionários, Salário Total e Total de Horas de Trabalho, oferecendo uma visão geral rápida da saúde da empresa.

    Análise de Desempenho por Gerente: Gráficos de barra que mostram a contagem de funcionários por gerente e uma tabela detalhada dos salários totais gerenciados.

    Demografia: Um Gráfico de Rosca (Employee Sex) para visualizar a distribuição de gênero na empresa.

    Análise Geográfica: Um Gráfico de Mapa que localiza os departamentos, fornecendo uma perspectiva geográfica das operações.

## Conclusão

Este projeto demonstra a capacidade de transformar dados brutos em inteligência de negócio. O dashboard Painel de Desempenho de Equipe é uma ferramenta poderosa para a gestão de pessoal e operações, permitindo que os líderes tomem decisões estratégicas com base em dados precisos e visualmente claros.
---
## 📈 Visual do Dashboard
Exemplo de visualização do dashboard:  

![Dashboard](https://github.com/jessica-re88/Dashboard-Desempenho-de-Equipe/blob/main/Dashboard.png)
---
