# Desafio Técnico para Desenvolvedor Fullstack Pleno (Vue e Laravel)

Como desenvolvedor fullstack pleno com ênfase em Vue e Laravel, esperamos que você compreenda profundamente a estrutura e os recursos do Vue.js.

Para este desafio, extraímos um código legado que mistura JavaScript nativo com Vue, mas sem explorar todo o potencial do Vue. Seu principal objetivo será isolar a função `initCustom` que trabalha com CommonJS e reescrevê-la parcialmente utilizando Vue.js para alcançar o mesmo resultado.

## Instruções:

1. **Clone o Repositório**: Clone o repositório do GitHub ou visualize-o diretamente na plataforma.
2. **Acesse o Arquivo**: Abra o arquivo `index.vue`.
3. **Conteúdo HTML e Script Setup**: Dentro do `index.vue`, você encontrará conteúdo HTML utilizando `script setup` com Vue 3.
4. **Referência ao Arquivo Scripts**: O conteúdo é baseado em um arquivo dentro de `scripts` chamado `scripts/index.js`.
5. **Simulação de Reatividade**: O script atual realiza ações na página, simulando "reatividade".

## Objetivo:

Seu objetivo é demonstrar, através de código, como essa reatividade pode ser implementada diretamente no Vue.js, eliminando a necessidade do código legado (script/index.js).

## Requisitos:

- **Foco na Lógica e Conhecimentos de Vue**: Não é necessário trabalhar aspectos visuais, apenas a lógica e os recursos do Vue.js.
- **Demonstração de Melhorias**: Explique como você aproveitou os recursos do Vue.js para melhorar o código, tanto no código quanto em uma call de apresentação.

## O que será Avaliado:

- Capacidade de isolar e refatorar funções utilizando Vue.js.
- Entendimento profundo dos recursos do Vue.js e como aplicá-los de forma eficiente.
- Clareza e qualidade na explicação das soluções implementadas.

Esperamos que esta atividade lhe permita demonstrar sua habilidade com Vue.js e sua capacidade de transformar código legado em soluções modernas e eficientes. Boa sorte!

## Solução

1. Remoção da Dependência de CommonJS (scripts/index.js)

**Melhoria**: Eliminei a necessidade do arquivo scripts/index.js, migrando toda a lógica de manipulação de estado e eventos para o componente Vue (index.vue).

**Motivo**: Centralizar a lógica no componente Vue melhora a manutenção do código, facilita a compreensão e aproveita os recursos nativos de reatividade do Vue.js.

2. Utilização de Reatividade do Vue.js

**Melhoria**: Utilizei reactive e ref para gerenciar o estado e referências de forma reativa.

**Motivo**: A reatividade do Vue.js permite que as mudanças de estado sejam automaticamente refletidas na interface do usuário, eliminando a necessidade de manipulação manual do DOM.

3. Implementação de Métodos Vue.js

**Melhoria**: Transformei os métodos de manipulação de DOM e eventos em métodos do Vue.js dentro do componente index.vue.

**Motivo**: Encapsular a lógica de manipulação de eventos dentro de métodos Vue.js melhora a clareza e a integração com o ciclo de vida do Vue.

4. Integração da Biblioteca Coloris

**Melhoria**: Configurei e inicializei a biblioteca Coloris diretamente no onMounted do componente Vue.

**Motivo**: Inicializar bibliotecas de terceiros no momento certo do ciclo de vida do componente garante que os elementos DOM estejam disponíveis e prontos para interação.

5. Validação e Tratamento de Erros

**Melhoria**: Adicionei validação para garantir que um número de telefone seja fornecido quando a ação for whatsapp.

**Motivo**: Melhorar a experiência do usuário e evitar erros ao garantir que todas as informações necessárias estejam disponíveis antes de executar ações.

6. Envio de Dados com fetch

**Melhoria**: Implementei a lógica de envio de dados do template utilizando fetch para fazer uma requisição POST para uma API.

**Motivo**: Integrar a funcionalidade de salvamento de dados em um endpoint remoto permite que os templates sejam persistidos de forma segura e eficiente.

7. Estado de Carregamento

**Melhoria**: Adicionei um indicador de estado de carregamento (state.loading) durante o processo de salvamento.

**Motivo**: Informar o usuário sobre o estado atual do processo de salvamento melhora a usabilidade e a experiência do usuário.
