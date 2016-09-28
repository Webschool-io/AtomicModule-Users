# AtomicModule-Users
Módulo atômico de gerenciamento de usuários em Node.js


## Conceito  

Esse módulo irá gerenciar os usuários desde sua criação, como na confirmação de conta e gerenciamento de autorização e autenticação.


## Funcionalidades  

* Gerenciamento de usuários;  
* Confirmação de conta;  
* Recuperação de senha;  
* Gerenciamento de autorização e autenticação.


## Interface

Aqui definimos a nomenclatura utilizada para cada funcionalidade, seus parâmetros e seu retorno:


### Escolher tipo de login

Nessa funcionalidade você irá decidir qual será o meio de login para o ecommerce. Se vai realizar o login através de uma conta cadastrando um e-mail válido ou se vai realizar o login através de suas redes sociais.


### Login através de conta cadastrando um e-mail válido

Aqui você irá realizar login no ecommerce através de um cadastro com um e-mail válido e alguns dados básicos.


#### Dados básicos do usuário necessários para cadastro

* Nome;  
* E-mail válido;  
* Senha.


* A restrição será cadastrar uma conta por e-mail.


#### Criar conta através de e-mail válido

> verificar e completar..


#### Login através de suas redes sociais

Aqui você irá realizar login no ecommerce através de um perfil em uma rede social, seja via Facebook, Google ou Twitter.


* Escolher qual rede social para realizar o login (Facebook / Google / Twitter).


* Ecommerce envia solicitação (OAuth) para rede social para ler dados do usuário;  
* Usuário condece permissão ao ecommerce ler seus dados na rede social escolhida;  
* Devolve permissão ao ecommerce que vai tratar se é válida e liberar acesso ao ecommerce ou não.


## Tipos

Aqui nós vamos definir os tipos de objeto usados nesse módulo.


### Conta local

`users.model`  

```js
{
  _id
  , name
  , email
  , password // melhorar esse campo, salt e os baguios lá
  , created_at
  , updated_at
}
```

> ver um esquema geral para os logs de edição da conta do usuário. Isso pode ser importante para gerar relatórios (future)


### Conta via rede social

* Pegar AppID de cada rede social (`env`) que o Suissa nos enviou;  
*


> ver se é necessário salvar algo no banco, o que salvar e como
