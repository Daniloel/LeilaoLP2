# LeilaoLP2
Necessidades a serem atendidas
Devido aos constantes produtos e imóveis apreendidos pela Receita Federal do Brasil, o
governo Brasileiro identificou a necessidade de desenvolver um Sistema de Leilões Eletrônicos
mais robusto e simples que o atual Sistema de Leilões Eletrônicos (SLE) já existente e usado
através do portal eCAC.
Visando direcionar melhor o escopo inicial deste sistema, a Receita Federal pretende
direcioná-lo somente para leilões de dispositivos de informática (notebooks, monitores, hubs,
switches e roteadores) e veículos (carros e motocicletas de passeio, caminhões e utilitários)
apreendidos.
Para tal, o sistema que está sendo solicitado deve conter:
Funcionalidades Básicas
1. Registro, consulta, atualização e remoção de dispositivos de informática a serem leiloados
(dentre os tipos acima destacados) – os detalhes dos dados a serem trabalhados para
representar os dispositivos fazem parte da pesquisa a ser realizada sobre o domínio do
sistema;
2. Registro, consulta, atualização e remoção de veículos a serem leiloados (dentre os tipos
acima destacados) – os detalhes dos dados a serem trabalhados para representar o
imóveis fazem parte da pesquisa a ser realizada sobre o domínio do sistema;
3. Registro, consulta, atualização e remoção dos leilões, constando a data de sua ocorrência
(futura), data de visitação dos itens do leilão, local em que o leilão ocorrerá e demais
detalhes pertinentes ao domínio de um leilão eletrônico (pesquisem), mas que também
terá entrada física no local (endereço, cidade e estado) de sua ocorrência;
4. Operações relacionadas a associação dos produtos registrados (dispositivos de
informática e/ou veículos) ao seu respectivo leilão;
a. O registro de produtos deve ser independente do leilão, porém no momento de
seu cadastro, obrigatoriamente eles deverão estar vinculados a um leilão já
registrado; e
b. Deve ser possível desassociar um item de leilão que não tenha sido VENDIDO (que
não recebeu lance) do atual, associando-o a outro leilão futuro (respeitando a
obrigatoriedade de um item de leilão sempre estar associado a um leilão presente
ou futuro.
5. Registro, consulta, atualização e remoção dos dados de cada Cliente autorizado a interagir
com o sistema, fornecendo lances e consultando os detalhes dos produtos anunciados no
leilão, bem como os leilões a serem realizados; e
6. Registro, consulta, atualização e remoção das instituições financeiras responsáveis pela
quitação das transações fechadas durante os leilões. Cada leilão terá ao menos uma
entidade financeira associada ao mesmo (CNPJ) e seus dados deverão estar disponíveis
aos clientes nas operações de consulta e detalhes do leilão.
Funcionalidades da Operação do Sistema de Leilão Eletrônico
1. Listagem dos leilões registrados no sistema, ordenados por data de ocorrência;
2. Detalhamento de um leilão específico, apresentando seu detalhes (lista de produtos
ordenado por nome, entidade financeira associada, dados do leilão, quantidade total de
produtos e demais dados pertinentes ao domínio);
3. Detalhamento de um produto associado ao leilão, apresentando todos os dados
pertinentes ao mesmo;
4. Filtro de busca de produtos em um leilão por:
a. Faixa de valores do lance inicial (min < R$ < max), sendo os valores mínimos e
máximos informados pelo usuário;
b. Faixa de valores considerando o lance inicial + lances adicionais (min < R$ < max),
sendo os valores mínimos e máximos informados pelo usuário;
c. Palavra chave contida no nome do produto; e
d. Tipo de produto.
5. Possibilitar a um cliente previamente cadastrado no sistema dar um lance de valor (R$)
para um produto específico – As devidas validações deverão ser mapeadas e
implementadas pelos membros do grupo em relação à regras de consistência dos lances
registrados;
6. Apresentação do histórico de lances realizado para um produto específico, destacando o
produto, cliente e valor do lance – Ordenação pelo ID do lance correspondente;
7. Sistema deverá automaticamente analisar a faixa de horário do leilão (início e fim), caso
o mesmo esteja ocorrendo no momento correspondente. Uma vez ultrapassado o
horário de finalização, ao consultar o detalhamento do leilão, o sistema deverá
apresentar a relação de produtos acompanhado de seus respectivos clientes
(ganhadores do leilão, caso o status seja FINALIZADO, senão não deverá apresentar o
cliente), valor do lance vencedor (R$) e o status de atua do leilão;
8. Todo leilão deverá ter atrelado ao mesmo três status chaves:
a. EM ABERTO - Para leilões registrados, porém ainda não iniciados;
b. EM ANDAMENTO - Para leilões registrados, cuja data e faixa de horário do leilão
estiverem ocorrendo no exato momento de operação do sistema; e
c. FINALIZADO – Para leilões cujo horário atual ultrapassou os limites da faixa de
horário registrada para ocorrência do leilão.
d. Observação: A gestão e tratamento dos status do leilão deverá ser executada
automaticamente pelo sistema, ou seja, não haverá funcionalidade para indicar
que o leilão foi registrado, iniciou-se ou foi finalizado. Isso deve ser processado
com base no horário atual e horários e início e fim do leilão.
9. O sistema deverá prover também uma funcionalidade de exportação dos detalhes do
leilão para um arquivo com extensão .DET contendo todas as informações do leilão,
seus produtos, clientes participantes do leilão, entidade financeira associada e histórico
de lances de cada produto (estrutura interna do arquivo será JSON).
10. Toda e qualquer persistência de dados da aplicação deverá ser implementada em
memória, simulando os registros de Objetos que seriam persistidos na base de dados,
porém mantendo-os na memória ou em um embedded database (H2, SQLite, Apache
Derby, HSQLDB). Consultas, registros, atualização e remoções deverão ser realizadas na
estrutura usada para armazenar tais registros;
11. Todas as operações descritas nos requisitos deverão ser executadas através de APIs
REST. Para consumo dessas APIs deverá ser criada a documentação Swagger de todas as
APIs desenvolvidas, considerando:
a. URL
b. Parâmetros do request payload (body, query, URL)
c. Parâmetros do response payload
d. HTTP status code para o sucesso da operação e tratamentos de erro
implementados
12. O código fonte do projeto do trabalho deverá ser entregue através de um repositório
Git via Github ou GitLab.
Boa
