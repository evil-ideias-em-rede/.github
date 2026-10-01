# Kit de Reprodutibilidade do Artigo "Contraponto: Docentes e IA em Colaboração na Geração de Materiais Didáticos a partir de Fontes Primárias"

Este repositório reúne os componentes necessários para executar e explorar:
1. O protótipo do Contraponto, uma plataforma baseada em agentes de inteligência artificial para apoiar docentes na criação de materiais didáticos a partir de fontes primárias.
2. O experimento realizado com professores do Ensino Fundamental II e Médio para medir a viabilidade de adotar a ferramenta Contraponto para incluir e/ou facilitar a inclusão de audiências públicas como fontes primárias para atividades e planos de aula focados em cidadania e temas relevantes para a população.

### A plataforma desenvolvida pode ser acessada via https://evil-levi.01424210.xyz/

O kit é composto por quatro repositórios, que operam partes diferentes do sistema e do experimento:

* **`back-end`** — API, agentes de inteligência artificial, autenticação, persistência e serviços de apoio à aplicação;
* **`front-end`** — interface web utilizada pelos docentes para interagir com o sistema;
* **`anotador`** — ferramentas utilizadas na preparação e anotação das falas dos debates segundo a taxonomia utilizada no artigo;
* **`experimento`** — documentos utilizados durante o experimento com os professores, respostas dos participantes e artefatos derivados destas respostas.

## Overview dos repositórios

### `back-end`

Responsável pela execução da API e pela lógica do sistema, incluindo os agentes responsáveis pelo processamento das solicitações e a comunicação com os serviços externos.

#### Principais componentes:

* agentes implementados com LangGraph;
* integração com modelos da OpenAI;
* banco de dados PostgreSQL;
* armazenamento vetorial para recuperação de informações.

### `front-end`

Responsável pela interface web do Contraponto, utilizada pelos docentes para interagir com a plataforma e com os materiais produzidos.

#### Principais componentes:

* interface desenvolvida com React e TypeScript;
* interação com a API disponibilizada pelo back-end;
* seleção e consulta de debates;
* visualização e edição dos materiais didáticos;
* gerenciamento de materiais e templates.

### `anotador`

Responsável pela preparação e anotação das falas dos debates públicos utilizados pelo Contraponto, organizando os dados segundo a taxonomia utilizada no artigo.

#### Principais componentes:

* preparação dos dados dos debates;
* organização por debates, participantes e falas;
* anotação das falas segundo a taxonomia do projeto;
* geração de resumos e propostas associadas às falas;
* ferramentas para revisão das anotações;
* prompts e ferramentas auxiliares para o processo de anotação.

### `experimento`

Responsável pelos materiais e registros relacionados ao experimento realizado com professores do Ensino Fundamental II e Médio.

#### Principais componentes:

* documentos utilizados durante a realização do experimento;
* materiais apresentados aos participantes;
* respostas dos professores;
* artefatos derivados das respostas coletadas.

## Execução e Requisitos

Cada componente possui suas próprias instruções de configuração, execução e reprodução. Recomendamos que você acesse cada repositório individualmente para mais instruções:

- [Back-end](https://github.com/evil-ideias-em-rede/back-end)
- [Front-end](https://github.com/evil-ideias-em-rede/front-end)
- [Anotador](https://github.com/evil-ideias-em-rede/anotador)
- [Experimento](https://github.com/evil-ideias-em-rede/experimento)

## Fluxo geral do sistema

De forma simplificada, o funcionamento do Contraponto pode ser representado pelo seguinte fluxo:

```text
Dados de debates
       ↓
Preparação e anotação
       ↓
Base de dados
       ↓
Recuperação de informações
       ↓
Agentes de IA
       ↓
Material didático
       ↓
Interface de edição
```

O docente permanece envolvido no processo, podendo selecionar informações, fornecer materiais de referência e revisar ou modificar o conteúdo produzido.

## Dados

O projeto utiliza dados de debates públicos disponibilizados pelo conjunto PublicHearingBR, provenientes de audiências públicas da Câmara dos Deputados.

O repositório anotador contém as ferramentas utilizadas para preparação e anotação desses dados.

Além dos debates, o sistema utiliza referências educacionais e pedagógicas para apoiar o processo de geração dos materiais.

Modelos e serviços externos

A execução do sistema depende de serviços externos utilizados pelos componentes do projeto, especialmente modelos de linguagem da OpenAI.

As configurações relacionadas aos modelos e às credenciais devem ser fornecidas por meio das variáveis de ambiente ou arquivos de configuração indicados nos respectivos repositórios.

As chaves de API e outras credenciais não devem ser incluídas no repositório.

## Observações sobre reprodutibilidade

Este kit disponibiliza o código necessário para executar o protótipo, os materiais utilizados no experimento e reproduzir o fluxo de funcionamento apresentado no trabalho.

Os resultados apresentados no manuscrito que ainda estão em desenvolvimento ou em caráter simulado não fazem parte deste procedimento de reprodução. O objetivo deste kit é disponibilizar os componentes implementados do sistema e os instrumentos utilizados no experimento, e não reproduzir resultados experimentais ainda não consolidados.

## Citação

Se você utilizar este material, cite o trabalho:

```text
VILAR, Iriedson; CHRISTIE, Emile; JUNIOR, Levi; PEREIRA, Vinicius.
Contraponto: Docentes e IA em Colaboração na Geração de Materiais
Didáticos a partir de Fontes Primárias. Ideias em Rede, 2026.
```
