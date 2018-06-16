# Aplicativo de pedido de merenda 

## Relatório de análise de requisitos

### 1. Declaração de necessidade	
<br> O campus São José do Instituto Federal de Santa Catarina futuramente terá uma distribuição de merenda gratuita no período noturno. Sendo assim, existe a necessidade de controle e organização da distribuição da merenda. </br>
<br>Para contribuir com o controle da merenda, foi sugerido, pelo servidor e diretor Saul Caetano, a criação de um aplicativo que irá saciar a necessidade do cliente.</br>

### 2. Viabilidade
<br> O sistema é viável porque é um aplicativo relativamente simples e não custará nada ao campus, totalmente feito pelos alunos, e pelo professor. O formato do sistema nos permite montá-lo na nossa respectiva linguagem de programação (JAVA), e será implementado num sistema Android.</br>


### 3. Declaração do escopo do sistema
<br> O aplicativo deve permitir que o aluno possa reservar uma merenda gratuita com antecedência para o seu devido dia. </br>

### 4. Lista de interessados que participaram do levantamento de requisitos

| NOME                        | INFO                                              |
|-----------------------------|---------------------------------------------------|
|      Saul Caetano           | Cliente                                           |
|Victor Cesconetto            | Analista de Sistema                               |

### 5. Descrição do ambiente técnico do sistema

<br> O aplicativo será desenvolvido para um sistema Android. Essas informações são transferidas para um banco de dados e a partir de relatórios os dados dos alunos serão tratados de acordo com as intenções do usuário. O tratamento será feito a partir de um sistema implementado na linguagem Java. </br>

### 6. Lista de requisitos
#### 6.1 Funcionais

<br>**RF1.** Permitir que o usuário reserve uma merenda no devido dia solicitado.</br>
<br>**RF2.** Permitir que o usuário visualize as merendas anteriores reservadas.</br>
<br>**RF3.** Permitir que o usuário possa cancelar a reserva de merenda até as 21:00 do dia anterior.</br>
<br>**RF4.** Permitir que o usuário possa reservar a merenda até 4 dias antes.</br>

#### 6.2 Não funcionais
<br>**RNF1.** O sistema deve possuir uma interface intuitiva.</br>
<br>**RNF2.** O sistema terá acesso a um banco de dados com as contas cadastradas de cada usuário.</br>
<br>**RNF3.** O sistema será implementado para celulares com Android.</br>
<br>**RNF4.** O sistema terá acesso a um banco de dados com os tickets(chaves) que serão convertidas em QRcode.</br>

### 7. Regras de negócio


| Regra | Descrição|
|-----------------------------|---------------------------------------------------|
|Autenticação do Usuário (RN01) | O aplicativo permitirá o aluno a reservar uma merenda no dia X |
|Reserva da merenda (RN02) | O aplicativo permitirá o aluno a reservar uma merenda no dia X |
|Cancelamento de pedido (RN03) | O aplicativo permitirá o aluno a cancelar uma reserva ate as 21hrs do dia anterior|
|Lista dos dias reservados (RN04)| O aplicativo gerará uma lista dos dias nos quais o aluno reservou a merenda|
|Tempo limite para a reserva (RN05) | O aplicativo permitirá ter um tempo limite de ate as 21hrs do dia anterior para a reserva |

### 8. Conjunto de cenários de uso

#### Autenticação do aplicativo (CSU01)
<br>Ator primário: Usuário.</br>
<br>Ator secundário: Base de dados com as contas de usuário cadastradas.</br>
<br>Resumo: O usuário faz a autenticação com seus dados cadastrais.</br>
<br>Fluxo Principal:</br>
1. O usuário abre o sistema.
2. O aplicativo abre sua tela principal com os campos de nome de usuário e senha para login.
3. O usuário informa seus dados cadastrados.
4. O aplicativo verifica a autenticidade dos dados. 
5. O aplicativo apresenta a primeira tela de menu ao usuário.
<br>Exceções:
Foram informados dados cadastrais incorretos (3). Veja caso “Erro ao se autenticar” (CSU02).</br>
&nbsp;
#### Erro ao se autenticar (CSU02)
&nbsp;
<br>Ator primário: Usuário.</br>
<br>Ator secundário: Base de dados com as contas de usuário cadastradas.</br>
<br>Resumo: O usuário erra os dados por três vezes.</br>
<br>Fluxo Principal:</br>
1- O usuário abre o sistema.
2- O aplicativo solicita o nome de usuário e senha para login.
3- O usuário informa seus dados cadastrados.
4- O aplicativo verifica a autenticidade dos dados.
5- O aplicativo mostra uma pop-up dizendo que os dados estão incorretos.
&nbsp;
#### Realizar pedido da merenda (CSU03)
&nbsp;
<br>Ator primário: Usuário.</br>
<br>Ator secundario: Base de dados com os tickets(códigos)</br>
<br>Pré-condição: O usuário está autenticado no sistema (ver CSU01).</br>
<br>Resumo: O usuário faz o pedido de merenda disponível para si no dia anterior.</br>
1. O usuário seleciona a opção de pedir merenda.
2. O aplicativo mostra um QRCode montado pelo ticket(código) na tela gerado pelo banco de dados.
3. O aplicativo armazena o ticket  na lista do histórico.
<br>Exceções:
Usuário quer cancelar o pedido(2). Veja caso “Cancelar pedido da merenda”(CSU04).</br>
&nbsp;
#### Cancelar pedido(CSU04)
&nbsp;
<br>Ator primário: Usuário</br>
<br>Pré-condição: O usuário está autenticado no sistema (ver CSU01).</br>
<br>Resumo: O usuário cancela o pedido da merenda.</br>
1. O usuário seleciona a opção de cancelar o pedido da merenda.
2. O aplicativo mostra uma pop-up informando que o pedido foi cancelado.
3. O usuário não poderá desfazer essa operação.


&nbsp;
#### Mostrar histórico de pedidos(CSU05)


&nbsp;
<br>Ator primário: Usuário</br>
<br>Ator secundário: Base de dados com o histórico dos tickets</br>
<br>Pré-condição: O usuário está autenticado no sistema (ver CSU01).</br>
<br>Resumo: O usuário requisita o histórico para a visualização dos pedidos anteriores.</br>
1. O usuário seleciona a opção de visualizar o histórico.
2. O aplicativo mostra todo o histórico de pedido.
&nbsp;
#### Mostrar histórico de pedidos(CSU05)

<br>Ator primário: Usuário</br>
<br>Ator secundário: Base de dados com o histórico dos tickets</br>
<br>Pré-condição: O usuário está autenticado no sistema (ver CSU01).</br>
<br>Resumo: O usuário requisita o histórico para a visualização dos pedidos anteriores.</br>
1.O usuário seleciona a opção de visualizar o histórico.
2.O aplicativo mostra todo o histórico de pedido.
&nbsp;
#### Mostrar cardápio(CSU06)
&nbsp;
<br>Ator primário: Usuário</br>
<br>Ator secundário: Base de dados com o cardapio da semana.</br>
<br>Pré-condição: O usuário está autenticado no sistema (ver CSU01).</br>
<br>Resumo: O usuario requisita visualizar o cardapio da semana.</br>
1.O usuario seleciona a opção de visualizar o cardapio.
2.O aplicativo mostra o cardapio da semana.










