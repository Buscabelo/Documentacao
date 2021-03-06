# Agendar Horário
## Descrição
O usuário escolhe um serviço e um horário disponível. Em seguida, um email é enviado para ambas as partes.

## Atores
- Cliente
  - Humano
  - Primário
  - Ativo
- Estabelecimento
  - Humano
  - Secundário
  - Passivo
- Servidor de email
  - Não humano
  - Secundário
  - Passivo

## Gatilhos
Não se aplica

## Pré-condições
- O usuário precisa estar autenticado ao sistema.

## Pós-condições
- Um email é enviado para o estabelecimento informando sobre o agendamento.
- É preenchido na dashboard do estabelecimentos os serviços futuros.
- Um email é enviado para o usuário informando sobre o agendamento.
- Uma faixa de horário é reservado para o agendamento do usuário.

## Fluxo Principal
_Após o caso de uso [`AcessarServico`](./acessarServico.md)_

1. O usuário seleciona a opção "Agendar"
1. O sistema mostra uma tela com um calendário
1. O usuário seleciona um dia disponível
1. O sistema mostra uma opção para escolher um intervalo de horário
1. O usuário seleciona um intervalo de horário
1. O sistema sinaliza a possibilidade de acionar o botão para finalizar agendamento
1. O usuário aperta o botão para confirmar o agendamento
1. O sistema exibe uma mensagem de confirmação de agendamento
1. O usuário confirma o agendamento.

**Ponto de extensão:**_
[`Detalhe do Agendamento`](./detalheAgendamento.md)

## Fluxos Alternativos
_Após o caso de uso [AcessarHistorico]_

O fluxo começa apartir do passo 2 do fluxo principal.

## Situações de Erro
### Não Há Faixa de Horário Disponível
Consequência: O usuário desiste de agendar horário. O caso de uso é cancelado.

### O Horário Desejado Foi Escolhido Por Outro Usuário Durante o Agendamento
Consequência: O usuário pode desistir de agendar horário, pois precisa reiniciar o caso de uso. O caso de uso é cancelado.

## Regra de negócio
O cliente agenda horário de um serviço em um estabelecimento, é enviado para o estabelecimento o horário e dia marcado, a informação vai para a dashboard de gerenciamento do estabelecimento e é notificado quando perto do dia marcado. O cliente também recebe um comprovante de horário marcado e também recebe notificação antes do horário agendado.

## Diagrama de Sequência do sistema
```mermaid
sequenceDiagram
  participant U as Usuario
  participant S as Sistema
  U->>+S: acessarSistema()
  S-->>-U: telaInicial(login, formulário de pesquisa)
  U->>+S: enviarTexto(texto)
  S-->>-U: telaResultados(estabelecimentos, serviços, filtro)
  U->>+S: acessarServiço(serviço)
  S-->>-U: telaServiço(descrição, profissionais, agendamento)
  U->>+S: agendar()
  S-->>-U: telaCalendário(datas, botão de finalizar)
  U->>+S: selecionarDia(data)
  S-->>-U: mostrarHorários(horarios)
  U->>+S: selecionarHorário(horario)
  S-->>-U: permitirFinalizar()
  U->>+S: confirmarAgendamento()
  S-->>-U: exibirConfirmação()
```
## Diagrama de Sequência
```mermaid
sequenceDiagram
  participant U as Usuario
  participant TI as TelaInicial
  participant TR as TelaResultado
  participant TS as TelaServiço
  participant TC as TelaCalendario
  participant CA as ControleAgendar
  participant BD as BancoDeDados

  U->>+CA: acessarSistema()
  #busca#
  CA->>+TI: criação() 
  CA-->>U: exibir(TI)
  U->>+TI: pesquisarEstabeleciomento(texto)
  TI->>+CA: pesquisarEstabeleciomento(texto)
  CA->>+BD: SELECT WHERE...
  BD->>+CA: estabelecimentos e serviços
  #busca#
  CA-->>-TR: criação(estabelecimentos, serviços)
  CA-->>+U: exibir(estabeleciomentos, serviço)
  #servico#
  U->>+TR: acessarServiço(serviço)
  TR->>+CA: acessarServiço(serviço)
  CA->>+BD:SELECT WHERE ID...
  BD->>+CA: retorna um serviço
  CA-->>-TS: criacao(descrição, profissionais, agendamento)
  CA-->+U: exibir(TS)
  #servico#
  #agendar#
  U->>+TS: agendar()
  TS->>+CA: agendar()
  CA->>+BD: SELECT...
  BD->>+CA: horarios 
  CA-->>-TC: criação(datas, botão de finalizar)
  TC-->>+U: exibir(calendario)
  #agendar#
  U->>+TC: confirmarAgendamento(horario)
  TC->>+CA: confirmarAgendamento(horario)
  CA->>+BD: INSERT
  BD->>+CA: query response
  CA-->>-TS: exibirConfirmação()
  TS-->>-U: exbir(TS)
```

_[`voltar para documento de visão`](../README.md)_
