# Apostila de Desenvolvimento Web com Laravel para disciplina de Desenvolvimento Web do 6º semestre do curso de Informática

##### Descrição:

Esta apostila servirá como guia para entender os conceitos básicos de desenvolvimento web com Laravel. O objetivo é que o aluno entenda os conceitos básicos de desenvolvimento web e que consiga desenvolver um sistema web simples utilizando o framework Laravel.

Um vez que as aulas são corridas, com pouco e existe muitos imprevistos. A apostila servirá como um guia para o aluno que não conseguiu acompanhar as aulas ou que deseja revisar os conceitos. Além disso, alguns conceitos vistos aqui servirão para prova da primeira unidade.

#### Sumário

# Table of contents

- [Introdução](#introduo)
  - [O que é um framework?](#o-que--um-framework)
  - [O que é o Laravel?](#o-que--o-laravel)
    - [Vantagens de usar o Laravel](#vantagens-de-usar-o-laravel)
    - [Desvantagens de usar o Laravel](#desvantagens-de-usar-o-laravel)
  - [O que é o MVC?](#o-que--o-mvc)
  - [O que é o Composer?](#o-que--o-composer)
- [Instalação](#instalao)
  - [Instalação do Composer](#instalao-do-composer)
  - [Instalação do Laravel](#instalao-do-laravel)
  - [Instalação do XAMPP](#instalao-do-xampp)
  - [Criando um projeto Laravel](#criando-um-projeto-laravel)
  - [Estrutura de um projeto Laravel](#estrutura-de-um-projeto-laravel)
- [Rotas](#rotas)
  - [Rotas nomeadas](#rotas-nomeadas)
  - [Rotas anônimas](#rotas-annimas)
  - [Métodos HTTP](#mtodos-http)
    - [Requisição GET](#requisio-get)
    - [Requisição POST](#requisio-post)
- [Views](#views)
  - [Criando uma view](#criando-uma-view)
  - [Passando dados para a view](#passando-dados-para-a-view)
  - [Exibindo dados na view](#exibindo-dados-na-view)
  - [Diretivas](#diretivas)
    - [Diretiva @if](#diretiva-if)
    - [Diretiva @else](#diretiva-else)
    - [Diretiva @elseif](#diretiva-elseif)
    - [Diretiva @for](#diretiva-for)
    - [Diretiva @foreach](#diretiva-foreach)
    - [Diretiva @forelse](#diretiva-forelse)
    - [Diretiva @empty](#diretiva-empty)
    - [Diretiva @isset](#diretiva-isset)
    - [Diretiva @switch](#diretiva-switch)
    - [Diretiva @include](#diretiva-include)
    - [Diretiva @Yield](#diretiva-yield)
    - [Diretiva @extends](#diretiva-extends)
    - [Diretiva @section](#diretiva-section)
    - [Diretiva @auth](#diretiva-auth)
    - [Diretiva @guest](#diretiva-guest)
  - [Funções de ajuda](#funes-de-ajuda)
    - [route( )](#route-)
    - [asset( )](#asset-)
    - [auth( )](#auth-)
    - [old( )](#old-)
    - [request( )](#request-)
    - [session( )](#session-)
- [Controllers (controladores)](#controllers-controladores)
  - [Criando um controller](#criando-um-controller)
  - [Métodos de um controller](#mtodos-de-um-controller)
- [Migrações (migrations)](#migraes-migrations)
  - [Criando uma migração](#criando-uma-migrao)
  - [Métodos de uma migração](#mtodos-de-uma-migrao)
  - [Adicionando colunas a uma tabela](#adicionando-colunas-a-uma-tabela)
    - [Tipos de colunas e como criar](#tipos-de-colunas-e-como-criar)
      - [ID](#id)
      - [String](#string)
      - [Integer](#integer)
      - [Text](#text)
      - [Boolean](#boolean)
      - [Timestamps](#timestamps)
      - [Datetime](#datetime)
      - [Decimal](#decimal)
      - [min, max e nullable](#min-max-e-nullable)
      - [unique](#unique)
      - [default](#default)
      - [foreignId](#foreignid)
      - [constrained](#constrained)
      - [onDelete](#ondelete)
      - [onUpdate](#onupdate)
  - [Executando uma migração](#executando-uma-migrao)
- [Modelos (models)](#modelos-models)
  - [Criando um modelo](#criando-um-modelo)
  - [Métodos de um modelo](#mtodos-de-um-modelo)
  - [Relacionamentos](#relacionamentos)


## Introdução
### O que é um framework?

Um framework é um conjunto de classes e funções que auxiliam o desenvolvedor a criar uma aplicação. O framework fornece uma estrutura para o desenvolvimento de uma aplicação. O desenvolvedor não precisa se preocupar com a estrutura da aplicação, pois o framework já fornece uma estrutura. O desenvolvedor precisa apenas se preocupar com a lógica da aplicação.

Por exemplo, códigos que são comumente utilizados em uma aplicação web, como a conexão com o banco de dados, a criação de uma sessão, a criação de um sistema de login, etc. Esses códigos são comumente utilizados em uma aplicação web. O framework fornece esses códigos para o desenvolvedor. O desenvolvedor não precisa se preocupar com a criação desses códigos, pois o framework já fornece esses códigos.

### O que é o Laravel?

O laravel é um framework PHP para desenvolvimento web. Ele é um framework que utiliza o padrão MVC (Model-View-Controller) e que utiliza o Composer para gerenciar as dependências.Ele reutiliza os componentes existentes de diferentes frameworks o que auxilia na criação de uma aplicação web. A aplicação web assim desenhada é mais estruturada e pragmática.

Componentes são partes de um sistema que podem ser reutilizadas em outros sistemas. Por exemplo, um sistema de login pode ser reutilizado em outros sistemas.

#### Vantagens de usar o Laravel
O Laravel oferece as seguintes vantagens:
- Facilidade de uso
- Facilidade de manutenção
- Facilidade de atualização
- seguro
- Redução de tempo de desenvolvimento visto que o desenvolvedor não precisa se preocupar com a estrutura da aplicação e criação de códigos comumente utilizados em uma aplicação web.

#### Desvantagens de usar o Laravel

- É necessário conhecer o básico PHP para entender e utilizar o Laravel


### O que é o MVC?

O padrão Model-View-Controller (MVC) é um padrão de arquitetura de software que separa a aplicação em três camadas: Model, View e Controller. O objetivo é separar a lógica da aplicação da interface do usuário.
- **Model**: é a camada que contém a lógica da aplicação. É a camada que contém as regras de negócio da aplicação. Regras de negócio são regras que definem como a aplicação deve funcionar. 
`Por exemplo, uma regra de negócio de um sistema de login é que o usuário deve informar o login e a senha para acessar o sistema, por sua vez, o model acessa o banco de dados para recuperar os dados e realizar as operações necessárias para verificar se o usuário pode acessar o sistema`.
- **View**: é a camada que contém a interface do usuário. É a camada que o usuário interage com a aplicação e é nela onde colocamos os HTML, CSS e javascript que juntos compõem a interface do usuário.
- **Controller**: é a camada que recebe as requisições do usuário e que envia as respostas para o usuário. É a camada que recebe as requisições do usuário e que envia as respostas para o usuário. Por exemplo, quando o usuário acessa a página de login, o controller recebe a requisição e envia a resposta para o usuário. O controller também é responsável por receber os dados do usuário e enviar para o model realizar as operações necessárias. Veja as figuras abaixo:

[![MVC](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/MVC-Process.svg/1200px-MVC-Process.svg.png)](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/MVC-Process.svg/1200px-MVC-Process.svg.png)


### O que é o Composer?
Composer é uma ferramenta para gerenciar as dependências de um projeto PHP. Lembra que falamos que o Laravel reutiliza os componentes existentes de diferentes sistemas? O Composer é a ferramenta que gerencia esses componentes. O Composer é responsável por baixar os componentes necessários para o projeto. Por exemplo, o Laravel utiliza o componente de autenticação do framework Symfony. O Composer é responsável por baixar esse componente e disponibilizar para o Laravel.
`Entenda dependência como um componente que é necessário para o funcionamento de um sistema. Por exemplo, um sistema de login é um componente que é necessário para o funcionamento de um sistema web.`
Todas as dependências do projeto são armazenadas no arquivo `composer.json`. O Composer lê esse arquivo e baixa as dependências necessárias para o projeto.

## Instalação
Para instalar o Laravel é necessário instalar o Composer e o XAMPP (não obrigatoriamente ele, poderia ser outro, mas a principio vamos trabalhar com ele para uso do banco).
### Instalação do Composer
 Como foi dito anteriormente, o Composer é responsável por gerenciar as dependências do projeto mas para isso é necessário instalar o Composer. Para instalar o Composer, acesse o site https://getcomposer.org/download/ e baixe o instalador do Composer. Após baixar o instalador, execute-o e siga as instruções de instalação. Após a instalação, abra o terminal (cmd) e digite o comando `composer`. Se aparecer a mensagem de ajuda do Composer, a instalação foi realizada com sucesso.
### Instalação do Laravel
Para instalar o Laravel, abra o terminal (cmd) e digite o comando `composer global require laravel/installer`. Após a instalação, digite o comando `laravel` para verificar se a instalação foi realizada com sucesso. Se aparecer a mensagem de ajuda do Laravel, a instalação foi realizada com sucesso.

### Instalação do XAMPP
O XAMPP é um pacote que contém o Apache, o PHP e o MySQL. O Apache é um servidor web, o PHP é uma linguagem de programação e o MySQL é um sistema gerenciador de banco de dados. O XAMPP é um pacote que contém esses três componentes. Para instalar o XAMPP, acesse o site https://www.apachefriends.org/pt_br/index.html e baixe o instalador do XAMPP. Após baixar o instalador, execute-o e siga as instruções de instalação. Após a instalação, abra o XAMPP e inicie o Apache e o MySQL. Após iniciar o Apache e o MySQL, abra o navegador e digite o endereço `http://localhost`. Se aparecer a página inicial do XAMPP, a instalação foi realizada com sucesso.

### Criando um projeto Laravel
Depois de certificar que o Composer e o Laravel foram instalados com sucesso, crie uma pasta de sua preferência para guardar seus projetos laravel. Isto não é obrigatório, mas é uma boa prática.

Existem duas formas de criar um projeto laravel. A primeira forma é utilizando o comando `composer create-project laravel/laravel^:x.* nome_projeto`. O comando `composer create-project laravel/laravel:^x.* nome_projeto` cria uma pasta com o nome do projeto e instala o Laravel dentro dessa pasta. A segunda forma é utilizando o comando `laravel new nome_projeto`.

`obs: x é a versão do laravel e o * diz vai ser a última versão daquele número. Além disso 'nome_projeto' é o nome do projeto que você vai criar.'`

Na pasta criada anteriormente, abra o terminal (CMD). Digite o comando `laravel new nome_projeto` para criar um projeto laravel. O comando `laravel new nome_projeto` cria uma pasta com o nome do projeto e instala o Laravel dentro dessa pasta. A seguir irá mostrar algo como a imagem abaixo:

![Laravel](https://www.tutorialspoint.com/laravel/images/composer_create_project%20.jpg)

por fim, para rodar o projeto, digite o comando `php artisan serve` ainda no terminal (dentro da pasta do projeto que foi criada) e acesse o endereço `http://localhost:8000` no navegador. Se aparecer a página inicial do Laravel, o projeto foi criado com sucesso.

Simulação:
```bash
	composer create-project laravel/laravel:^7.* meu_projeto
```
Então será criado uma pasta chamada `meu_projeto` com o Laravel instalado dentro dela, bastando apenas acessar a pasta e rodar o comando `php artisan serve` para rodar o projeto.

a tela que deve aparecer ao acessar o endereço `http://localhost:8000` é a seguinte:

![Laravel](https://i.postimg.cc/15gJMpYc/laravel8.png)

**obs:** O comando `php artisan alguma-coisa` será muito utilizado, então é bom já ir se acostumando com ele pois ele é o responsável por rodar o projeto, criar controllers, models, migrations, etc.

### Estrutura de um projeto Laravel
A estrutura de um projeto Laravel é a estrutura de pastas, subpastas e arquivos incluídos em um projeto. Assim que criamos um projeto no Laravel, temos uma visão geral da estrutura da aplicação conforme mostrado na imagem aqui.

![Laravel](https://res.cloudinary.com/practicaldev/image/fetch/s--Y9VMd0xK--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/tagpdhwz8izcf2yta6x6.png)

| Diretório/arquivo      | Descrição                                                                                                                                                                                                                                                                       |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| app/.                  | Diretório que armazena os principais arquivos do seu código, como por exemplo, os controllers e os models.                                                                                                                                                                      |
| app/Http/Controllers/. | Armazena os controllers do seu site. Em uma aplicação MVC, o controller é responsável pelo carregamento das views e pelo acesso aos dados por meio da ligação com os models. Por convenção, arquivos de controller devem iniciar com letra maiúscula.                           |
| app/Models/.           | Diretório que armazena os models do seu site. Em uma aplicação MVC, o model é responsável pelo acesso aos dados. Por convenção, arquivos do model devem iniciar com letra maiúscula.                                                                                            |
| bootstrap/.            | Armazena os arquivos necessários para a inicialização do Laravel. Não alteramos os arquivos dessa pasta.                                                                                                                                                                        |
| config/.               | Armazena os arquivos de configuração do framework. Podemos alterar os arquivos dessa pasta.                                                                                                                                                                                     |
| config/app.php         | Esse é o principal arquivo de configuração do PHP. Por exemplo, na linha 57 podemos alterar a URL padrão. Note que a melhor alternativa é realizar essas configurações                                                                                                          |
| config/database.php    | Arquivo usado para configurar a conexão com um banco de dados.                                                                                                                                                                                                                  |
| database/.             | Armazena definições referentes às bases de dados. Caso você esteja utilizando o sistema de gerenciamento de banco de dados SQLite, os arquivos da sua base de dados ficarão armazenados nesse diretório.                                                                        |
| lang/.                 | Diretório que armazena códigos que personalizam mensagens de acordo com o idioma escolhido.                                                                                                                                                                                     |
| public/.               | Essa é a pasta raiz do Laravel. Note que se quisermos adicionar arquivos de estilo, imagens, favicon ou scripts, podemos alocá-los dentro desta pasta.                                                                                                                          |
| public/index.php       | Arquivo de índice. Principal arquivo carregado pelo servidor web. Não alteramos esse arquivo, pois, no padrão MVC, estilos e estruturas são configurados nas views.                                                                                                             |
| resources/views/.      | Neste diretório ficam armazenadas as views. No padrão MVC, as views ou visões são responsáveis por carregar as interfaces exibidas ao usuário. Por convenção, todo o arquivo correspondente a uma view deve começar com letra minúscula e terminar com a extensão “.blade.php”. |
| routes/web.php         | Esse arquivo armazena as rotas permitidas na aplicação. As rotas delimitam qual controller irá responder para determinada URL acessada no navegador.                                                                                                                            |
| storage/.              | Armazena arquivos criados durante o processamento da aplicação, além de logs de erros do Artisan.                                                                                                                                                                               |
| tests/.                | Diretório onde podemos armazenar nossos testes automatizados.                                                                                                                                                                                                                   |
| vendor/.               | Este diretório é gerenciado pelo Composer. Nesse diretório ficam armazenados os arquivos de autoload, códigos de implementações de padrões de projeto, além de códigos referentes a pacotes de terceiros. Não devemos fazer alterações nos arquivos desse diretório.            |
| artisan                | Arquivo responsável por carregar o Artisan: a interface de linha de comando do Laravel.                                                                                                                                                                                         |
| composer.json          | É utilizado pelo Composer para gerenciar as dependências de pacotes do PHP. Por esse arquivo podemos adicionar na nossa aplicação códigos desenvolvidos por terceiros.                                                                                                          |
| package.json           | Tem uma funcionalidade parecida com o composer.json, entretanto, o package.json é utilizado para gerenciar as dependências de arquivos JavaScript.                                                                                                                              |
| .env                   | Arquivo usado para armazenar dados sensíveis, como senhas de banco de dados e a URL principal usada pelo comando url(‘/’);                                                                                                                                                      |


## Rotas

Rotas são a forma como o Laravel recebe as requisições e responde para o usuário. Quando o usuário acessa uma URL, o Laravel identifica a rota e envia a resposta. Por exemplo, quando o usuário acessa a URL http://localhost:8000, o Laravel identifica a rota / e envia a resposta. Quando o usuário acessa a URL http://localhost:8000/home, o Laravel identifica a rota /home e envia a resposta. Quando o usuário acessa a URL http://localhost:8000/login, o Laravel identifica a rota /login e envia a resposta.

Elas são responsáveis fazer a ligação entre uma URL e um controller (veremos mais abaixo sobre controladores). Quando o usuário acessa uma URL, a rota é responsável por chamar um método de um controller. Por exemplo, quando o usuário acessa a página principal do sistema, a rota é responsável por chamar o método de um controller que irá carregar a página principal do sistema. Quando o usuário acessa a página de login, a rota é responsável por chamar o método de um controller que irá carregar a página de login.

O Laravel possui um arquivo de rotas que é responsável por mapear as requisições para o código que deve ser executado. O arquivo de rotas está localizado em `routes/web.php`. O Laravel possui dois tipos de rotas: rotas nomeadas e rotas anônimas.

### Rotas nomeadas
Rotas nomeadas são rotas que possuem um nome. Por exemplo, a rota `/` é nomeada como `home`. Para criar uma rota nomeada, utilize o método `name` do objeto `Route`. O código abaixo cria uma rota nomeada `home` que retorna a view `welcome`.

```php
Route::get('/', function () {
    return view('welcome');
})->name('home');
```
### Rotas anônimas
Rotas anônimas são rotas que não possuem um nome. Para criar uma rota anônima, não utilize o método name do objeto Route. O código abaixo cria uma rota anônima / que retorna a view welcome.

```php
Route::get('/', function () {
    return view('welcome');
});
```

### Métodos HTTP
Os métodos HTTP são utilizados para indicar o tipo de ação que será realizada. Por exemplo, quando o usuário acessa uma página, o navegador envia uma requisição do tipo GET para o servidor. Quando o usuário envia um formulário, o navegador envia uma requisição do tipo POST para o servidor. O Laravel suporta os seguintes métodos HTTP:
- **GET**:	É o método utilizado para acessar uma página. Quando o usuário acessa uma página, o navegador envia uma requisição do tipo GET para o servidor.
- **POST**:	É o método utilizado para enviar dados para o servidor. Quando o usuário envia um formulário, o navegador envia uma requisição do tipo POST para o servidor.
- **PUT**:	É o método utilizado para atualizar dados no servidor.
- **PATCH**:	É o método utilizado para atualizar
- **DELETE**:	É o método utilizado para deletar dados no servidor.


A O método get() indica que a rota aceita apenas requisições do tipo GET. O método get() recebe dois parâmetros: o primeiro parâmetro é a URL e o segundo parâmetro é uma função anônima que retorna uma view. A função anônima é uma função sem nome. Nesse caso, a função anônima retorna a view welcome.blade.php.


obs: o comando 'php artisan serve' já inicia o projeto no endereço 'http://localhost:8000'




<p data-line="217" class="sync-line" style="margin:0;"></p>

A rota acima recebe uma requisição do tipo GET, ou seja, uma requisição que acessa uma página. Quando a rota recebe uma requisição, ela executa a função anônima e retorna a string Olá, mundo!. A rota acima é responsável por receber uma requisição do tipo GET para o endereço http://localhost:8000/ola e retornar a string Olá, mundo!.

#### Requisição GET
A requisição GET é utilizada quando queremos acessar uma página. Para criar uma rota que recebe uma requisição do tipo GET, utilize o método Route::get. O método Route::get recebe dois parâmetros: o primeiro parâmetro é a URL e o segundo parâmetro é a função anônima que será executada quando a rota receber uma requisição. O código abaixo mostra como criar uma rota que recebe uma requisição do tipo GET:

```php
Route::get('/ola', function () {
	return 'Olá, mundo!';
});
```

A rota acima é responsável por receber uma requisição do tipo GET para o endereço http://localhost:8000/ola e retornar a string Olá, mundo!.

#### Requisição POST
A requisição POST é utilizada quando queremos enviar dados para o servidor. Para criar uma rota que recebe uma requisição do tipo POST, utilize o método Route::post. O método Route::post recebe dois parâmetros: o primeiro parâmetro é a URL e o segundo parâmetro é a função anônima que será executada quando a rota receber uma requisição. O código abaixo mostra como criar uma rota que recebe uma requisição do tipo POST:

```php
Route::post('/receber-dados', function () {
	return 'Olá, mundo!';
});
```

Detalhando alguns trechos do código de rotas:
```php
	Route::
``` 
- é o objeto que representa uma rota. O Laravel possui vários métodos que representam os métodos HTTP. Por exemplo, o método get() representa o método HTTP GET, o método post() representa o método HTTP POST.

```php
	function
```
- lembram do MVC? Então, aqui é onde fica a lógica da aplicação. É aqui que você vai colocar o código que vai ser executado quando a rota for acessada. Por exemplo, quando o usuário acessa a URL http://localhost:8000/ola, a rota /ola é acessada e a função anônima é executada. É comum em vez de usar função anônima, usar um controller (Veremos mais abaixo sobre controllers) pois é ideal que a lógica da aplicação fique em um controller e não em uma rota.

Então, no geral, a estrutura da rota é a seguinte:
```php
	Route::metodo_http('url', controlador_ou_funcao);
```

## Views

A view é a camada que o usuário interage com a aplicação. Por exemplo, quando o usuário acessa a página de login, a view `login.blade.php` (o nome é dado na criação) é carregada e o usuário interage com a aplicação. Em outros termos o a view é o HTML, css e javascript que o navegador interpreta e exibe para o usuário.

Em especial, o laravel usa o Blade como template engine para criar, manipular e exibir as views. O Blade vai compilar os arquivos `.blade.php` em arquivos `.php` e o PHP vai interpretar esses arquivos e exibir para o usuário. Por isso, em em alguns momentos poderemos usar códigos PHP dentro de arquivos `.blade.php`. bem como diretivas que vão facilitar a criação de código.

Os arquivos `.blade.php` são armazenados no diretório `resources/views`.

### Criando uma view
Para criar uma view, crie um arquivo com a extensão .blade.php no diretório `resources/views`. Por exemplo, para criar uma view com o nome `welcome.blade.php`, crie um arquivo com o nome `welcome.blade.php` no diretório `resources/views`. Após criar a view, crie uma rota que retorna a view. O código abaixo cria uma rota que retorna a view `welcome.blade.php`:

```php

Route::get('/bem-vindo', function () {
	return view('welcome');
});
```



### Passando dados para a view

Acima falamos que a view por usar o template engine Blade nos permite ter mais poderes em relação ao HTML,css e javascript. Um desses poderes é a possibilidade de passar dados para a view, usar condições, laços de repetição, etc. Para passar dados para a view, use como segundo parâmetro da função `view()` a função compact() que recebe como parâmetro o nome da variável e o valor da variável. O código abaixo passa a variável `nome` para a view `welcome.blade.php`:

```php

Route::get('/bem-vindo', function () {
	$nome = 'João';
	return view('welcome', compact('nome'));
});
```

Outros exemplos:

```php
Route::get('/bem-vindo', function () {
	$nome = 'João';
	$idade = 20;
	return view('welcome', compact('nome', 'idade'));
});
```

```php
Route::get('/bem-vindo', function () {
	$nome = 'João';
	$idade = 20;
	$profissao = 'Programador';
	return view('welcome', compact('nome', 'idade', 'profissao'));
});
```
**obs**: Variáveis ou informações são passadas para view comumente no controlador, mas como estamos usando uma função anônima, passamos diretamente na rota para fins didáticos.

### Exibindo dados na view

Após certificarmos que a variável foi passada para a view, podemos exibir o valor da variável na view. Para exibir o valor da variável na view, utilize a sintaxe `{{ $nome_variavel }}`. O código abaixo exibe o valor da variável `nome` na view `welcome.blade.php`:

```php
<h1>Olá, `{{ $nome }}`</h1>
```

Outros exemplos:

```php

<h1>Olá, {{ $nome }}. Você tem {{ $idade }} anos.</h1>
```

```php

<h1>Olá, {{ $nome }}. Você tem {{ $idade }} anos e é {{ $profissao }}.</h1>
```

caso a variável seja um array, podemos usar a sintaxe `{{ $nome_array['chave'] }}` para exibir o valor da variável na view. O código abaixo exibe o valor da variável `nome` na view `welcome.blade.php`:

```php

<h1>Olá, {{ $pessoa['nome'] }}. Você tem {{ $pessoa['idade'] }} anos e é {{ $pessoa['profissao'] }}.</h1>
```
### Diretivas

Diretivas blade são instruções que o blade entende e que facilitam a criação de código.  Imagine que você precisa criar um código que exibe uma mensagem caso o usuário esteja logado. Você poderia criar um código PHP que verifica se o usuário está logado e exibe a mensagem caso o usuário esteja logado. Porém, o blade possui uma diretiva que facilita a criação desse código. A diretiva @auth verifica se o usuário está logado e exibe a mensagem caso o usuário esteja logado. O código abaixo exibe a mensagem Bem-vindo, usuário! caso o usuário esteja logado:

```php

@auth
	Bem-vindo, usuário!
@endauth
```

Ou imagine que você queira mostrar um trecho html somente se a variável `$idade` seja maior que 18. Você poderia criar um código PHP que verifica se a variável `$idade` é maior que 18 e exibe o trecho html caso a variável `$idade` seja maior que 18. Porém, o blade possui uma diretiva que facilita a criação desse código. A diretiva @if verifica uma condição que pode depender do que você quer. No caso acima, podemos fazer isso:

```php

@if($idade > 18)

<h1>Olá, {{ $nome }}. Você tem {{ $idade }} anos e é {{ $profissao }}.</h1>

@endif

e finalizamos com @endif que é o fechamento da diretiva @if
```


#### Diretiva @if
A diretiva @if é usada para verificar uma condição e, com base nessa condição, decidir se o código dentro dela deve ser executado. Por exemplo:
```php
@if($idade > 18)
    <h1>Olá, {{ $nome }}. Você tem mais de 18 anos.</h1>
@endif
```
O código acima verifica se a variável $idad éé maior que 18. Se a variável $idade for maior que 18, o código dentro da diretiva @if é executado. Caso contrário, o código dentro da diretiva @if não é executado.

#### Diretiva @else
A diretiva @else é usada em conjunto com @if para definir um bloco de código que será executado quando a condição do @if for falsa. Por exemplo:
```php

@if($idade > 18)
    <h1>Olá, {{ $nome }}. Você tem mais de 18 anos.</h1>
@else
    <h1>Olá, {{ $nome }}. Você tem 18 anos ou menos.</h1>
@endif
```
O código acima verifica se a variável $idade é maior que 18. Se a variável $idade for maior que 18, o código dentro da diretiva @if é executado. Caso contrário, o código dentro da diretiva @else é executado.

#### Diretiva @elseif
A diretiva @elseif é usada quando você precisa verificar múltiplas condições em sequência. Por exemplo:
```php	
@if($idade < 18)
    <p>Você é menor de idade.</p>
@elseif($idade >= 18 && $idade < 65)
    <p>Você é um adulto.</p>
@else
    <p>Você é um idoso.</p>
@endif
```
O código acima verifica se a variável $idade é menor que 18. Se a variável $idade for menor que 18, o código dentro da diretiva @if é executado. Caso contrário, o código dentro da diretiva @elseif é executado. O código dentro da diretiva @elseif é executado se a variável $idade for maior ou igual a 18 e menor que 65. Caso contrário, o código dentro da diretiva @else é executado.

#### Diretiva @for
A diretiva @for permite que você crie loops for em suas views Blade. Isso é útil quando você deseja gerar repetidamente conteúdo com base em uma variável contadora. Por exemplo:

```php	

@for($i = 1; $i <= 5; $i++)
    <p>Este é o parágrafo número {{ $i }}</p>
@endfor
```
O código acima cria um loop for que executa 5 vezes. A variável $i é inicializada com o valor 1. A cada iteração, o valor da variável $i é incrementado em 1. O loop for é executado enquanto o valor da variável $i for menor ou igual a 5. A cada iteração, o código dentro da diretiva @for é executado.
#### Diretiva @foreach
A diretiva @foreach é usada para iterar sobre uma matriz ou coleção de dados e exibir conteúdo para cada item. Por exemplo:

```php

@foreach($pessoas as $pessoa)
	<p>Olá, {{ $pessoa['nome'] }}. Você tem {{ $pessoa['idade'] }} anos e é {{ $pessoa['profissao'] }}.</p>
@endforeach
```
O código acima itera sobre a variável $pessoas. A variável $pessoas é uma matriz que contém os dados de várias pessoas. A cada iteração, o código dentro da diretiva @foreach é executado. A variável $pessoa contém os dados de uma pessoa. O código dentro da diretiva @foreach exibe os dados de uma pessoa.
#### Diretiva @forelse
A diretiva @forelse é semelhante ao @foreach, mas permite que você especifique um bloco de código para ser executado quando a matriz ou coleção estiver vazia. Por exemplo:

```php

@forelse($carrinho as $item)
    <p>{{ $item->nome }}</p>
@empty
    <p>Seu carrinho está vazio.</p>
@endforelse
```

O código acima itera sobre a variável $carrinho. A variável $carrinho é uma matriz que contém os dados dos itens do carrinho. A cada iteração, o código dentro da diretiva @forelse é executado. A variável $item contém os dados de um item do carrinho. O código dentro da diretiva @forelse exibe os dados de um item do carrinho. Caso a variável $carrinho esteja vazia, o código dentro da diretiva @empty é executado.


#### Diretiva @empty
A diretiva @empty é usada para verificar se uma variável ou coleção está vazia. Ela é frequentemente usada em conjunto com @forelse. Por exemplo:

```php	
@forelse($itens as $item)
    <p>{{ $item->nome }}</p>
@empty
    <p>Nenhum item disponível.</p>
@endforelse
```

#### Diretiva @isset
A diretiva @isset verifica se uma variável foi definida. Se a variável estiver definida, o código dentro dela será executado. Por exemplo:

```php	
@isset($nome)
	<p>Olá, {{ $nome }}.</p>
@endisset
```

#### Diretiva @switch
A diretiva @switch é usada para criar uma estrutura de seleção semelhante ao switch em PHP. É útil quando você precisa testar uma variável em várias condições diferentes. Por exemplo:

```php
@switch($diaDaSemana)
    @case(1)
        <p>Segunda-feira</p>
        @break
    @case(2)
        <p>Terça-feira</p>
        @break
    @default
        <p>Dia desconhecido</p>
@endswitch
```

O código acima verifica o valor da variável $diaDaSemana. Se o valor da variável $diaDaSemana for 1, o código dentro da diretiva @case(1) é executado. Se o valor da variável $diaDaSemana for 2, o código dentro da diretiva @case(2) é executado. Se o valor da variável $diaDaSemana não for 1 nem 2, o código dentro da diretiva @default é executado.

#### Diretiva @include
A diretiva @include permite que você inclua outros arquivos de View em uma View atual. Isso é útil para dividir seu código em partes reutilizáveis. Por exemplo:

```php
@include('header')
```

O código acima inclui o arquivo de View `header.blade.php` na View atual. O arquivo de View header.blade.php deve estar localizado no diretório resources/views. O arquivo de View header.blade.php pode conter HTML, CSS, JavaScript, PHP, etc.
#### Diretiva @Yield

A diretiva @yield é usada para definir áreas onde o conteúdo de uma View estendida será injetado. Ela é usada em conjunto com @extends. Por exemplo:

```php
// master.blade.php
@yield('titulo')

// welcome.blade.php
@extends('master')

@section('titulo')
	<title>Minha página</title>
@endsection

ou

@extends('master')

@section('titulo', 'Minha página')

```

O código acima define uma área chamada titulo na View master.blade.php. O código abaixo estende a View master.blade.php e define o conteúdo da área titulo. O conteúdo da área titulo é inserido na View `master.blade.php`. O código abaixo estende a View master.blade.php e define o conteúdo da área titulo. O conteúdo da área titulo é injetado na View master.blade.php.

#### Diretiva @extends
A diretiva @extends  é usada para criar uma View estendida que herda o layout de outra View. Ela é usada em conjunto com @yield. Por exemplo:

```php

// master.blade.php
@yield('titulo')

// welcome.blade.php

@extends('master')

@section('titulo')
	<title>Minha página</title>
@endsection

```

O código acima define uma área chamada titulo na View master.blade.php. O código abaixo estende a View master.blade.php e define o conteúdo da área titulo. O conteúdo da área titulo é inserido na View master.blade.php. O código abaixo estende a View master.blade.php e define o conteúdo da área titulo. O conteúdo da área titulo é inserido na View master.blade.php.
#### Diretiva @section

A diretiva @section é usada para definir o conteúdo de uma área em uma View estendida. Ela é usada em conjunto com @extends. Por exemplo:

```php

// master.blade.php

@yield('titulo')

// welcome.blade.php

@extends('master')

@section('titulo', 'Minha página')

```
#### Diretiva @auth
A diretiva @auth é usada para verificar se o usuário está logado. Por exemplo:

```php

@auth
	<p>Olá, {{ Auth::user()->name }}.</p>
@endauth

```

O código acima verifica se o usuário está logado. Se o usuário estiver logado, o código dentro da diretiva @auth é executado. Caso contrário, o código dentro da diretiva @auth não é executado.

#### Diretiva @guest

A diretiva @guest é usada para verificar se o usuário não está logado. Por exemplo:

```php

@guest
	<p>Olá, visitante.</p>
@endguest

```

O código acima verifica se o usuário não está logado. Se o usuário não estiver logado, o código dentro da diretiva @guest é executado. Caso contrário, o código dentro da diretiva @guest não é executado.

### Funções de ajuda

O Laravel possui várias funções de ajuda que podem ser usadas em qualquer lugar do código. Elas são úteis para realizar tarefas comuns.

#### route( )
A função `route()` retorna a URL de uma rota nomeada (lembra que falamos sobre rotas nomeadas?). A função `route()` recebe como parâmetro o nome da rota. O código abaixo retorna a URL da rota nomeada `home`:

```php

// no routes/web.php

Route::get('/', function () {
	return view('welcome');
})->name('home');

// na view welcome.blade.php

<a href="{{ route('home') }}">Home</a>

```


#### asset( )

A função `asset()` retorna a URL de um arquivo armazenado no diretório `public`. A função `asset()` recebe como parâmetro o nome do arquivo. O código abaixo retorna a URL do arquivo `css/app.css`:

```php

<link rel="stylesheet" href="{{ asset('css/app.css') }}">

```

#### auth( )

A função `auth()` retorna uma instância da classe `AuthManager`. A classe `AuthManager` é responsável por gerenciar a autenticação. A função `auth()` é útil quando você precisa verificar se o usuário está logado. O código abaixo verifica se o usuário está logado:

```php

@if(auth()->check())
	<p>Olá, {{ auth()->user()->name }}.</p>

	ou

	<p>Olá, {{ Auth::user()->name }}.</p>
@endif

```

#### old( )

A função `old()` retorna o valor de um campo de formulário que foi enviado anteriormente (enviou e deu errado). A função `old()` recebe como parâmetro o nome do campo. O código abaixo retorna o valor do campo `nome`:

```php

<input type="text" name="nome" value="{{ old('nome') }}">

```

#### request( )

A função `request()` retorna uma instância da classe `Request`. A classe `Request` é responsável por gerenciar as requisições. A função `request()` é útil quando você precisa verificar qual é a rota atual. O código abaixo verifica se a rota atual é a rota `home`:

```php

@if(request()->routeIs('home'))
	<p>Estou na página home.</p>
@endif
```
#### session( )

A função `session()` retorna uma instância da classe `SessionManager`. A classe `SessionManager` é responsável por gerenciar as sessões. 
- Sessões são uma forma de armazenar informações sobre o usuário entre requisições.
A função `session()` é útil quando você precisa verificar se existe uma mensagem de erro na sessão. O código abaixo verifica se existe uma mensagem de erro na sessão como resultado de uma validação de formulário:

```php

@if(session('error'))
	<p>{{ session('error') }}</p>
@endif
```

## Controllers (controladores)

O controller é responsável por receber uma requisição que vem da rota e retornar uma resposta. Até o momento, ao definir as rotas nós definimos uma função que retorna uma view, mas o ideal é que a lógica da aplicação fique em um controller e não em uma rota. Por exemplo, quando o usuário acessa a página principal do sistema, a rota é responsável por chamar o método de um controller que irá carregar a página principal do sistema. Quando o usuário acessa a página de login, a rota é responsável por chamar o método de um controller que irá carregar a página de login.

### Criando um controller
Para iniciarmos o uso do *controller* então, a primeira que coisa que devemos fazer é criar um controller. Para criar um controller, utilize o comando `php artisan make:controller NomeController`. O código abaixo cria um controller chamado `HomeController`:

```bash

php artisan make:controller HomeController
```

No escopo funcional de um sistema, cada parte do sistema vai ter ações comuns que podem ser chamadas de CRUD (Create, Read, Update, Delete). O Laravel já nos fornece um controller com essas ações comuns (métodos), o `php artisan make:controller --resource NomeController`. O código abaixo cria um controller chamado `HomeController` com as ações comuns:

```bash

php artisan make:controller --resource HomeController
```

Os códigos acima vão criar um arquivo de controlador na pasta `app/Http/Controllers`. O arquivo de controlador vai conter uma classe com o nome `HomeController`. A classe `HomeController` vai conter os métodos `index()`, `create()`, `store()`, `show()`, `edit()`, `update()`, `destroy()` caso você tenha usado a terminação `--resource` no comando. Caso contrário, a classe `HomeController` vai vir sem nenhum método.


### Métodos de um controller

Os métodos de um controller são definidos usando `public function` seguido do nome do método. Por exemplo, o código abaixo define o método `index()`:

```php

public function index()
{
	// código
}
```

O código abaixo define o método `create()`:

```php

public function create()
{
	// código
}
```

Após isso, o código da lógica da aplicação é inserido dentro do método. Por exemplo, o código abaixo define o método `index()` que retorna a view `welcome.blade.php`:

```php

public function index()
{
	return view('welcome');
}
```

Então agora podemos montar um fluxo completo entre rota e controller. O código abaixo cria uma rota que chama o método `index()` do controller `HomeController`:

```php

Route::get('/', [HomeController::class, 'index']);
```

Perceba que o método `index()` do controller `HomeController` retorna a view `welcome.blade.php`. Então, quando o usuário acessa a URL http://localhost:8000, a rota é acessada e o método `index()` do controller `HomeController` é chamado. O método `index()` do controller `HomeController` retorna a view `welcome.blade.php`. A view `welcome.blade.php` é carregada e exibida para o usuário.

Quanto a sintaxe de chamar o controller, isto é, a sintaxe `[HomeController::class, 'index']`, ela é a nossa antiga função usada para retornar a view, só que agora estamos chamando o controller e o método que queremos executar. A chamada é feita usando um [ e dentro a classe referente ao controlador e o método separados por vírgula.

Veja outro exemplo:

```php

Route::get('/bem-vindo', [HomeController::class, 'BemVindo']);
```

```php

public function BemVindo()
{
	return view('outro');
}
```

Neste caso, quando o usuário acessa a URL http://localhost:8000/bem-vindo, a rota é acessada e o método `BemVindo()` do controller `HomeController` é chamado. O método `BemVindo()` do controller `HomeController` retorna a view `outro.blade.php`. A view `outro.blade.php` é carregada e exibida para o usuário.

## Migrações (migrations)

A migração é responsável por criar e alterar a estrutura do banco de dados. Por exemplo, se o sistema possui uma tabela chamada `pessoas`, a migração é responsável por criar a tabela `pessoas` já com os campos que você deseja. 

Antes você precisava acessar o banco de dados e criar as tabelas manualmente. Com o Laravel, você pode criar as tabelas usando migrações. As migrações são arquivos PHP que contém instruções para criar e alterar a estrutura do banco de dados. As migrações são armazenadas no diretório `database/migrations`.

### Criando uma migração

Para criarmos uma migração, utilizamos o comando `php artisan make:migration NomeMigracao`. O ideal é já ter criado a migration junto com o modelo e o controlador, pois assim já criamos a migration com o nome da tabela que queremos. O código abaixo cria uma migração chamada `create_pessoas_table`:

```bash
	php artisan make:migration create_pessoas_table
```

### Métodos de uma migração

Assim que criamos uma migração, ela já vem com alguns códigos. Como no exemplo abaixo:

```php
<?php

use Illuminate\Database\Migrations\Migration;

class CreatePessoasTable extends Migration
{
	/**
	 * Run the migrations.
	 *
	 * @return void
	 */
	public function up()
	{
		Schema::create('pessoas', function (Blueprint $table) {
			$table->id();
			$table->timestamps();
		});
	}

	/**
	 * Reverse the migrations.
	 *
	 * @return void
	 */
	public function down()
	{
		Schema::dropIfExists('pessoas');
	}
}

```

O código base da criação de uma tabela é esse. O método `up()` é responsável por criar a tabela e o método `down()` é responsável por deletar a tabela. A classe Schema é responsável por criar e alterar a estrutura do banco de dados. O método `create()` cria uma tabela.
Veja que para definirmos o nome da nossa tabela no banco de dados, usamos o método `create()` e passamos como parâmetro o nome da tabela.

### Adicionando colunas a uma tabela

Na construção de um sistema, é normal que tenha várias tabelas, e essas tabelas possuam várias colunas para guardar os dados. Para 
adicionar colunas para nossa migração, vamos dentro da função da Classe Schema, que é a função `create()`, e vamos adicionar as colunas que queremos. 

#### Tipos de colunas e como criar

##### ID

O tipo de coluna ID é um tipo de coluna que é muito usado para identificar um registro. P Por exemplo, se temos uma tabela chamada `pessoas`, é comum que a tabela `pessoas` possua uma coluna chamada `id` que é responsável por identificar uma pessoa. Para criar uma coluna do tipo ID, utilize o método `id()`:

```php
	$table->id();
```

##### String

O tipo de coluna String é um tipo de coluna que é muito usado para guardar textos. Por exemplo, se temos uma tabela chamada `pessoas`, é comum que a tabela `pessoas` possua uma coluna chamada `nome` que é responsável por guardar o nome de uma pessoa. Para criar uma coluna do tipo String, utilize o método `string()`:

```php
	$table->string('nome');
```


##### Integer

O tipo de coluna Integer é um tipo de coluna que é muito usado para guardar números inteiros. Por exemplo, se temos uma tabela chamada `pessoas`, é comum que a tabela `pessoas` possua uma coluna chamada `idade` que é responsável por guardar a idade de uma pessoa. Para criar uma coluna do tipo Integer, utilize o método `integer()`:

```php
	$table->integer('idade');
```

##### Text

O tipo de coluna Text é um tipo de coluna que é muito usado para guardar textos grandes. Por exemplo, se temos uma tabela chamada `pessoas`, é comum que a tabela `pessoas` possua uma coluna chamada `descricao` que é responsável por guardar a descrição de uma pessoa. Para criar uma coluna do tipo Text, utilize o método `text()`:

```php
	$table->text('descricao');
```

##### Boolean

O tipo de coluna Boolean é um tipo de coluna que é muito usado para guardar valores booleanos. Por exemplo, se temos uma tabela chamada `pessoas`, é comum que a tabela `pessoas` possua uma coluna chamada `ativo` que é responsável por guardar se uma pessoa está ativa ou não. Para criar uma coluna do tipo Boolean, utilize o método `boolean()`:

```php
	$table->boolean('ativo');
```

##### Timestamps

O tipo de coluna Timestamps é um tipo de coluna que é muito usado para guardar a data e hora de criação e atualização de um registro. Por exemplo, se temos uma tabela chamada `pessoas`, é comum que a tabela `pessoas` possua uma coluna chamada `created_at` que é responsável por guardar a data e hora de criação de uma pessoa e uma coluna chamada `updated_at` que é responsável por guardar a data e hora de atualização de uma pessoa. Para criar uma coluna do tipo Timestamps, utilize o método `timestamps()`:

```php
	$table->timestamps();
```

##### Datetime

O tipo de coluna Datetime é um tipo de coluna que é muito usado para guardar a data e hora de um evento. Por exemplo, se temos uma tabela chamada `pessoas`, é comum que a tabela `pessoas` possua uma coluna chamada `data_nascimento` que é responsável por guardar a data e hora de nascimento de uma pessoa. Para criar uma coluna do tipo Datetime, utilize o método `datetime()`:

```php
	$table->datetime('data_nascimento');
```


##### Decimal


O tipo de coluna Decimal é um tipo de coluna que é muito usado para guardar números decimais. Por exemplo, se temos uma tabela chamada `pessoas`, é comum que a tabela `pessoas` possua uma coluna chamada `altura` que é responsável por guardar a altura de uma pessoa. Para criar uma coluna do tipo Decimal, utilize o método `decimal()`:

```php
	$table->decimal('altura');
```

Ainda podemos passar como parâmetro a quantidade de casas decimais que queremos e a quantidade de casas antes da vírgula. Por exemplo, o código abaixo cria uma coluna chamada `altura` que é responsável por guardar a altura de uma pessoa. A coluna `altura` possui 2 casas decimais e 3 casas antes da vírgula:

```php
	$table->decimal('altura', 5, 2);
```

##### min, max e nullable

Após criarmos uma coluna podemos definir o tamanho mínimo e máximo da coluna. Por exemplo, o código abaixo cria uma coluna chamada `nome` que é responsável por guardar o nome de uma pessoa. A coluna `nome` possui no mínimo 3 caracteres e no máximo 100 caracteres:

```php
	$table->string('nome')->min(3)->max(100);
```

Ou ainda podemos definir se a coluna pode ser nula ou não. Por exemplo, o código abaixo cria uma coluna chamada `nome` que é responsável por guardar o nome de uma pessoa. A coluna `nome` pode ser nula:

```php
	$table->string('nome')->nullable()->max(100);
```

##### unique

Podemos definir se uma coluna deve ser única ou não. Por exemplo, o código abaixo cria uma coluna chamada `email` que é responsável por guardar o email de uma pessoa. A coluna `email` deve ser única:

```php
	$table->string('email')->unique();
```

##### default

Podemos definir um valor padrão para uma coluna. Por exemplo, o código abaixo cria uma coluna chamada `ativo` que é responsável por guardar se uma pessoa está ativa ou não. A coluna `ativo` possui o valor padrão `true`:

```php
	$table->boolean('ativo')->default(true);
```


##### foreignId

O conceito de banco de dados é muito importante na construção de sistemas. Como é de constume, um sistema sempre terá tabelas se relacionando entre si, isto é, um registro de uma tabela pode estar relacionado com um registro de outra tabela. Por exemplo, se temos uma tabela chamada `pessoas` e uma tabela chamada `cidades`, é comum que a tabela `pessoas` possua uma coluna chamada `cidade_id` que é responsável por guardar o id da cidade de uma pessoa. Para criar uma coluna do tipo foreignId, utilize o método `foreignId()`:

```php
	$table->foreignId('cidade_id');
```

##### constrained

Após criarmos uma coluna do tipo foreignId, podemos definir a tabela e a coluna que a coluna do tipo foreignId está relacionada. Por exemplo, o código abaixo cria uma coluna chamada `cidade_id` que é responsável por guardar o id da cidade de uma pessoa. A coluna `cidade_id` está relacionada com a tabela `cidades` e com a coluna `id` da tabela `cidades`:

```php
	$table->foreignId('cidade_id')->constrained('cidades');
```

##### onDelete

Após criarmos uma coluna do tipo foreignId, podemos definir o que acontece com os registros relacionados quando um registro é deletado. Por exemplo, o código abaixo cria uma coluna chamada `cidade_id` que é responsável por guardar o id da cidade de uma pessoa. A coluna `cidade_id` está relacionada com a tabela `cidades` e com a coluna `id` da tabela `cidades`. Quando um registro da tabela `cidades` é deletado, os registros relacionados da tabela `pessoas` são deletados:

```php
	$table->foreignId('cidade_id')->constrained('cidades')->onDelete('cascade');
```

##### onUpdate

Após criarmos uma coluna do tipo foreignId, podemos definir o que acontece com os registros relacionados quando um registro é atualizado. Por exemplo, o código abaixo cria uma coluna chamada `cidade_id` que é responsável por guardar o id da cidade de uma pessoa. A coluna `cidade_id` está relacionada com a tabela `cidades` e com a coluna `id` da tabela `cidades`. Quando um registro da tabela `cidades` é atualizado, os registros relacionados da tabela `pessoas` são atualizados:

```php
	$table->foreignId('cidade_id')->constrained('cidades')->onUpdate('cascade');
```



### Executando uma migração

Após criarmos uma migração, precisamos executar a migração para que a tabela seja criada no banco de dados. Para executarmos uma migração, utilizamos o comando `php artisan migrate`. O código abaixo executa a migração:

```bash
	php artisan migrate
```

Haverá casos que você precisa migrar os dados novamente após fazer modificações na migração. Então, para isso, você pode usar o comando `php artisan migrate:fresh`. O código abaixo executa a migração novamente e deleta a estrutura do banco de dados antiga:

```bash
	php artisan migrate:fresh
```
## Modelos (models)

O modelo é responsável por representar uma tabela do banco de dados. Por exemplo, se o sistema possui uma tabela chamada `pessoas`, o modelo `Pessoa` é responsável por representar a tabela `pessoas` e realizar operações no banco de dados relacionadas a tabela `pessoas`. Por exemplo, o modelo `Pessoa` é responsável por inserir, atualizar, deletar e consultar dados da tabela `pessoas`.

### Criando um modelo

Para criarmos um modelo, utilizamos o comando `php artisan make:model NomeModelo`. O código abaixo cria um modelo chamado `Pessoa`:

```bash

php artisan make:model Pessoa
```	

Além disso, caso você queira agilizar o desenvolvimento, você pode criar o modelo e já criar a migração e com o controlador, tudo de uma vez só. Veja os três exemplos abaixo:

```bash

php artisan make:model Pessoa -m -c
```
Esse comando cria o modelo, a migração e o controlador.

```bash

php artisan make:model Pessoa -m
```

Esse comando cria o modelo e a migração.

```bash

php artisan make:model Pessoa -c
```

Esse comando cria o modelo e o controlador.

### Métodos de um modelo

Os modelos criados no laravel já possuem alguns métodos que facilitam a manipulação dos dados. Os métodos mais comuns são:
- `all()`: retorna todos os registros da tabela.
- `find($id)`: retorna o registro com o id passado como parâmetro.
- `create($dados)`: cria um novo registro com os dados passados como parâmetro.
- `update($dados)`: atualiza um registro com os dados passados como parâmetro.
- `delete()`: deleta o registro.
- `where($campo, operador ,$valor)`: retorna os registros que possuem o valor passado como parâmetro no campo passado como parâmetro.
- `whereBetween($campo, [$valor1, $valor2])`: retorna os registros que possuem o valor passado como parâmetro no campo passado como parâmetro.
- `whereNotBetween($campo, [$valor1, $valor2])`: retorna os registros que não possuem o valor passado como parâmetro no campo passado como parâmetro.
- `whereNull($campo)`: retorna os registros que possuem o valor nulo no campo passado como parâmetro.
- `whereNotNull($campo)`: retorna os registros que não possuem o valor nulo no campo passado como parâmetro.
- `whereIn($campo, [$valor1, $valor2])`: retorna os registros que possuem o valor passado como parâmetro no campo passado como parâmetro.
- `get()`: retorna os registros que possuem o valor passado como parâmetro no campo passado como parâmetro.
- `first()`: retorna o primeiro registro que possui o valor passado como parâmetro no campo passado como parâmetro.
- `paginate($quantidade)`: retorna os registros que possuem o valor passado como parâmetro no campo passado como parâmetro.
- `orderBy(campo, ordem)`: retorna os dados com a ordenação passada como parâmetro.
- `count()`: retorna a quantidade de registros.
- `sum($campo)`: retorna a soma dos valores do campo passado como parâmetro.

Esse são os métodos mais comuns, mas existem outros métodos que podem ser usados. Para saber mais sobre os métodos, acesse a [documentação](https://laravel.com/docs/8.x/eloquent#retrieving-models) do laravel.

Vale ressaltar que alguns métodos podem ser usados de forma estática, ou seja, sem a necessidade de instanciar o modelo. Por exemplo, o método `all()` pode ser usado de forma estática. Já outros como update() e delete() precisam ser usados com uma instância do modelo. Veja os exemplos abaixo:

```php

// usando o método all() de forma estática

Pessoa::all();

// usando o método all() com uma instância do modelo

$pessoa = new Pessoa();

$pessoa->all();

```

Veja a tabela abaixo com exemplo de cada método acima:

| Método | Exemplo |
| ------ | ------ |
| all() | Pessoa::all() |
| find($id) | Pessoa::find(1) |
| create($dados) | Pessoa::create(['nome' => 'João']) |
| update($dados) | $pessoa = Pessoa::find(1); $pessoa->update(['nome' => 'João']) |
| delete() | $pessoa = Pessoa::find(1); $pessoa->delete() |
| where($campo, operador ,$valor) | Pessoa::where('nome', 'João')->get() |
| whereBetween($campo, [$valor1, $valor2]) | Pessoa::whereBetween('idade', [18, 65])->get() |
| whereNotBetween($campo, [$valor1, $valor2]) | Pessoa::whereNotBetween('idade', [18, 65])->get() |
| whereNull($campo) | Pessoa::whereNull('nome')->get() |
| whereNotNull($campo) | Pessoa::whereNotNull('nome')->get() |
| whereIn($campo, [$valor1, $valor2]) | Pessoa::whereIn('nome', ['João', 'Maria'])->get() |
| get() | Pessoa::where('nome', 'João')->get() |
| first() | Pessoa::where('nome', 'João')->first() |
| paginate($quantidade) | Pessoa::paginate(10) |
| orderBy(campo, ordem) | Pessoa::orderBy('nome', 'asc')->get() |
| count() | Pessoa::count() |
| sum($campo) | Pessoa::sum('idade') |
### Relacionamentos
