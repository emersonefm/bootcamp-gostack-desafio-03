<h1 align="center">
  <img alt="Fastfeet" title="Fastfeet" src=".github/logo.png" width="300px" />
</h1>

<h3 align="center">
  Desafio 2: FastFeet, o início (backend)
</h3>

<h3 align="center">
  :warning: Etapa 2/4 do Desafio Final :warning:
</h3>

<p>Esse desafio faz parte do Desafio Final, que é uma aplicação completa (Back-end, Front-end e Mobile) que é avaliada para emissão do Certificado do Bootcamp GoStack, por isso é fundamental que ele seja feito com muito empenho!</p>

<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/emersonefm/bootcamp-goStack-desafio-03.svg">

  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/emersonefm/bootcamp-goStack-desafio-03.svg">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/emersonefm/bootcamp-goStack-desafio-03.svg">
  <a href="https://github.com/emersonefm/bootcamp-gostack-desafio-03/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/emersonefm/bootcamp-goStack-desafio-03.svg">
  </a>

  <a href="https://github.com/emersonefm/bootcamp-gostack-desafio-03/issues">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/emersonefm/bootcamp-goStack-desafio-03.svg">
  </a>

  <a href="https://github.com/emersonefm/bootcamp-goStack-desafio-03/blob/master/LICENSE">
    <img alt="GitHub" src="https://img.shields.io/github/license/emersonefm/bootcamp-goStack-desafio-03.svg">
  </a>

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-%2304D361">
  </a>

</p>

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#computer-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#information_source-como-usar">Como usar</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#mag_right-funcionalidades">Funcionalidades</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

## :rocket: Sobre o desafio

A aplicação que iremos dar início ao desenvolvimento a partir de agora é um app para uma transportadora fictícia, o FastFeet.

Nesse primeiro desafio vamos criar algumas funcionalidades básicas que aprendemos ao longo das aulas até aqui. Esse projeto será desenvolvido aos poucos até o fim da sua jornada onde você terá uma aplicação completa envolvendo back-end, front-end e mobile, que será utilizada para a **certificação do bootcamp**, então, bora pro código!



## :computer: Tecnologias

Este projeto foi desenvolvido com as seguintes tecnologias:

-  [Yup](https://github.com/jquense/yup)
-  [redis](https://redis.io/)
-  [Multer](https://github.com/expressjs/multer)
-  [Node.js](https://nodejs.org/)
-  [Express](https://expressjs.com/)
-  [Sucrase](https://github.com/alangpierce/sucrase)
-  [bcryptjs](https://github.com/dcodeIO/bcrypt.js)
-  [date-fns](https://date-fns.org/)
-  [Nodemon](https://nodemon.io/)
-  [Sequelize](https://sequelize.org/)
-  [bee-queue](https://github.com/bee-queue/bee-queue)
-  [Nodemailer](https://nodemailer.com/about/)
-  [Handlebars](https://handlebarsjs.com/)
-  [JsonWebToken](https://jwt.io/)
-  [VS Code][vc] com [EditorConfig][vceditconfig],  [ESLint][vceslint] e [Prettier][vcprettier]

## :information_source: Como usar

Para clonar e usar esta aplicação, você precisará do [Git](https://git-scm.com), [Node.js v12.15.0][nodejs] ou superior + [Yarn v1.21.1][yarn] ou superior instalados no seu computador. No seu terminal:

```bash
# Clonar este repositório
$ git clone https://github.com/emersonefm/bootcamp-gostack-desafio-03.git desafio-03

# Aceder a este repositório
$ cd desafio-03

# Instalar dependências
$ yarn install

# Rodar a aplicação
$ yarn dev

# Rodar a fila de emails
$ yarn queue
```

Além disso, você precisará configurar o servidor postgres e redis.

## :mag_right: Funcionalidades

Abaixo estão descritas as funcionalidades que adicionei a minha aplicação.

### **1. Autenticação dos Administradores**

Criei a permissão para que um usuário se autentique na aplicação utilizando e-mail e uma senha.

- A autenticação foi feita utilizando JWT.
- Realizei a validação dos dados de entrada.
- Administrador tem acesso a todas as rotas da aplicação.
- Pode gerenciar todos os entregadores, destinatários e entregas.

### **2. Gestão de destinatários**

Criei a permissão para que os destinatários sejam mantidos (cadastrados/atualizados) na aplicação.

- O gerenciamento de destinatários só pode ser feito por administradores autenticados na aplicação.
- Realizei a validação dos dados de entrada
- O destinatário não pode se autenticar no sistema, ou seja, não possui senha.

### **3. Gestão de entregadores**

Criei um CRUD para que os entregadores sejam mantidos na aplicação.

- O gerencimaneto de entregadores só pode ser feito por administradores autenticados na aplicação.
- Realizei a validação dos dados de entrada
- O entregador não pode se autenticar no sistema, ou seja, não possui senha.
- O entregador pode visualizar as entregas vinculadas a ele.
- O entregador pode iniciar uma entrega desde que esteja dentro do horário ( 08: as 18:00 ), e desde que não tenha atingido a cota de  5 ou entregas iniciadas no dia.
- O entregador pode finalizar uma entrega, desde que envie uma foto de sua assinatura.
- O entregador pode cadastrar um problema nas suas entregas.

### **4. Gestão de encomendas**

Criei um CRUD para que as encomendas sejam mantidas na aplicação.

- O gerencimaneto de encomendas só pode ser feito por administradores autenticados na aplicação.
- Realizei a validação dos dados de entrada.
- A retirada de encomendas só pode ser feita entre 08:00 e 18:00 horas

## :memo: Licença
Este projeto está sob a licença do MIT . Veja a [LICENÇA](https://github.com/emersonefm/bootcamp-goStack-desafio-03/blob/master/LICENSE) para mais informações.

---


[nodejs]: https://nodejs.org/
[yarn]: https://yarnpkg.com/
[vc]: https://code.visualstudio.com/
[vceditconfig]: https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig
[vceslint]: https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint
[vcprettier]: https://prettier.io/

