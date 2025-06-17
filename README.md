# SysDoa

É notório que o controle de candidatos à doação de sangue é fundamental para garantir um estoque seguro e suficiente nos bancos de sangue. Atualmente, a coleta e análise desses dados são feitas de forma manual, dificultando a identificação rápida de doadores aptos e a organização das doações. Neste contexto, propõe-se o desenvolvimento do SysDoa, um sistema móvel que permite não só uma gestão virtual de candidatos de uma agência de banco de sangue, como também possibilita análises estatísticas das informações coletadas.

## Escopo

O escopo define os limites e objetivos do projeto, estabelecendo o que será ou não implementado. No SysDoa, ele orienta o desenvolvimento conforme as necessidades da clínica. Dessa forma, cada interação representa uma fase com evoluções específicas no sistema. Veja a seguir o escopo de cada interação:

### Interação I

Neste momento, o sistema SysDoa será desenvolvido exclusivamente para atender uma clínica específica. Por isso, algumas funcionalidades serão deliberadamente excluídas desta versão inicial, como:

- Cadastro individual de candidatos;
- Edição e exclusão de registros;
- Funcionalidades de login e registro de usuários.

Por outro lado, o sistema contará com: 

- Cadastro de candidatos por lote via upload de arquivos jsons;
- Listagem de possíveis doadores de sangue;
- Informações estatísticas de quantos candidatos existem em cada estado do Brasil;
- Informações estatísticas do IMC médio em cada faixa de idade de dez em dez anos;
- Informações estatísticas do percentual de obesos entre os homens e entre as mulheres;
- Informações estatísticas da média de idade para cada tipo sanguíneo;
- Informações estatísticas da quantidade de possíveis doadores para cada tipo sanguíneo receptor.

## Padrão de Diretórios dos Artefatos

O projeto segue uma estrutura clara de pastas para ajudar na manutenção e colaboração em equipe. Dessa forma, para nortear a organização dos artefatos de requisitos do produto, adotou-se a seguinte hierarquia de diretórios:

documentos  
&nbsp;&nbsp;&nbsp;&nbsp;↳ requisitos  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↳ funcionais  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↳ nao-funcionais

Essa separação permite localizar rapidamente os arquivos e manter a rastreabilidade entre os tipos de requisito.

## Padrão de Nomenclatura dos Artefatos

Para padronizar nomes, evitar confusões e facilitar buscas, foi adotado o seguinte padrão de nomeclatura dos artefatos:

- **Diretórios**: em minúsculas, sem pontuações e separados por hífem em vez de espaços; 

- **Requisitos**: em Markdown (.md) e nomeados com letras maiúsculas para destaque, além de iniciar com o prefixo **RF** para requisitos funcionais e **RNF** para requisitos não funcionais, sempre fornecendo o número de identificação posteriormente.

## Padrão de Artefato de Requisitos

Para garantir rastreabilidade e facilitar a validação dos requisitos ao longo do projeto, será adotado um modelo padronizado. Veja a seguir as regras de padronização dos requistos funcionais e não funcionais:

- **Requisitos funcionais** incluirão campos como caso de uso, fluxos, atores e tabelas de dados, permitindo compreender claramente o comportamento esperado do sistema. Dessa forma, o modelo definido deve conter os campos conforme a ordem seguinte:

    - Identificador
    - Caso de Uso
    - Descrição
    - Prioridade
    - Atores
    - Pré-condições
    - Pós-condições
    - Fluxos Principais
    - Fluxos Alternativos
    - Fluxos de Exceções
    - Dependências
    - Cardinalidades
    - Tabelas de Dados
        - Nome
        - Tipo
        - Valor Obrigatório
        - Restrições
    - Observações Extras

- **Requisitos não funcionais** terão estrutura simples com identificador, prioridade e categoria, focando em restrições e qualidades do sistema. Dessa forma, o modelo definido deve conter os campos conforme a ordem seguinte:

    - Identificador
    - Descrição
    - Prioridade
    - Categoria
    - Observações Extras


## Processo de Desenvolvimento de Artefatos de Requisitos

O processo de desenvolvimento de artefatos de requisitos estabelece as fases em que os requisitos do sistema são criados, revisados e atualizados ao longo do projeto. Essa definição garante a rastreabilidade e alinhamento contínuo entre as necessidades do sistema e sua implementação. Veja na tabela baixo mais detalhes de cada fase aplicada.

| **Fase** | **Descrição** | **Momento** |**Resultados** | **Rastreabilidade** |
|----------|---------------|-------------|---------------|---------------------|
| Criação | Documentação inicial dos requisitos do sistema com base no levantamento com stakeholders | Início de cada interação do projeto | requisitos funcionais e não funcionais criados com padrão definido | Sempre referenciando o commit com o prefixo feat e a identificação do requisito. Exemplos: "feat (RFxx): ...", "feat (RNFxx): ..." | 
| Revisão | Correção de erros ou ambiguidades nos requisitos existentes | Após testes, validações ou feedbacks internos | Ajustes nos textos ou regras dos requisitos |  Sempre referenciando o commit com o prefixo fix e a identificação do requisito. Exemplos: "fix (RFxx): ...", "fix (RNFxx): ..." | 
| Atualização | Modificações nos requisitos para refletir novas funcionalidades, melhorias ou mudanças externas | A cada nova demanda ou mudança de escopo | Versões novas dos requisitos funcionais ou não funcionais | Sempre referenciando o commit com o prefixo refactore e a identificação do requisito. Exemplos: "refactor (RFxx): ...", "refactor (RNFxx): ..." | 