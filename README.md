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

## Padrão de Diretórios dos Artefatos de Requisito

O projeto segue uma estrutura clara de pastas para ajudar na manutenção e colaboração em equipe. Dessa forma, para nortear a organização dos artefatos de requisitos do produto, adotou-se a seguinte hierarquia de diretórios:

documentos  
&nbsp;&nbsp;&nbsp;&nbsp;↳ requisitos  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↳ funcionais  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↳ nao-funcionais

Essa separação permite localizar rapidamente os arquivos e manter a rastreabilidade entre os tipos de requisito.

## Padrão de Nomenclatura dos Artefatos de Requisito

Para padronizar nomes, evitar confusões e facilitar buscas, foi adotado o seguinte padrão de nomeclatura dos artefatos:

- **Diretórios**: em minúsculas, sem pontuações e separados por hífem em vez de espaços; 

- **Requisitos**: em Markdown (.md) e nomeados com letras maiúsculas para destaque, além de iniciar com o prefixo **RF** para requisitos funcionais e **RNF** para requisitos não funcionais, sempre fornecendo o número de identificação posteriormente.

## Padrão de Artefato de Requisitos

Para garantir rastreabilidade e facilitar a validação dos requisitos ao longo do projeto, será adotado um modelo padronizado. Veja a seguir as regras de padronização dos requistos funcionais e não funcionais:

- **Requisitos funcionais** incluirão campos como caso de uso, fluxos, atores e tabelas de dados, permitindo compreender claramente o comportamento esperado do sistema. Dessa forma, o modelo definido deve conter os campos conforme a ordem seguinte:

    - **Identificador:** código único que permite identificar o requisito de forma rastreável;
    - **Caso de Uso:** nome objetivo da funcionalidade que representa o comportamento esperado do sistema;
    - **Descrição:** explica de forma clara o que o sistema deve fazer e qual o objetivo da funcionalidade, geralmente com o foco no usuário final e no propósito do requisito;
    - **Prioridade:** grau de importância da característica funcional para o sistema, normalmente definidas como **_Alta_**, **_Média_** e **_Baixa_**;
    - **Atores:** papeis de usuários ou sistemas externos que interagem com a funcionalidade;
    - **Pré-condições:** condições que precisam ser verdadeiras ou existentes antes do início da execução da funcionalidade.
    - **Pós-condições:** Estado esperado do sistema após a execução bem-sucedida da funcionalidade;
    - **Fluxos Principais:** sequência de passos padrão (cenário de sucesso) que o usuário e o sistema seguem para realizar a funcionalidade;
    - **Fluxos Alternativos:** Caminhos alternativos que o usuário pode seguir, mas que ainda resultam no sucesso da operação;
    - **Fluxos de Exceções:** Situações de erro ou imprevistos que podem ocorrer durante o fluxo, com as respectivas ações do sistema;
    - **Dependências:** outros requisitos que precisam estar presentes ou operacionais para que este requisito funcione corretamente.
    - **Cardinalidades:** Quantidade mínima e máxima de interações entre entidades envolvidas. Pode ser omitido se não houver impacto no requisito;
    - **Tabelas de Dados:** Define os dados usados ou manipulados pela funcionalidade Cada campo da tabela contém:
        - **Nome:** nome da informação;
        - **Tipo:** tipo de dado;
        - **Valor Obrigatório:** se o campo é ou não obrigatório ser preenchido;
        - **Restrições:** validações ou limitações; 
    - **Observações Extras:** informações adicionais relevantes que não se enquadram nos campos anteriores.

- **Requisitos não funcionais** terão estrutura simples com identificador, prioridade e categoria, focando em restrições e qualidades do sistema. Dessa forma, o modelo definido deve conter os campos conforme a ordem seguinte:

    - **Identificador:** código único que permite identificar o requisito de forma rastreável;
    - **Descrição:** explica a qualidade, restrição ou condição que o sistema deve cumprir, sem estar diretamente relacionado a uma funcionalidade específica.
    - **Prioridade:** grau de importância da característica não funcional para o sistema, normalmente definidas como **_Alta_**, **_Média_** e **_Baixa_**;
    - **Categoria:** classificação do requisito não funcional com base em seu foco, como:
        - **Segurança:** proteção de dados sensíveis;
        - **Capacidade:** armazenamento e processamento necessários;
        - **Compatibilidade:** suporte a sistemas e hardware;
        - **Disponibilidade:** estabilidade e tempo online;
        - **Manutenibilidade:** facilidade de suporte técnico;
        - **Escalabilidade:** crescimento sem perda de desempenho;
        - **Usabilidade:** facilidade e experiência do usuário;
        - **Desempenho:** tempo de resposta adequado;
        - **Conformidade:** atendimento a normas legais;
        - **Ambiental:** adaptação ao ambiente físico.
    - **Observações Extras:** informações adicionais relevantes que não se enquadram nos campos anteriores.

