# 3. DOCUMENTO DE ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE

Nesta parte do trabalho você deve detalhar a documentação dos requisitos do sistema proposto de acordo com as seções a seguir. Ressalta-se que aqui é utilizado como exemplo um sistema de gestão de cursos de aperfeiçoamento.

## 3.1 Objetivos deste documento
Descrever e especificar as necessidades da Coordenação do Curso de Sistemas de Informação da PUC Minas que devem ser atendidas pelo projeto SCCA – Sistema de Cadastro de Cursos de Aperfeiçoamento.

## 3.2 Escopo do produto

### 3.2.1 Nome do produto e seus componentes principais
O produto será denominado SCCA – Sistema de Cadastro de Cursos de Aperfeiçoamento. Ele terá somente um componente (módulo) com os devidos elementos necessários à gestão de cursos.

### 3.2.2 Missão do produto
Gerenciar informações sobre a oferta de cursos de aperfeiçoamento, gerenciar a composição das turmas, alunos, professores e matrículas. 

### 3.2.3 Limites do produto
O SCCA não fornece nenhuma forma de avaliação de alunos, pagamento de parcelas do curso, pagamento a professore e agendamentos. O SCCA não contempla o atendimento a vários cursos de Sistemas de Informação de outras unidades da PUC Minas.

### 3.2.4 Benefícios do produto

| # | Benefício | Valor para o Cliente |
|--------------------|------------------------------------|----------------------------------------|
|1	| Facilidade no cadastro de dados |	Essencial |
|2 | Facilidade na recuperação de informações | Essencial | 
|3 | Segurança no cadastro de matrículas | Essencial | 
|4	| Melhoria na comunicação com os alunos	| Recomendável | 

## 3.3 Descrição geral do produto

### 3.3.1 Requisitos Funcionais

| Código | Requisito Funcional (Funcionalidade) | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| RF1 | Gerenciar receitas |	Processamento de Inclusão, Alteração, Exclusão e Consulta de Receitas |
| RF2 |	Gerenciar usuários	| Processamento de Inclusão, Alteração, Exclusão e Consulta de Usuários |
| RF3	| Gerenciar avaliações de receitas |	Processamento de Inclusão, Alteração, Exclusão e Consulta de Avaliações de Receitas |
| RF4 |	Gerenciar receitas favoritadas	| Processamento de Inclusão, Exclusão e Consulta de receitas na lista de receitas favoritadas de um usuário |
| RF5 | Gerenciar alimentos/ingredientes	| Processamento de Inclusão, Exclusão e Consulta de Ingredientes (apenas para admin) |
| RF6 | Gerenciar comentários de cada receita	| Processamento de Inclusão, Exclusão e Consulta de Comentários |
| RF7 |	Gerenciar categorias de receitas	| Processamento de Inclusão, Exclusão e Consulta de Categorias de Receitas (apenas para admin) |
| RF8 |	Gerenciar categorias de ingredientes	| Processamento de Inclusão, Exclusão e Consulta de Categorias de Ingredientes (apenas para admin) |
| RF9 |	Gerenciar sugestões	| Listar sugestões de receitas relacionadas com o que o usuário já pesquisou |
| RF10 | Requisitar a adição de ingredientes	| Processamento de Inclusão de Solicitações para adicionar mais ingredientes no sistema |
| RF11 | Gerenciar solicitação de adição de ingredientes	| Processamento de Consulta, Aprovação e Rejeição de Solicitações para adicionar mais ingredientes no sistema (apenas para admin) |
| RF12 | Enviar notificações de novas receitas | Envio de notificação para usuários quando novas receitas de gostos similares forem adicionadas |
| RF13 | Gerenciar preferências | Processamento de Inclusão, Alteração, Exclusão e Consulta de Preferências para sugestões e notificações de receitas |
| RF14 | Gerenciar usuários seguidos | Processamento de Inclusão, Exclusão e Consulta de usuários seguidos por outro usuário |
| RF15 | Visualizar usuários seguidores | Consulta de usuários seguidores |
| RF16 | Gerenciar cardápios | Processamento de Inclusão, Alteração, Exclusão e Consulta de Cardápios utilizando receitas escolhidas pelo usuário |
| RF17 | Gerenciar lista de casa/compras | Processamento de Alteração e Consulta da lista de ingredientes que o usuário possui em casa e da lista dos que precisam ser comprados para uma receita de sua escolha |
| RF18 | Tornar o perfil parceiro (nutricionistas/restaurantes) | Usuário pode pagar para tornar seu perfil parceiro |

### 3.3.2 Requisitos Não Funcionais

| Código | Requisito Não Funcional (Restrição) |
|--------------------|------------------------------------|
| RNF1 | O ambiente operacional a ser utilizado é o Windows 10/11. |
| RNF2 | Responsividade para telas mobile. |
| RNF3 |	O produto deve restringir o acesso por meio de senhas individuais para o usuário. |
| RFN4 |	O sistema deve ser codificado usando javascript. |
| RFN5 | O sistema deve ser compatível com navegador Chrome e Firefox. |
| RFN6 | O sistema deve ser capaz de fazer uma busca em menos de 2 minutos. |

