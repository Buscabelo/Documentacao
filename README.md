# Documento de visão
 
## 1 - Resumo
 
O Buscabelo é uma solução que promove uma maior integração entre estabelecimentos de estética e o consumidor interessado em seus serviços. Temos o objetivo de ser uma ponte entre esses dois clientes, ajudando os consumidores na busca de serviços de estética de forma prática e os estabelecimentos a gerir melhor seu negócio.
 
## 2 - Clientes
 
### 2.1 - Consumidor
É o cliente ao qual busca praticidade e otimização do seu tempo, é vaidoso e gosta de ter serviços de qualidade com o preço adequado, para ele, nossa aplicação trará o conforto de agendar um serviço de estética específico do conforto da sua casa, podendo ele comparar preços e avaliações para um mesmo serviço e por fim agendar aonde se sentir mais confortável a ir.
 
### 2.2 - Estabelecimento
É o cliente ao qual busca organização, com uma ferramenta de gerência para seus atendimentos,facilitando os agendamentos dos seus serviços de forma prática.
 
## 3 - Problemas
#### 3.1 - Dificuldade em encontrar serviços de estética especializados
Devido a grande quantidade de estabelecimentos de estética, diferentes serviços e a busca por como cuidar melhor de sua aparência e de como se cuidar de forma saudável.

Os públicos, tanto feminino quanto masculino, têm tido certas dificuldades para encontrar serviços especializados e profissionais de qualidade e confiáveis.
 
### 3.2 - Dificuldade em comparar preços de serviços de estética em uma região
Como em alguns bairros há uma grande quantidade de estabelecimentos e na cidade em geral há vários estabelecimentos que oferecem o mesmo serviço, o consumidor pode ficar em dúvida de onde ir e de qual é melhor para ele. A ideia de comparar os preços de serviços é dar a opção ao consumidor de escolher um lugar em que ele se sinta confortável em pagar o preço que ele acha justo pelo serviço e qualidade do estabelecimento.
 
### 3.3 - Experiências negativas ao fazer agendamentos online
Alguns estabelecimentos possuem formas de agendamento de serviços, porém eles possuem dificuldade de usabilidade e trazem uma experiência de usuário negativa. Outros estabelecimentos não fazem agendamentos e trabalham por ordem de chegada dos seus clientes e fazem-os desperdiçar tempo para ser atendido. Nossa solução quer focar no conforto do consumidor, criando um ambiente onde ele possa ter uma experiência agradável ao fazer seu agendamento.

### 3.4 - Gestão de fluxo de clientes agendados
Na busca de praticidade e uma melhor gestão do estabelecimento, de forma a evitar registros manuais que podem gerar inconsistências e demandar um grande esforço para ter as informações do negocio registradas. Nosso sistema oferece uma forma simples de organizar o fluxo de agendamento dos clientes, reduzindo o indice de faltas dos mesmos, organizando a semana de atendimento dos funcionários, trazendo relatorios mensais e anuais do estabelecimento.
 
## 4 - Escopo
### 4.1 - O Buscabelo é
- Uma plataforma para buscar serviços e estabelecimentos de estética.
- Uma plataforma de agendamentos online de serviços de estética.
- Uma plataforma para gerência de fluxo de clientes de estabelecimentos de estética.
 
### 4.2 - O Buscabelo não é
- Uma plataforma para comprar perucas.
- Uma plataforma de delivery.
- Uma plataforma de compra.
- Uma plataforma de blog.
- Uma plataforma que faz intermedio de atendimento a domicilio.
 
### 4.3 - O Buscabelo faz
- Realiza a busca de serviços de beleza.
- Possibilita a filtragem da busca de serviços de beleza por região.
- Realiza o agendamento de serviços em estabelecimentos de beleza.
- Permite a avaliação de estabelecimentos de beleza ao qual o consumidor agendou o serviço.
- Permite ao consumidor o acesso ao histórico de serviços de beleza contratados.
- Permite ao estabelecimento de beleza o acesso ao histórico de clientes que contrataram seus serviços.
- Permite ao consumidor avaliar o serviço agendado após finalização do serviço. 
 
### 4.4 - O Buscabelo não faz
- Realizar pagamentos pela plataforma.
- Acompanhar a rota até o estabelecimento de beleza contratado pelo cliente na plataforma.
- Permitir avaliação pública.
 
## 5 - Usuários
### 5.1 Consumidor
- Utilizam a plataforma para encontrar estabelecimentos com serviços de beleza.
- Utilizam a plataforma para marcar horário em estabelecimentos de beleza.
 
#### 5.2 Estabelecimento de beleza
- Utilizam a plataforma para anunciar seus serviços de beleza.
- Utilizam a plataforma para exibir no perfil um quadro de horários para agendamento.
- Utilizam a plataforma para melhor gerência de seus atendimentos.
 
## 6 - Requisitos
### 6.2.1 Requisitos Funcionais
| Cód. | Nome | Descrição | Categoria |
| -------- | -------- | -------- | -------- |
| RF01 | Catalogar serviços e produtos | Possibilitar a catalogação dos serviços e produtos ofertados pelo estabelecimentos de beleza | Obrigatório
| RF02 | Agendar serviços de beleza | Possibilita que usuário consiga marcar um horário em comum com o estabelecimento para que o usuário tenha acesso ao serviço | Obrigatório
| RF03 | Avaliar estabelecimentos de beleza | Permitir que os usuários possam avaliar os serviços de beleza que utilizarem |  Obrigatório
| RF04 | Gerenciar atendimentos | Permite o usuário ter controle dos atendimento realizados no dia | Obrigatório
 
### 6.2.2 Requisitos não funcionais
| Cód. | Nome | Descrição | Categoria |
| -------- | -------- | -------- | -------- |
| NF01 | Stack JavaScript | O sistema deve ser desenvolvido utilizando tecnologias que sejam implementadas com JavaScript (React JS, Node.js, TypeScript)  | Obrigatório |
| NF02 | Sistema distribuído | O sistema deve ser um sistema distribuído | Obrigatório |
| NF03 | Banco de dados | O sistema deve utilizar o banco de dados PostgreSQL | Obrigatório |
 
## 7 - Regras de Negócios
- O agendamento estará disposto em faixas de horários personalizáveis pelo estabelecimento de beleza conforme a duração do serviço e a necessidade.
- Um estabelecimento de beleza oferta ao menos um serviço.
- Os serviços são listados de acordo com a pesquisa feita.
- A avaliação de um serviço é feita só depois da conclusão do serviço agendado.
- O consumidor e os estabelecimentos têm acessos diferentes à plataforma.

## 8 - Lista de casos de uso

1. [`Acessar dashboard`](casos_de_uso/acessarDashboard.md)
1. [`Acessar estabelecimento`](casos_de_uso/acessarEstabelecimento.md)
1. [`Acessar historico`](casos_de_uso/acessarHistorico.md)
1. [`Acessar serviço`](casos_de_uso/acessarServico.md)
1. [`Agendar horário`](casos_de_uso/agendarHorario.md)
1. [`Avaliar serviço`](casos_de_uso/avaliarServico.md)
1. [`Pesquisar`](casos_de_uso/buscarEstabelecimentoServico.md)
1. [`Cadastrar serviço`](casos_de_uso/cadastrarServico.md)
1. [`Acessar detalhes de agendamentos`](casos_de_uso/detalheAgendamento.md)
 
## 9 - Glossário
- Estabelecimentos: Salões de beleza e/ou barbearias.
- Serviços: Serviços de estética.
- Região: Bairro ou cidade.
 