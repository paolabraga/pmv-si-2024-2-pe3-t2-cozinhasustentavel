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
| RF9 |	Gerenciar sugestões de receitas	| Listar sugestões de receitas relacionadas com o que o usuário já pesquisou |
| RF10 | Requisitar a adição de ingredientes/categorias	| Processamento de Inclusão de Solicitações para adicionar mais ingredientes ou categorias no sistema |
| RF11 | Gerenciar solicitação de adição de ingredientes/categorias	| Processamento de Consulta, Aprovação e Rejeição de Solicitações para adicionar mais ingredientes ou categorias no sistema (apenas para admin) |
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
Como observado no diagrama de casos de uso da Figura 1, a usuário pode gerenciar suas receitas, seu perfil, suas avaliações e comentários em receitas de outros usuários, suas receitas favoritadas, suas preferências, seus usuários seguidos, seus cardápios e sua lista de casa/compra. Ele também pode requisitar a adição de novos ingredientes e categorias ao usuário administrador, visualizar seus usuários seguidores e tornar seu perfil parceiro. O usuário administrador é responsável por gerenciar a lista de ingredientes, as categorias de ingredientes e categorias de receitas e as solicitações de adição de novos ingredientes e categorias ao sistema.

#### Figura 1: Diagrama de Casos de Uso do Sistema.

![image](https://github.com/user-attachments/assets/aec67690-903c-4365-b6f1-0570fd0f1417)



 
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

---

#### Gerenciar Receitas (CSU01)

Sumário: O Usuário realiza a gestão (inclusão, remoção, alteração e consulta) dos dados sobre as receitas.

Ator Primário: Usuário.

Pré-condições: O Usuário deve estar cadastrado e logado no sistema.

Fluxo Principal:

1) 	O Usuário entra na página de suas receitas.
2) 	O Sistema apresenta as operações que podem ser realizadas: inclusão de uma nova receita, alteração de uma receita, a exclusão de um receita e a consulta de dados de uma receita.
3) 	O Usuário seleciona a operação desejada: Inclusão, Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
4) 	Se o Usuário desejar continuar com a gestão de receitas, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a)	O Usuário requisita a inclusão de uma receita. <br>
b)	O Sistema apresenta uma janela solicitando o título da receita, os ingredientes, o modo de preparo e a categoria em que ela se encaixa, se disponível. <br>
c)	O Usuário fornece as informações solicitadas. <br>
d)	O Sistema verifica se o título ou o modo de preparo possuem algum caractere inválido, se sim ele mostra um erro ao Usuário para que os campos sejam corrigidos. Senão ele realiza a inclusão da nova receita. <br>

Fluxo Alternativo (2): Remoção

a)	O Usuário seleciona uma de suas receitas e requisita ao Sistema que a remova. <br>
b)	Se a receita pode ser removida, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato. <br>

Fluxo Alternativo (3): Alteração

a)	O Usuário altera um ou mais dos detalhes da receita e requisita sua atualização. <br>
b)	O Sistema verifica a validade dos dados e, se eles forem válidos, altera os dados na lista de receitas, caso contrário, o erro é reportado. <br>
 
Fluxo Alternativo (4): Consulta 

I) Fluxo se a receita for do usuário logado:
a) O Usuário seleciona uma de suas receitas. <br>
b)	O Sistema apresenta as informações da receita na página de detalhes da receita. <br>

II) Fluxo se a receita for de outro usuário:
a)	O Usuário opta por pesquisar por palavras do título da receita ou por categoria da receita e solicita a consulta sobre a lista de receitas. <br>
b)	O Sistema apresenta uma lista de receitas. <br>
c) O Usuário seleciona uma das receitas. <br>
d)	O Sistema apresenta as informações da receita na página de detalhes da receita. <br>

Pós-condições: Uma receita foi inserida ou removida, seus dados foram alterados ou apresentados na tela.

---

#### Gerenciar usuários (CSU02)

Sumário: O Usuário realiza a gestão (inclusão, remoção, alteração e consulta) dos dados sobre seu perfil.

Ator Primário: Usuário.

