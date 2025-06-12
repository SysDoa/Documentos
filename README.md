# SysDoa - Documents

Repositório que representa a documentação do SysDoa.

## Padrões de diretórios

Cada ciclo de um Produto mínimo viável (Minimum viable product - MVP) terá um prórpio diretorio como forma de pacote, no qual terá diretórios de:
- Descoberta: Tudo que serve de base levantamentos do sistema, como tipos de dados coletados de um documento, formulários de pesquisa, contexto, slides de workshops, ata e etc.
- Requisitos: são analisados e definidos. Nele terá os diretórios de requisitos funcionais, não funcionais e prd.
- Diagramas: são os diagramas resultantes dos requisitos, como diagrama de caso de uso, diagrama de classe e etc.

O modelo fica mais ou menos assim:

Documents
    - MVP-01
        - descobertas
        - requisitos
            - funcionais
            - nao-funcionais
            - prd
        - diagramas
    - MVP-02
        - descobertas
        - requisitos
            - funcionais
            - nao-funcionais
            - prd
        - diagramas
    - MVP-03
        - descobertas
        - requisitos
            - funcionais
            - nao-funcionais
            - prd
        - diagramas

## Padrões de nomeclatura dos artefatos

- Diretórios: 
    - Sempre em minusculo, separados por hífem em vez de espaços e sem pontuação
- Requisitos:
    - Markdown, ou seja, com final .md
    - Sempre em letra maiuscula
    - Requisitos funcionais: prefixo RF com o número de identificação logo após, como RF01
    - Requisitos não funcionais: prefixos RNF com o número de identificação logo após, como RNF01
- Descobertas:
    - Sempre em letra maiuscula, separada com hífem em vez de espaços e sem pontuação, como LISTA-DE-CANDIDATOS.json
- Diagramas:
    - Sempre em letra maiuscula, separada com hífem em vez de espaços e sem pontuação, como DIAGRAMA-DE-CASO-DE-USO.png

## Padrões de artefatos dos requisitos

### Requisitos funcionais

Devem ter:

- Identificador 
- Caso de uso
- Descrição
- Prioridade
- Dependências
- Cardinalidades
- Tabela de Dados
    - Nome	
    - Tipo	
    - Valor Obrigatório
    - Restrições
- Observações Extras

### Requisitos não funcionais

Devem ter:

- Identificador
- Descrição
- Prioridade
- Categoria
- Observações Extras

