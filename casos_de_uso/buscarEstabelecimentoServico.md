# Buscar (Estabelecimento/Serviço)
 
## Descrição
Resultado de pesquisa emitido após submissão no formulário de pesquisa da página inicial.
 
## Atores
- visitante
 - Humano
 - Primário
 - Ativo
- cliente
 - Humano
 - Primário
 - Ativo
- Estabelecimento
 - Humano
 - Secundário
 - Passivo

## Gatilhos
Não se aplica

## Pré-condições
Não se aplica.
 
## Pós-condições
- O visitante/consumidor tem acesso a uma lista de estabelecimentos/serviço do sistema.
 
## Fluxo Principal
1. O usuário acessa a tela inicial do buscabelo.
1. O usuário preenche o formulário de pesquisa e envia-o.
1. O sistema exibe a tela com resultados da pesquisa que contem opções de filtro, estabelecimentos e/ou serviços.
 
_**ponto de extensão:**_
[`Acessar Estabelecimento`](./CDU-AcessarEstabelecimento.md)
 
_**ponto de extensão:**_
[`Acessar Serviço`](./CDU-AcessarServico.md)
 
## Fluxos Alternativos
1. O usuário preenche o formulário de pesquisa de outra página que não seja a página inicial.
1. Volta ao fluxo principal
 
## Situações de Erro
1. O usuário envia um formulário vazio.
1. O sistema não permite a busca e informa ao usuário que ele deve preencher o campo de pesquisa.
 
## Rega de negócio
Resultado de pesquisa do cliente/visitante após pesquisar usando o formulário de pesquisa.
 
_[`voltar para documento de visão`](../README.md)_