Pré-condições: Realização do fluxo de cadastro do Usuário e logar na aplicação.

Fluxo de Inclusão: 

a)	O Usuário acessa a página de cadastro. <br>
b)	O Sistema apresenta uma janela solicitando seu nome completo, email e a senha que deseja usar. <br>
c)	O Usuário fornece as informações solicitadas. <br>
d)	O Sistema verifica se todos os campos contém informações válidas, se sim ele realiza a inclusão do novo Usuário. Senão mostra um erro ao Usuário para que os campos sejam corrigidos. <br>

Fluxo Principal: Consulta

1) 	O Usuário entra na sua página de perfil.
2) 	O Sistema apresenta os dados do Usuário e as operações que podem ser realizadas: alteração de seus dados pessoais e a exclusão de seu perfil.
3) 	O Usuário seleciona a operação desejada: Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
4) 	Se o Usuário desejar continuar com a gestão de seu perfil, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (1): Remoção

a)	O Usuário seleciona a opção de excluir seu perfil. <br>
b)	O Sistema realiza a remoção; caso contrário, o Sistema reporta o fato. <br>

Fluxo Alternativo (2): Alteração

a)	O Usuário altera um ou mais dos detalhes do seu perfil e requisita sua atualização. <br>
b)	O Sistema verifica a validade dos dados e, se eles forem válidos, altera os dados no seu cadastro, caso contrário, o erro é reportado. <br>

Pós-condições: Um Usuário foi inserido ou removido, seus dados foram alterados ou apresentados na tela.

---

#### Gerenciar avaliações de receitas (CSU03)

Sumário: O Usuário realiza a gestão (inclusão, remoção, alteração e consulta) das avaliações de receitas.

Ator Primário: Usuário.

Pré-condições: O Usuário deve estar cadastrado e logado no sistema.

Fluxo Principal:

1) 	O Usuário entra na página de uma receita que pertence a outro Usuário.
2) 	O Sistema apresenta as operações que podem ser realizadas: inclusão de uma avalição, ou alteração e exclusão de uma avaliação do Usuário já existe na receita escolhida.
3) 	O Usuário seleciona a operação desejada: Inclusão , Alteração ou Exclusão, ou opta por finalizar o caso de uso.
4) 	Se o Usuário desejar continuar com a gestão de avaliações de receitas, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a)	O Usuário clica em um valor de 1 a 5 para a avaliação da receita selecionada. <br>
b)	O Sistema realiza a inclusão da avaliação; caso contrário, o Sistema reporta o fato. <br>

Fluxo Alternativo (2): Alteração

a)	O Usuário altera o valor de uma avaliação já existente. <br>
b)	O Sistema altera o valor dessa avaliação para dada receita, caso contrário, o erro é reportado. <br>

Fluxo Alternativo (3): Remoção

a) O Usuário seleciona uma avaliação e requisita ao Sistema que a remova.  
b) Se a avaliação pode ser removida, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (4): Consulta

a) O Usuário seleciona uma receita, sua ou de outro usuário, e consegue visualizar o valor da média das avaliações para a receita escolhida

Pós-condições: Uma avaliação foi inserida ou removida, seu valor foi alterado ou apresentado na tela (em conjunto com os valores de outras avaliações da mesma receita).

---

#### Gerenciar receitas favoritadas (CSU04)

Sumário: O Usuário realiza a gestão (inclusão, remoção, alteração e consulta) de receitas favoritadas.

Ator Primário: Usuário.

Pré-condições: O Usuário deve estar cadastrado e logado no sistema.

Fluxo Principal:

1) 	O Usuário entra na página de uma receita que pertence a outro usuário.
2) 	O Sistema apresenta as operações que podem ser realizadas: inclusão da receita na lista de receitas favoritadas do usuário ou exclusão de uma receita da lista.
3) 	O Usuário seleciona a operação desejada: Inclusão ou Exclusão, ou opta por finalizar o caso de uso.
4) 	Se o Usuário desejar continuar com a gestão de receitas favoritadas, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a)	O Usuário clica no botão de favoritar uma receita selecionada. <br>
b)	O Sistema realiza a inclusão da receita na lista de receitas favoritas do usuário; caso contrário, o Sistema reporta o fato. <br>

