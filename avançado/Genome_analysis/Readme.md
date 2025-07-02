# Genome_analysis

Projeto criado para comunidade Pyladies Bioinformática para aprimoramento do conhecimento sobre Bioinformática para integrantes de nível .


## Objetivo

O objetivo deste projeto é criar um pipeline acessível para usuários com conhecimentos  em bioinformática que permita baixar, processar e comparar genomas bacterianos para identificar genes de resistência a antibióticos.

### Ferramentas

| Nome da Ferramenta | Versão | Razão de uso |
|--------------------|--------|--------------|
| Visual Studio Code | 1.101.0 | IDE para escrita de código |
| Conda | 25.5.1 | simplifica a instalação e gerenciamento de softwares científicos |
| ncbi-genome-download | 0.3.3 | Download de genomas do ncbi |
| QUAST | 5.3.0 | Avaliar a qualidade de genomas montados (assemblies) |
| BUSCO | 5.8.3 | Avaliar a completude de genomas usando genes essenciais conservados |
| ResFinder | | Identificar genes de resistência a antibióticos em genomas bacterianos |

### Mapa de execução

**Etapa 1**
- [ ] Criação de ambiente virtual conda
- [ ] Download de genomas de Salmonella spp. que estejam completamente montados (Assembly level complete), anotados pelo RefSeq (Annotated by NCBI RefSeq) e suja montagem tenha sido a partir do material Tipo do gênero (assembly from type material)

**Etapa 2**
- [ ] Análise da qualidade da montagem dos genomas com QUAST
- [ ] Verificar a completude dos genomas com BUSCO
- [ ] Gerar gráficos sobre a qualidade dos genomas utilizados

**Etapa 3**
- [ ] Download do Resfinder
- [ ] Identificar genes de resistência à antimicrobianos utilizando ResFinder
- [ ] Gerar gráfico comparativo com a porcentagem de genes relacionados à resistência à antimicrobianos, presentes nos genomas
- [ ] Construir relatório com a conclusão da análise

**Etapa 4**
- [ ] Disponibilizar os scripts de forma organizada em um repositório em seu GitHub
- [ ] Disponibilizar o Readme.md com a explicação da análise


### Instalação Conda

`wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`

**Executar instalação**

`bash Miniconda3-latest-Linux-x86_64.sh -b -p $HOME/miniconda`

**💡 Comandos úteis:**

| Ação                | Comando                          |
|---------------------|----------------------------------|
| Inicializar conda   | `source ~/miniconda/bin/activate` `conda init`|
| Criar ambiente conda| `conda create -n genome-analysis python=3.10 -y`|
| Ativar ambiente     | `conda activate genome-analysis` |
| Desativar ambiente  | `conda deactivate`               |
| Listar ambientes    | `conda env list`                 |
| Remover ambiente    | `conda env remove -n genome-analysis` |

### Instalação ncbi-genome-download

`conda install -c bioconda ncbi-genome-download`

### Instalação QUAST

`conda install -c bioconda quast -y`

### Instalação BUSCO

`conda install -c bioconda busco -y`

### Instalação Resfinder

`git clone https://github.com/genomicepidemiology/resfinder.git`
`cd resfinder`
`pip install -r requirements.txt`
`python INSTALL.py`

### Referências

Florensa, A. F et al, 2022. ResFinder – an open online resource for identification of antimicrobial resistance genes in next-generation sequencing data and prediction of phenotypes from genotypes https://doi.org/10.1099/mgen.0.000748

ResFinder software repository: https://github.com/genomicepidemiology/resfinder.

Manni, M. et al, 2021. BUSCO: Assessing genomic data quality and beyond. Current Protocols, 1, e323. https://doi.org/10.1002/cpz1.323.

### Autoria

**Jeniffer Fonseca**

https://github.com/Jenifferbio

jeniffer_evangelista@hotmail.com



