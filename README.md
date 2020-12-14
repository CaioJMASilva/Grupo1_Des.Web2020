# Grupo1_Des.Web2020
Projeto de desenvolvimento Web
- 8062877 - Caio Jorge de Menezes Abreu Silva		
- 10748347 - Tarcídio Antônio Júnior		

## Descrição do Projeto

Nesse projeto desenvolvemos uma loja de jogos para computador, chamada "Bee Games".<br>
Na nossa loja os jogos estão organizados por categoria, além da página inicial, que mostra os jogos lançados mais recentemente.<br>
A nossa funcionalidade extra, será a visualização de um vídeo de gameplay do jogo, que poderá ser acessado pelo usuário dentro da página de produto.<br>
Utilizamos o "Marvelapp" para desenhar os mockups do nosso site, que vocês poderão acessar através do link a seguir:<br>
[Mockups do Projeto](https://marvelapp.com/prototype/25i5e036/screen/73256281)

### Funcionalidades

Para o usuário comum:

- **Página inicial** com a lista de todos os produtos.
- **Página de categoria** com a lista dos produtos de uma categoria específica.
- **Página do produto** com informações do produto e a opção de adicionar no carrinho.
- **Página do carrinho** com os produtos adicionados e a possibilidade de alterar a quantidade. Caso o usuário esteja logado é enviado para a página de endereço de entrega, caso contrário, para a página de login.
- **Página de endereço de entrega** puxando a informação de endereço do usuário logado e permitindo alterar o endereço de entrega.
- **Página de pagamento** para o usuário informar as informações do cartão e finalizar a transação. Caso tudo esteja correto, o usuário é enviado para a página de histórico de pedidos.
- **Página de histórico** de pedido mostra todos os pedidos realizados pelo usuário logado
- **Página de perfil** mostra as informações pessoais e endereço do usuário logado, permitindo alteração e mudança de senha.
- **Página de login** para o usuário realizar o acesso.
- **Página de cadastro** para a criação de um novo usuário.

Para o usuário administrador:

- **Página de login** para o usuário realizar o acesso.
- **Gerenciamento de produtos** permitindo a listagem e edição de produtos, adição de novo e por fim pausa para não aparecer mais na loja.
- **Gerenciamento de categorias** permitindo a listagem e edição de categorias, adição de novo e por fim pausa para não aparecer mais na loja.
- **Gerenciamento de clientes** permitindo a listagem, visualização das informações e histórico de compras, além de desativar negando acesso a loja.
- **Gerenciamento de administradores** permitindo a listagem e edição de usuários, adição de novo e por fim desativar negando acesso a loja.
- **Relatórios** das últimas transações realizadas na loja, além de histórico de vendas por produto.

**Para logar como administrador, utilize as credenciais: Login: admin  -  Senha: 123**
**Todas as páginas e rotas de API estão validando a autorização do usuário para acesso.**

## Comentários sobre o código

### Dependências 
- [NodeJS](https://nodejs.org/en/)
- [Yarn](https://yarnpkg.com/) ou [NPM](https://www.npmjs.com/)
- [MongoDB](https://www.mongodb.com/)

### Tecnologias

Para o **backend**, desenvolvemos uma API REST utilizando **NodeJS** e o **framework Express**. Para armazenar os dados foi escolhido o banco de dados **MongoDB** e para conexão a **biblioteca mongoose**.

Para trabalhar a autenticação de usuários usamos a **biblioteca jsonwebtoken** e para o upload das imagens dos produtos a **biblioteca multer**.

No frontend, desenvolvemos uma aplicação usando **ReactJS** e duas bibliotecas específicas: **Styled Components** para auxiliar na estilização e **React Router** para a criação das páginas.

As informações do carrinho e se o usuário está logado são armazenados em **LocalStorage**, dessa forma, se o usuário retornar a aplicação, essas informações serão persistidas.

### Organização

Na pasta `api`está o projeto do backend, tendo a seguinte organização:

- `/configs`contém as informações de configuração do multer para upload de imagens
- `/lib` contém as funções responsáveis para verificar se o usuário tem permissão para acessar as rotas
- `/models` contém as definições de cada tabela do banco de dados
- `/routes` contém as funções para cuidar de cada rota da API
- `/uploads` contém as imagens que foram realizadas upload
- `.env`contém informações de conexão com o banco de dados
- `app.js` é o arquivo principal da API que conecta com o banco de dados e define todas as rotas

Na pasta `ui`está o projeto do frontend, tendo a seguinte organização:

- `/public`fica o arquivo final HTML da aplicação
- `/src` contém todos os arquivos principais da aplicação
- `/src/components` contém os componentes utilizados pelas páginas
- `/src/images` contém as imagens estáticas
- `/src/pages` contém as páginas da aplicação
- `/src/styles` contém os estilos reusáveis
- `/src/App.js` contém a definição das rotas
- `/src/index.js` arquivo principal do ReactJs
- `/src/store.js` contém o código responsável por armazenar informações que podem ser compartilhadas entre as páginas, como se o usuário está logado ou itens do carrinho

Na pasta `static` contém os arquivos puros HTML, CSS e JS das etapas anteriores.

Na parta `dump` contém uma cópia do banco de dados.




## Plano de Teste

Não utilizamos nenhuma ferramenta atomatizada para realizar testes. Nossos testes foram manuais utilizando o Google Chrome.

###Teste 1 
Na Home, selecionei o primeiro produto -> Na página do produto, cliquei em comprar -> Na primeira página do carrinho, fui para a página de lançamentos -> Na página de Lançamentos, selecionei o primeiro produto ->  Na página do produto, cliquei em comprar -> Na primeira página do carrinho, adicionei e depois removi 1 produto igual ao último adicionado -> Na página de carrinho, cliquei em continuar -> Na página Login, cliquei em criar sua conta -> Após criar a conta, voltei para o carrinho ->  Na página de carrinho, cliquei em continuar -> Na página de endereço, cliquei em continuar -> Na página de pagamento, adicionei informações de pagamento e cliquei em finalizar compra.

###Teste 2
Na Home, selecionei o ícone de login -> Na página de login, inseri as credencias que criei no teste anterior -> Na página do usuário, verifiquei o histórico de compras.

###Teste 3
Na página de admin, coloquei as credenciais -> Cliquei na botão Relatórios, e verifiquei o relatório de Vendas -> Cliquei no botão Usuários, e verifiquei as informações dos clientes.

## Resultados de teste

Durante a implementação, testavamos as páginas a cada modificação feita nos arquivos .html, .css e .js, e isso foi fundamental para conseguirmos realizar essa entrega.
Nos testes finais, o resultado foi satisfatório.


## Procedimentos de compilação

- **Passo 0:** Instalar todas as dependências

- **Passo 1:** Clonar o repositório git

`git clone https://github.com/CaioJMASilva/Grupo1_Des.Web2020.git`

- **Passo 2:** Importar o dump do banco de dados

`mongorestore --host <host:port> --username <username> --password <password> -d store --drop dump/store`

- **Passo 3:** Na pasta /api/.env alterar a variável `DB_CONNECTION` com suas credenciais de conexão ao banco de dados 

- **Passo 4:** Na pasta /api instalar os pacotes NodeJS

`cd api/`

`yarn install` ou `npm install`

- **Passo 5:** Na pasta /api rodar o backend

`yarn start` ou `npm start`

- **Passo 6:** Na pasta /ui instalar os pacotes NodeJS

`cd ui/`

`yarn install` ou `npm install`

- **Passo 7:** Na pasta /ui rodar o backend

`yarn start` ou `npm start`

- **Passo 8:** Na url `http://localhost:3000` estará o ecommerce rodando

- **Passo 9:** Na url `http://localhost:3000/admin` estará a página de administrador. (Login: admin  -  Senha: 123)


## Problemas

As maiores dificuldades que tivemos durante a implementação, foi na construção da formatação/estilo das páginas, e conexão com a API.
Tivemos que consultar bastante o GitHub e Youtube para encontrarmos outras referencias que poderíamos utilizar/adaptar para o nosso projeto.

Até a última entrega, tínhamos a ideia de colocar a funcionalidade de cálculo de Frete no nosso site, mas após algumas pesquisas percebemos que a integração com o site dos correios é paga, e por isso desistimos da ideia. Como alternativa, deixamos o campo de cálculo de frete, porém o resultado sempre será "Frete Grátis".

## Comentários Gerais

Durante o projeto, um dos integrantes do grupo trancou a disciplina, e isso acabou sobrecarregando o restante da equipe.