Fluxo Alternativo (2): Remoção

a) O Usuário seleciona uma receita da sua lista de receitas favoritas e requisita ao Sistema que a remova.  
b) Se a receitas favoritada pode ser removida, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (3): Consulta

a) O Usuário entra na sua página de receitas favoritadas e consegue visualizar a sua lista de receitas favoritas com os dados de cada receita.

Pós-condições: Uma receita foi inserida ou removida da lista de receitas favoritas do usuário, a lista foi apresentada na tela.

---

#### Gerenciar alimentos/ingredientes (CSU05)

Sumário: O Admin realiza a gestão (inclusão, remoção, alteração e consulta) de Ingredientes.

Ator Primário: Admin.

Pré-condições: O Admin deve estar cadastrado e logado no sistema.

Fluxo Principal:

1) O Admin entra na pagina de gerenciar ingredientes.
2) O Sistema apresenta as operações que podem ser realizadas: adição de um ingrediente, exclusão ou alteração de um ingrediente já existente.
3) O Admin seleciona a operação desejada: adição, exclusão ou alteração, ou opta por finalizar o caso de uso.
4) Se o Admin desejar continuar com a gestão de ingredientes, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a) O Admin requisita a inclusão de um ingrediente. <br>
b) O Sistema apresenta uma janela solicitando o nome do ingrediente. <br>
c) O Admin fornece as informações solicitadas. <br>
d) O Sistema verifica se o nome do ingrediente possui algum caractere inválido, se sim ele mostra um erro ao Admin para que os campos sejam corrigidos. Senão ele realiza a inclusão do ingrediente na lista de ingredientes.

Fluxo Alternativo (2): Alteração

a) O Admin altera o nome do ingrediente e requisita sua atualização. <br>
b) O Sistema verifica a validade dos dados e, se eles forem válidos, altera os dados na lista de ingredientes, caso contrário, o erro é reportado.

Fluxo Alternativo (3): Remoção

a) O Admin seleciona um ingrediente e requisita ao Sistema que o remova. <br>
b) Se o ingrediente pode ser removido, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (4): Consulta

a) O Usuário deseja adicionar um ingrediente em sua receita. <br>
b) O Sistema apresenta uma lista de ingredientes.

Pós-condições: Um ingrediente foi inserido ou removido, seus dados foram alterados ou apresentados na tela.

---

#### Gerenciar comentários de cada receita (CSU06)

Sumário: O Usuário realiza a gestão (inclusão, remoção, alteração e consulta) de Comentários.

Ator Primário: Usuário.

Pré-condições: O Usuário deve estar cadastrado e logado no sistema.

Fluxo Principal:

1) O Usuário entra na página de uma receita que pertence a outro Usuário.
2) O Sistema apresenta as operações que podem ser realizadas: adição de um comentário, exclusão ou alteração de um comentário já existente.
3) O Usuário seleciona a operação desejada: adição, exclusão ou alteração, ou opta por finalizar o caso de uso.
4) Se o Usuário desejar continuar com a gestão de comentários, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a) O Usuário digita o comentário que quer fazer na receita selecionada. <br>
b) O Sistema realiza a inclusão do comentário; caso contrário, o erro é reportado.

Fluxo Alternativo (2): Alteração

a) O Usuário altera o texto de um comentário já existente. <br>
b) O Sistema altera o texto desse comentário para dada receita, caso contrário, o erro é reportado.

Fluxo Alternativo (3): Remoção

a) O Usuário seleciona um comentário e requisita ao Sistema que o remova. <br>
b) Se o comentário pode ser removido, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (4): Consulta

a) O Usuário seleciona uma receita, sua ou de outro usuário, e consegue visualizar os comentários postados nesta receita.

Pós-condições: Um Comentário foi inserido ou removido, seus dados foram alterados ou apresentados na tela.

---

#### Gerenciar categorias de receitas (CSU07)

Sumário: O Admin realiza a gestão (inclusão, remoção, alteração e consulta) de Categorias de Receitas.

