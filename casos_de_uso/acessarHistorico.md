# Acessar histórico de serviços
## Descrição
Possibilita ao usuário visualizar o seu histórico de serviços

## Atores
Cliente
* Humano
* Primário
* Ativo

Estabelecimento
* Humano
* Principal
* Ativo

## Gatilhos
Não se aplica

## Pré-condições
A opção só estará disponível para um usuaŕios autenticado no sistema.

## Pós-condições
O usuário tem do sistema o retorno com os agendamentos já feitos. 

## Fluxo Principal
1. O usuário acessa a opção de histórico
2. O sistema retorna os agendamentos já realizados onde aquele usuário está vinculado (seja ele do tipo Cliente ou Estabelecimento)
 
_**ponto de extensão:**_
[`Detalhe de serviço`](./detalheAgendamento.md)
[`Agendar Horário`](./agendarHorario.md)

## Fluxo Alternativo
Não se aplica

## Regra de negócio
O usuário, sendo cliente ou estabelecimento, acessa a lista constando o histórico de serviços. Somente o cliente pode a partir do acesso ao histórico fazer um novo agendamento baseado nos serviços já desfrutados. 

_[`voltar para documento de visão`](../README.md)_
