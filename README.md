# Análise de Risco Climático e Impacto no Atlântico (CLIMADA)

## Visão Geral do Projeto

Este projeto utiliza a plataforma de avaliação de risco climático **CLIMADA** para analisar e quantificar os riscos e impactos de eventos climáticos e oceanográficos extremos em ativos empresariais. O foco está em regiões estratégicas do **Oceano Atlântico**, visando proteger tanto as operações de **embarcações** quanto as **sedes** localizadas em áreas costeiras ou portuárias.

Através da combinação de dados de hazard (perigo), exposição (ativos) e funções de impacto (vulnerabilidade), este projeto busca fornecer uma avaliação probabilística dos danos potenciais e informar estratégias de mitigação e adaptação.

## Objetivos Principais

* **Processar Dados de Hazard**: Ingerir e transformar dados atmosféricos (vento) e oceanográficos (ondas) de modelos de previsão/hindcast em objetos `Hazard` compatíveis com o CLIMADA.
* **Definir Exposição**: Modelar a localização e o valor das embarcações e sedes como objetos `Exposures`.
* **Desenvolver Funções de Impacto**: Criar funções que descrevam a vulnerabilidade dos nossos ativos a diferentes intensidades de vento e ondas.
* **Calcular Impactos Probabilísticos**: Utilizar o motor do CLIMADA para calcular os impactos financeiros esperados sob diferentes cenários.
* **Analisar Risco e Adaptação**: Avaliar as curvas de risco (frequência de excedência) e explorar a eficácia de potenciais medidas de adaptação para reduzir os impactos.

## Estrutura do Repositório

* `data/`: Contém todos os dados de entrada e saída intermediários.
    * `raw/`: Dados originais de modelos (WRF, WW3) e informações brutas de exposição.
    * `processed/`: Objetos CLIMADA (Hazards, Exposures) salvos após processamento.
* `scripts/`: Scripts Python para as etapas do pipeline de análise CLIMADA. Cada script é projetado para uma etapa específica do fluxo de trabalho.
* `notebooks/`: Notebooks Jupyter para análise exploratória de dados, demonstrações interativas do CLIMADA e análises detalhadas.
* `results/`: Resultados finais da análise, incluindo gráficos, relatórios e dados de impacto processados.
* `.gitignore`: Define arquivos e diretórios a serem ignorados pelo Git.
* `README.md`: Este arquivo, fornecendo uma visão geral do projeto.
* `environment.yml`: Arquivo para replicar o ambiente Conda necessário para o projeto.
* `requirements.txt`: Arquivo para replicar o ambiente pip (alternativa a `environment.yml`).