Ator Primário: Admin.

Pré-condições: O Admin deve estar cadastrado e logado no sistema.

Fluxo Principal:

1) O Admin entra na pagina de gerenciamento de categorias de receitas.
2) O Sistema apresenta as operações que podem ser realizadas: adição de uma categoria, exclusão ou alteração de uma categoria já existente.
3) O Usuário seleciona a operação desejada: adição, exclusão ou alteração, ou opta por finalizar o caso de uso.
4) Se o Usuário desejar continuar com a gestão de comentários, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a) O Admin requisita a inclusão de uma categoria de receitas. <br>
b) O Sistema apresenta uma janela solicitando o nome da categoria. <br>
c) O Admin fornece as informações solicitadas. <br>
d) O Sistema verifica se o nome da categoria possui algum caractere inválido, se sim ele mostra um erro ao Admin para que os campos sejam corrigidos. Senão ele realiza a inclusão da categoria na lista de categorias de receitas.

Fluxo Alternativo (2): Alteração

a) O Admin altera o nome da categoria e requisita sua atualização. <br>
b) O Sistema verifica a validade dos dados e, se eles forem válidos, altera os dados na lista de categorias de receitas, caso contrário, o erro é reportado.

Fluxo Alternativo (3): Remoção

a) O Admin seleciona uma das categorias de receitas e requisita ao Sistema que a remova. <br>
b) Se a categoria pode ser removida, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (4): Consulta

a) O Usuário opta por pesquisar uma receita por categorias. <br>
b) O Sistema apresenta uma lista de categorias com categorias de receitas e ingredientes.

Pós-condições: Uma Categoria foi inserida ou removida, seus dados foram alterados ou apresentados na tela.

---

#### Gerenciar categorias de ingredientes (CSU08)

Sumário: O Admin realiza a gestão (inclusão, remoção, alteração e consulta) de Categorias de Ingredientes.

Ator Primário: Admin.

Pré-condições: O Admin deve estar cadastrado e logado no sistema.

Fluxo Principal:

1) O Admin entra na pagina de gerenciamento de categorias de ingredientes.
2) O Sistema apresenta as operações que podem ser realizadas: adição de uma categoria, exclusão ou alteração de uma categoria já existente.
3) O Usuário seleciona a operação desejada: adição, exclusão ou alteração, ou opta por finalizar o caso de uso.
4) Se o Usuário desejar continuar com a gestão de comentários, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a) O Admin requisita a inclusão de uma categoria de ingredientes. <br>
b) O Sistema apresenta uma janela solicitando o nome da categoria. <br>
c) O Admin fornece as informações solicitadas. <br>
d) O Sistema verifica se o nome da categoria possui algum caractere inválido, se sim ele mostra um erro ao Admin para que os campos sejam corrigidos. Senão ele realiza a inclusão da categoria na lista de categorias de ingredientes.

Fluxo Alternativo (2): Alteração

a) O Admin altera o nome da categoria e requisita sua atualização. <br>
b) O Sistema verifica a validade dos dados e, se eles forem válidos, altera os dados na lista de categorias de ingredientes, caso contrário, o erro é reportado.

Fluxo Alternativo (3): Remoção

a) O Admin seleciona uma das categorias de ingredientes e requisita ao Sistema que a remova. <br>
b) Se a categoria pode ser removida, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (4): Consulta

a) O Usuário opta por pesquisar uma receita por categorias. <br>
b) O Sistema apresenta uma lista de categorias com categorias de receitas e ingredientes.

Pós-condições: Uma Categoria foi inserida ou removida, seus dados foram alterados ou apresentados na tela.

---
#### Gerenciar Preferências (CSU13)

Sumário: O usuário realiza a gestão (inclusão, alteração, exclusão e consulta) com base em suas preferências e interesses alimentares.

Ator Primário: Usuário.

Pré-condições: As preferências do usuário serão atualizadas no sistema para influenciar as sugestões de receitas.

Fluxo Principal: 