## Estrutura Padrão das Issues

As issues são usadas para planejar, distribuir e acompanhar as atividades do projeto. Elas estão localizadas no **[_Project (projeto)_](https://github.com/orgs/SysDoa/projects/1/views/1)** desta organização e cada uma deve conter informações completas para garantir entendimento e rastreabilidade. Neste contexto, o modelo adotado de issue/atividade segue o consecutivo padrão abaixo:

- **Identificador:** número de identificação de cada issue. É gerado automaticamente.
- **Título:** curto, claro e descritivo (ex: "Criar componente de listagem de doadores").
- **Descrição:** estruturada como uma história de usuário, no formato **Como** [papel], **Quero** [ação], **Para** [finalidade]. Além disso, também referenciado os **Requisitos Funcionais (RF)** e **Requisitos Não Funcioanis (RNF)**.
- **Prioridade (Priority):** nível de urgência classificadas em:
    - **P0:** crítica e bloqueia outras funcionalidades;
    - **P1:** importante, mas não bloqueia outras funcionalidades;
    - **P2:** pode ser feita depois, sem impacto imediato.
- **Construção (Construction):** tipo de evolução de artefato, podendo ser:
    - **Evolutiva (Evolutionary):** adiciona funcionalidades novas ou melhorias planejadas;
    - **Corretiva (Corrective):** corrige erros, falhas de lógica ou validações que impedem o funcionamento adequado;
    - **Adaptativa (Adaptive):** altera o sistema para se adaptar a mudanças externas.
- **Estimativa (Estimate):** tempo estimado para a execução (em dias).
- **Rótulos (Labels):** identificadores como bug, development, design, planning, etc.
- **Tamanho (Size):** complexidade da tarefa:
    - **XS:** ajuste simples (ex: correção de texto);
    - **S:** alteração pequena (ex: adicionar campo);
    - **M:** funcionalidade moderada (ex: novo formulário);
    - **L:** alteração abrangente (ex: lógica com múltiplos arquivos);
    - **XL:** atividade complexa ou com pesquisa/investigação.
- **Data de Início (Start Date) e Data de Fim (End Date):** para controle de tempo real de execução.
- **Interação (Iteration):** a qual sprint/interação a tarefa pertence (deve durar entre 15 a 30 dias).
- **Responsável (Assignees):** membro(s) atribuídos para executar a tarefa.

## Processo de Desenvolvimento de Artefatos de Requisitos

O processo de desenvolvimento de artefatos de requisitos estabelece as fases em que os requisitos do sistema são criados, revisados e atualizados ao longo do projeto. Essa definição garante a rastreabilidade e alinhamento contínuo entre as necessidades do sistema e sua implementação. Veja na tabela baixo mais detalhes de cada fase aplicada.

| **Fase** | **Descrição** | **Momento** |**Resultados** | **Rastreabilidade** |
|----------|---------------|-------------|---------------|---------------------|
| Criação | Documentação inicial dos requisitos do sistema com base no levantamento com stakeholders | Início de cada interação do projeto | requisitos funcionais e não funcionais criados com padrão definido | Sempre referenciando o commit com o prefixo feat e a identificação do requisito. Exemplos: "feat (RFxx): ...", "feat (RNFxx): ..." | 
| Revisão | Correção de erros ou ambiguidades nos requisitos existentes | Após testes, validações ou feedbacks internos | Ajustes nos textos ou regras dos requisitos |  Sempre referenciando o commit com o prefixo fix e a identificação do requisito. Exemplos: "fix (RFxx): ...", "fix (RNFxx): ..." | 
| Atualização | Modificações nos requisitos para refletir novas funcionalidades, melhorias ou mudanças externas | A cada nova demanda ou mudança de escopo | Versões novas dos requisitos funcionais ou não funcionais | Sempre referenciando o commit com o prefixo refactore e a identificação do requisito. Exemplos: "refactor (RFxx): ...", "refactor (RNFxx): ..." | 

