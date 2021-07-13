# Acessar Serviço
## Descrição
Na lista de resultado de pesquisa o usuário acessa um serviço.

## Atores
- Visitante
  - Humano
  - Primário
  - Ativo
- Cliente
  - Humano
  - Primário
  - Ativo
- Serviço
  - Não humano
  - Secundário
  - Passivo

## Pré-condições
Não se aplica

## Pós-condições
- A página de detalhes do serviço é mostrada na tela.

## Fluxo Principal
_Após o caso [`BuscarEstabelecimentoServico`](./buscarEstabeleciemntoServico.md)_

1. O usuário acessa a página de um serviço

__**Ponto de extensão:**_
[`Agendar horario`](./agendarHorario.md)
## Fluxos Alternativos
### Página de estabelecimento
1. A partir da página de estabelecimento o usuário pode acessar um serviço que faz parte daquele estabelecimento.

### Página de historico
1. A partir da página de historico o usuário pode acessar um serviço uma vez que já agendado.

## Regra de negócio
Acesso a pagina de um serviço.

_[`voltar para documento de visão`](../README.md)_
