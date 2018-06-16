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

**RF1.** Permitir que o usuário reserve uma merenda no devido dia solicitado.
**RF2.** Permitir que o usuário visualize as merendas anteriores reservadas.
**RF3.** Permitir que o usuário possa cancelar a reserva de merenda até as 21:00 do dia anterior
**RF4.** Permitir que o usuário possa reservar a merenda até 4 dias antes.

#### 6.2 Não funcionais
**RNF1.** O sistema deve possuir uma interface intuitiva.
**RNF2.** O sistema terá acesso a um banco de dados com as contas cadastradas de cada usuário.
**RNF3.** O sistema será implementado para celulares com Android.
**RNF4.** O sistema terá acesso a um banco de dados com os tickets(chaves) que serão convertidas em QRcode.

### 7. Regras de negócio


|Autenticação do Usuário (RN01)|
|Descrição | O sistema permitirá o aluno a reservar uma merenda no dia X |



