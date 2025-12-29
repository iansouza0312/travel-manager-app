# TPlanner - Aplicativo para gerenciamento de viagens

## Objetivo do projeto

- O projeto tem como seu principal objetivo auxiliar o usuário a organizar viagens à trabalho/lazer. O usuário pode criar um novo registro de viagem informando um título, data de início e data de fim. Dentro de cada viagem, o usuário pode planejar seu roteiro adicionando atividades para realizar em cada dia.

## Engenharia de requisitos

- A seguir, estão todos os requisitos funcionais e não-funcionais que a aplicação irá entregar ao usuário.

### Requisitos funcionais

1. O usuário cadastra um registro de viagem informando o local de destino, data de início, data de término, e-mails de convidados e também o seu nome completo e endereço;

2. O usuário que realiza a criação do registro recebe um e-mail para confirmação da viagem através de um link. Ao clicar no link, a viagem é confirmada, os convidados recebem e-mails de confirmação de presença e o usuário responsável pela criação da viagem é redirecionado para a página da viagem;

3. Os convidados, ao clicarem no link de confirmação de presença, são redirecionados para a aplicação onde devem inserir seu nome (além do e-mail que já estará preenchido) e então estarão confirmados na viagem;

4. Na página do evento, os participantes da viagem podem adicionar links importantes da viagem como reserva do AirBnB, locais que deseja visitar, etc ...;

5. Ainda na página da viagem, o cirador e os convidados podem adicionar atividades que irão ocorrer durante a viagem com um título, data e horário;

6. Novos participantes podem ser convidados dentro da página de viagem através do e-mail e asssim devem passar plo fluxo de confirmação como qualquer outro convidado

### Documentação da aplicação - MODELO C4

Para a documentação completá do projeto, irá ser utilizado o modelo C4, dividinvo a aplicação em camadas de contexto, container, componente e código

<br />

- [acessar documentação completa do projeto](./docs/)

### Passo-a-passo para a criação do projeto

- Criar projeto utilizando o `Spring initializr`

  - Spring web
  - Flyway
  - Dev tools
  - Lombok
  - JPA
  - H2 Database

- Configurar database da aplicação
- Criar migration para tabela `Trip`
- Criar entidades para representar a tabela `Trip`
- Criar repository da entidade viagem
- Criar endpoint de cadastro de viagem (**POST**)
  - /trips
- Criar endpoint de consulta de viagem (**GET**)
  - /trips/{tripId}

#### Importante saber

- Arquivos de Migration representam mudanças na estrutura de tabelas do DataBase
  - criar uma tabela
  - alterar tabela, remover campo, adicionar um campo
  - instalação de driver's
  - inserção em massa, de dados default
- Arquivos de Migration -> scripts SQL, p/ rodar comandos no DataBase
