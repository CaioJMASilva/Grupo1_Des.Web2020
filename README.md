# Grupo1_Des.Web2020
Projeto de desenvolvimento Web
- 8062877 - Caio Jorge de Menezes Abreu Silva		
- 9805928 - Leonardo Henrique Martins Florentino		
- 10748347 - Tarcídio Antônio Júnior		

## Requisitos
- O sistema deve ter 2 tipos de usuários: Clientes e Administradores 
  - Os administradores são responsáveis por registrar/gerenciar administradores, clientes e produtos. O aplicativo já vem com uma conta de administrador com senha admin.
- Clientes são usuários que acessam o sistema para comprar produtos.
- O registro do administrador inclui, pelo menos: nome, id(gerado pelo sistema), telefone, e-mail.
- O registro de cada cliente inclui, no mínimo: nome, id(gerado pelo sistema), endereço, telefone, e-mail
- Os registros de produtos incluem: nome, id(gerado pelo sistema), foto, descrição, preço, quantidade (em estoque), quantidade vendida, Link para vídeo gameplay, categoria, data de lançamento.
- Sobre a venda dos produtos: Os produtos são selecionados e incluídos em um carrinho. Os produtos são comprados usando um número de cartão de crédito (qualquer número é aceito pelo sistema). A quantidade de produto vendida é subtraída da quantidade em estoque e adicionada à quantidade vendida. Os carrinhos são esvaziados apenas mediante pagamento ou pelos clientes.
- O Administrador pode gerar os seguintes relatórios no sistema:
  - Vendas (Data_Pedido, Id_Pedido, Qtd, Valor )
  - Produtos ( Id_Produto , Nome_Produto, Valor_Unidade, Estoque,  Unidades_Vendidas , Valor_Arrecadado )



## Descrição do Projeto
Nesse projeto desenvolvemos uma loja de jogos para computador, chamada "Bee Games".<br>
Na nossa loja os jogos estão organizados por categoria, além da página inicial, que mostra os jogos lançados mais recentemente.<br>
A nossa funcionalidade extra, será a visualização de um vídeo de gameplay do jogo, que poderá ser acessado pelo usuário dentro da página de produto.<br>
Utilizamos o "Marvelapp" para desenhar os mockups do nosso site, que vocês poderão acessar através do link a seguir:<br>
[Mockups do Projeto](https://marvelapp.com/prototype/25i5e036/screen/73256281)






## Comentários sobre o código



## Plano de teste
Não utilizamos nenhuma ferramenta atomatizada para realizar testes. Nossos testes foram manuais através da execução dos arquivos html utilizando o Google Chrome.


## Resultados de teste
Durante a implementação, testavamos as páginas a cada modificação feita nos arquivos .html, .css e .js, e isso foi fundamental para conseguirmos realizar essa entrega.
Nos testes finais, o resultado foi satisfatório.


## Build Procedures
Todos os arquivos necessários para a execução/visualização do projeto estão no .ZIP. Você deve descompactar a pasta no seu computador, e executar o arquivo "index.html" através de um browser(preferencialmente o Google Chrome).
Para visualizar as telas de admin, entre na pasta "/admin" e execute qualquer um dos arquivos html através de um browser(preferencialmente o Google Chrome).

## Problemas
As maiores dificuldades que tivemos durante a implementação, foi na construção da formatação/estilo das páginas.
Tivemos que consultar bastante o GitHub e Youtube para encontrarmos referencias em CSS que poderíamos utilizar/adaptar para o nosso projeto.

## Comentários