### 3.3.3 Usuários 

| Ator | Descrição |
|--------------------|------------------------------------|
| Administrador |	Usuário gerente do sistema responsável pelo cadastro e manutenção de novos itens. Possui acesso geral ao sistema. |
| Usuário |	Usuário responsável por registros de receita, comentarios, e avaliações. |


## 3.4 Modelagem do Sistema

### 3.4.1 Diagrama de Casos de Uso
Como observado no diagrama de casos de uso da Figura 1, a secretária poderá gerenciar as matrículas e professores no sistema, enquanto o coordenador, além dessas funções, poderá gerenciar os cursos de aperfeiçoamento.

#### Figura 1: Diagrama de Casos de Uso do Sistema.

![image](https://github.com/user-attachments/assets/af08bf15-04b0-49ba-aee2-c4e8cfad6c34)


 
### 3.4.2 Descrições de Casos de Uso

Cada caso de uso deve ter a sua descrição representada nesta seção. Exemplo:

#### Gerenciar Professor (CSU01)

Sumário: A Secretária realiza a gestão (inclusão, remoção, alteração e consulta) dos dados sobre professores.

Ator Primário: Secretária.

Ator Secundário: Coordenador.

Pré-condições: A Secretária deve ser validada pelo Sistema.

Fluxo Principal:

1) 	A Secretária requisita manutenção de professores.
2) 	O Sistema apresenta as operações que podem ser realizadas: inclusão de um novo professor, alteração de um professor, a exclusão de um professor e a consulta de dados de um professor.
3) 	A Secretária seleciona a operação desejada: Inclusão, Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
4) 	Se a Secretária desejar continuar com a gestão de professores, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (3): Inclusão

a)	A Secretária requisita a inclusão de um professor. <br>
b)	O Sistema apresenta uma janela solicitando o CPF do professor a ser cadastrado. <br>
c)	A Secretária fornece o dado solicitado. <br>
d)	O Sistema verifica se o professor já está cadastrado. Se sim, o Sistema reporta o fato e volta ao início; caso contrário, apresenta um formulário em branco para que os detalhes do professor (Código, Nome, Endereço, CEP, Estado, Cidade, Bairro, Telefone, Identidade, Sexo, Fax, CPF, Data do Cadastro e Observação) sejam incluídos. <br>
e)	A Secretária fornece os detalhes do novo professor. <br>
f)	O Sistema verifica a validade dos dados. Se os dados forem válidos, inclui o novo professor e a grade listando os professores cadastrados é atualizada; caso contrário, o Sistema reporta o fato, solicita novos dados e repete a verificação. <br>

Fluxo Alternativo (3): Remoção

a)	A Secretária seleciona um professor e requisita ao Sistema que o remova. <br>
b)	Se o professor pode ser removido, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato. <br>

Fluxo Alternativo (3): Alteração

a)	A Secretária altera um ou mais dos detalhes do professor e requisita sua atualização. <br>
b)	O Sistema verifica a validade dos dados e, se eles forem válidos, altera os dados na lista de professores, caso contrário, o erro é reportado. <br>
 
Fluxo Alternativo (3): Consulta

a)	A Secretária opta por pesquisar pelo nome ou código e solicita a consulta sobre a lista de professores. <br>
b)	O Sistema apresenta uma lista professores. <br>
c)	A Secretária seleciona o professor. <br>
d)	O Sistema apresenta os detalhes do professor no formulário de professores. <br>

Pós-condições: Um professor foi inserido ou removido, seus dados foram alterados ou apresentados na tela.

### 3.4.3 Diagrama de Classes 

A Figura 2 mostra o diagrama de classes do sistema. A Matrícula deve conter a identificação do funcionário responsável pelo registro, bem com os dados do aluno e turmas. Para uma disciplina podemos ter diversas turmas, mas apenas um professor responsável por ela.

#### Figura 2: Diagrama de Classes do Sistema.
 
![image](https://github.com/user-attachments/assets/2d6c2381-7883-44b5-8623-abca7def1d04)

### 3.4.4 Descrições das Classes 

| # | Nome | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| 1	|	Usuário |	Cadastro de informações relativas aos usuários. |
| 2	|	Administrador |	Cadastro de informações relativas ao usuário do tipo administrador. |
| 3	| Ingredientes |	Cadastro geral de itens e ingredientes. |
| 4 |	Receita |	Cadastro de receitas. |
| 5 |	Avaliação |	Cadastro de avaliação de uma receita. |
| 6	|	Comentário |	Cadastro de comentários de uma receita. |
| 7	|	Categoria de ingrediente |	Cadastro de categoria para ingredientes. |
| 8	|	Categoria de receita |	Cadastro de categoria para receitas. |
| 9	|	Preferências |	Cadastro de categorias como preferidas. |
| 10	|	Solicitação |	Cadastro de solicitação de ingredientes e de categorias. |