1) O usuário acessa a área de configurações de preferências dentro da aplicação.
2) O sistema exibe as preferências de sugestões e notificações configuradas previamente pelo usuário (se existirem), incluindo tipos de receita (ex: vegana, sem glúten), frequência de notificações, e horários preferenciais.
3) O usuário seleciona a opção de adicionar uma nova preferência.
4) O sistema solicita informações sobre a nova preferência, como tipos de receitas preferidas, restrições alimentares, e frequência de notificações.

Fluxo Alternativo (1): Consulta Sem Preferências Configuradas
a) Se o usuário não tiver preferências configuradas, o sistema exibe uma mensagem informando não haver preferências salvas e oferece a opção de adicionar uma nova.

Fluxo Alternativo (2): Alteração/Exclusão
a) O usuário decide cancelar uma alteração ou exclusão de preferência.
b) O sistema reverte para o estado anterior sem salvar as mudanças.

Fluxo Alternativo (3): Erro na Inclusão de Preferências
a) Caso o sistema detecte um erro na inclusão de uma nova preferência (ex: dados inválidos ou incompletos), o usuário é notificado do erro e solicitado a corrigir os dados antes de tentar novamente.

---
### Gerar relatório de vendas (CSU16)

Sumário: Este caso de uso permite ao Administrador gerar relatórios de vendas com base em períodos de tempo específicos, como diário, semanal, mensal ou personalizado.

Ator Primário: Administrador

Pré-condições: O Administrador deve estar autenticado no sistema.

Fluxo Principal:

1) O Administrador acessa a opção "Relatórios de Vendas".
2) O Administrador seleciona o período desejado para o relatório.
3) O sistema gera o relatório com as informações de vendas no período especificado.
4) O Administrador visualiza o relatório e pode optar por exportá-lo em formato PDF ou CSV.

Pós-condições: O relatório de vendas é gerado com sucesso e pode ser visualizado ou exportado para formatos como PDF ou CSV.

---

### Gerenciar categorias de produtos (CSU17)

Sumário: Este caso de uso permite ao Administrador gerenciar as categorias de produtos, realizando operações como inclusão, alteração, exclusão e consulta de categorias.

Ator Primário: Administrador

Pré-condições: O Administrador deve estar autenticado no sistema.

Fluxo Principal:

1) O Administrador acessa a opção "Gerenciar Categorias".
2) O Administrador pode:
 * Incluir uma nova categoria, fornecendo o nome e a descrição.
 * Alterar uma categoria existente.
 * Excluir uma categoria (desde que não esteja associada a produtos ativos).
 * Consultar as categorias cadastradas no sistema.
3) O sistema confirma as alterações e atualiza as categorias conforme solicitado.

Pós-condições: As categorias são gerenciadas com sucesso, e o sistema reflete as alterações imediatamente nos produtos relacionados.

---

### Gerenciar estoque de produtos (CSU18)

Sumário: Este caso de uso permite ao Administrador gerenciar o estoque de produtos, realizando operações como inclusão de novas unidades, remoção de unidades e consulta de níveis de estoque.

Ator Primário: Administrador

Pré-condições: O Administrador deve estar autenticado no sistema.

Fluxo Principal:

1) O Administrador acessa a opção "Gerenciar Estoque".
2) O Administrador pode:
 * Adicionar unidades ao estoque de um produto.
 * Remover unidades do estoque de um produto.
 * Consultar o nível de estoque atual de um produto.
3) O sistema atualiza as informações de estoque conforme as operações realizadas.

Pós-condições: O estoque é atualizado com sucesso e reflete a quantidade correta de produtos disponíveis para venda.

---

### 3.4.3 Diagrama de Classes 

A Figura 2 mostra o diagrama de classes do sistema. Uma receita deve conter pelo menos um ingrediente e pode pertencer a várias categorias. Ela também pode possuir comentários e avaliações. O usuário pode abrir solicitações para adicionar novos ingredientes e categorias ao sistema, que podem ser aprovados ou rejeitados pelo administrador. O usuário também pode conter preferências.

#### Figura 2: Diagrama de Classes do Sistema.
 
![image](https://github.com/user-attachments/assets/e3fd8170-ab5a-45b4-a239-8e3279b34505)

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
