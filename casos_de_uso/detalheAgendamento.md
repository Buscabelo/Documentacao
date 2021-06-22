# Detalhe do Agendamento
## Descrição
Apresentar detalhamento de um agendamento.

## Atores
- Cliente
  - Humano
  - Primário
  - Ativo

- Estabelecimento
  - Humano
  - Primário
  - Ativo

## Gatilhos
- Criação do agendamento

## Pré-condições
- Ter um agendamento criado
- Estar autenticado

## Pós-condições
- Visualizar as informações detalhadas do agendamento selecionado

## Fluxo Principal
_Após o caso de uso [`Agendar Horário`](./agendarHorario.md)_
1. Cliente é redirecionado para uma página com os detalhes do agendamento

## Fluxos Alternativos
_Após o caso de uso [`Acessar Histórico`](./acessoHistorico.md)_
1. Cliente ou Estabelecimento serão redirecionados para página com detalhes de agendamentos que constam no histórico 

_Após o caso de uso [`Acessar Dashboard`](./acessarDashboard.md)_
1. Estabelecimento é redirecionado para página com detalhes de agendamentos que constam no histórico

## Situações de Erro
Não se aplica
## Rega de negócio
Exibe os detalhes de um agendamento, indepente se o serviço referente ao agendamento foi realizado ou não.

_[`voltar para documento de visão`](../README.md)_
