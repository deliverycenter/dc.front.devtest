# Processo Seletivo Front end - Delivery Center

O objetivo deste teste é avaliar a organização do seu código, sua criatividade e lógica, e ver como você estrutura uma solução de forma simples e eficiente baseada em requisitos simples.

---

## O desafio
O desafio consiste na refatoração de um projeto MVP fictício que lista usuários e álbuns de fotos.  
![image](https://user-images.githubusercontent.com/7800446/126558146-de2e5532-5d75-4184-87a3-bd38d9750c57.png)

Mais abaixo listamos os requisitos e algumas tarefas necessárias para dar andamento no desenvolvimento do projeto.  


O desenvolvimento foi iniciado com base no Create React App, portanto tem vários arquivos que talvez não serão utilizados.  
Para rodar o projeto é bem simples:
```
npm install
npm start
```

### <a id="requisitos"></a> Requisitos

#### Tela de lista de usuários
- Caminho da rota: `usuarios/`
- Deve exibir a tabela de usuarios
- A tabela deve ser estilizada com um componente do Material UI (sugestão: Table)
- Cada item da tabela deve conter:
  - dados do usuário
    - nome
    - email
    - telefone
    - website
  - link para o detalhe
  - quantidade de álbuns

#### Tela de detalhe do usuário
- Caminho da rota: `usuarios/:userId`
- Deve exibir todos os detalhes do usuário, conforme os contextos:
  - dados pessoais e de acesso
  - endereço
  - empresa
  - álbuns: link para lista de álbuns do user

#### Tela de álbuns do usuário
- Caminho da rota: `usuarios/:userId/albuns/`
- Deve listar todos os álbuns do usuário
- A lista de álbuns deve ser estilizada com um componente do Material UI (sugestão: [ImageList -Image list with titlebars](https://material-ui.com/components/image-list/#image-list-with-titlebars))
- Cada álbum da lista deve ter:
  - uma capa (primeira photo do álbum);
  - o nome do álbum
  - link para lista de photos do álbum

#### Tela de detalhe do álbum
- Caminho da rota: `usuarios/:userId/albuns/:albumId`
- Deve exibir o nome do álbum
- A lista de fotos deve ser estilizada com um componente do Material UI (sugestão: [ImageList -Basic Image list](https://material-ui.com/components/image-list/#basic-image-list))
- Deve listar as fotos do álbum
  - A lista deve exibir apenas 12 resultados por vez
  - A lista deve possuir uma paginação

## Tarefas

**Importante:**
- Cada tarefa deve ser feita de forma isolada, em sua própria branch ou commit;
- As tarefas devem ser feitas na ordem em que estão listadas abaixo, porém;
- Caso não saiba como resolver ou tenha dificuldades, pode pular para a próxima tarefa, e;
- Caso não consiga terminar todas as tarefas à tempo, não se preocupe;

#
**Sinta-se à vontade para alterar, organizar e limpar o código como achar necessário, assim como criar casos de teste, documentar o projeto e utilizar 
ferramentas que melhoram a qualidade e confiabilidade do código. A avaliação ocorrerá em acordo com o esforço colocado no projeto.**
#

### 1. fix: corrigir funcionamento do app
- Lista de álbuns deve ser filtrada por usuário;
- Filtro de usuários deve filtrar a tabela por nome e e-mail;
- Filtro de usuários deve ser case insensitive;
- Temos alguns warnings no console que precisam ser corrigidos;

### 2. refactor: melhorar a estrutura do código
Atualmente temos alguns problemas que precisam ser resolvidos:
- O código está escrito com classes e é necessário reescrevê-lo de forma funcional, utilizando hooks.
- O código está todo em um único arquivo, o que pode dificultar manutenção e leitura.
- Temos muitos estilos inline, o que causa repetição de código e também dificulta a manutenção.
- Há várias inconsistências de semântica nas marcações HTML.

### 3. refactor: Melhorar estrutura de comunicação com API
- Temos algumas promises espalhadas pelo componente, o que dificulta rastrear e reaproveitar as requisições para APIs;

### 4. feature: Mover telas do projeto para suas respectivas rotas
É necessário que algumas telas estejam em rotas específicas:
- Cada tela deve estar em sua respectiva rota, [conforme descrito anteriormente nos requisitos](#requisitos);
- Cada rota deve funcionar corretamente, tanto por navegação em tela quanto acessando diretamente a URL;

### 5. refactor: redesign da aplicação
Não temos um layout para o projeto e decidimos utilizar a biblioteca do Material UI no nosso app.  

Nos [requisitos do projeto](#requisitos) há algumas sugestões de componentes, mas fique à vontade para utilizar outras opções ou desenvolver por conta própria, se achar necessário.  

De modo geral, você só precisa seguir os padrões de estilo e projeto da biblioteca, inclusive nos demais componentes não listados nas sugestões (ex: botões, listas, paginação, campos de formulário).  

### 6. refactor: Gerenciamento de estado por contexto
Otimizar o gerenciamento de estado da aplicação, global ou por contextos (Context API, Redux, Mobx, etc).

---

## Avaliação

### O que avaliaremos
- Código: semântica, organização, legibilidade, manutenibilidade, escalabilidade, reaproveitamento;
- Projeto: estrutura, documentação, histórico e mensagens de commit;
- Aplicação: experiência, usabilidade, performance;

### O que deve ser feito
- Código HTML semântico e com boa legibilidade;
- O projeto deve ser feito em React, com estrutura funcional e utiliando a arquitetura de Hooks;
- Integração com uma biblioteca de UI (ex: Material UI);
- O projeto deve ter um README explicando como rodar a aplicação;
- Utilização dos proptypes nos componentes;

### O que consideramos importante que seja feito
- Layout responsivo;
- Otimização de estados da aplicação;
- Validação do código (ESlint, Prettier, Stylelint, editorConfig, sonar, etc);
- Verificação de tipos (PropTypes, jsdoc, TypeScript, etc);
- Utlização de conceitos modernos de JavaScript;
- Testes unitários (Jest) e integração (Testing Library)

### O que gostaríamos de ver no seu teste (diferenciais)
- Otimização de performance do código e da aplicação;
- Estilo consistente;
- Preocupação com acessibilidade (leitores de tela, navegação por teclado);
- Um README de saltar os olhos;
- Cache na aplicação ou acesso offline;
- Código rodando live;
- Testes end to end (Cypress, Selenium);
- Typescript;

#

## Após a finalização do teste, ele deve ser entregue seguindo estes passos:
1. Crie um novo repositório
2. No repositório novo, clique importar código:  
![image](https://user-images.githubusercontent.com/22237876/118177366-fa7a7700-b408-11eb-8ac3-4fe92758db03.png)

3. Adicione o seguinte repo: https://github.com/deliverycenter/dc.front.devtest  
![image](https://user-images.githubusercontent.com/22237876/118177376-fd756780-b408-11eb-8cb1-530516902db9.png)

4. Mude a visibilidade do projeto para privado  
![image](https://user-images.githubusercontent.com/22237876/118177453-167e1880-b409-11eb-9ebc-bfe6d0a76b78.png)
![image](https://user-images.githubusercontent.com/22237876/118177483-20a01700-b409-11eb-9c48-b759a9346f2e.png)
![image](https://user-images.githubusercontent.com/22237876/118177497-2564cb00-b409-11eb-9760-b671f9d8eced.png)

5. Por fim, convide o usuário **deliverycenter-devs** como colaborador  
![image](https://user-images.githubusercontent.com/22237876/118177547-39103180-b409-11eb-8884-50f4526f6ed7.png)

6. Abra um PullRequest em seu repositório com o código alterado, para que possamos avaliar as alterações realizadas por você em relação à base do teste
