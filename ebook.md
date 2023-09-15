# Apostila de Desenvolvimento Web com Laravel para disciplina de Desenvolvimento Web do 6º semestre do curso de Informática

##### Descrição:

Esta apostila servirá como guia para entender os conceitos básicos de desenvolvimento web com Laravel. O objetivo é que o aluno entenda os conceitos básicos de desenvolvimento web e que consiga desenvolver um sistema web simples utilizando o framework Laravel.

Um vez que as aulas são corridas, com pouco e existe muitos imprevistos. A apostila servirá como um guia para o aluno que não conseguiu acompanhar as aulas ou que deseja revisar os conceitos. Além disso, alguns conceitos vistos aqui servirão para prova da primeira unidade.

#### Sumário


1. [Introdução](#introdução)
	1. [O que é um framework?](#o-que-é-um-framework)
	2. [O que é o Laravel?](#o-que-é-o-laravel)
		1. [Vantagens de usar o Laravel](#vantagens-de-usar-o-laravel)
		2. [Desvantagens de usar o Laravel](#desvantagens-de-usar-o-laravel)
	3. [O que é o MVC?](#o-que-é-o-mvc)
	4. [O que é o Composer?](#o-que-é-o-composer)
2. [Instalação](#instalação)
	1. [Instalação do Composer](#instalação-do-composer)
	2. [Instalação do Laravel](#instalação-do-laravel)
	3. [Instalação do XAMPP](#instalação-do-xampp)
	4. [Criando um projeto Laravel](#criando-um-projeto-laravel)
	5. [Estrutura de um projeto Laravel](#estrutura-de-um-projeto-laravel)
3. [Rotas](#rotas)
	1. [Rotas nomeadas](#rotas-nomeadas)
	2. [Rotas anônimas](#rotas-anônimas)
	3. [Métodos HTTP](#métodos-http)
4. [Views](#views)
	1. [Criando uma view](#criando-uma-view)
	2. [Passando dados para a view](#passando-dados-para-a-view)
	3. [Exibindo dados na view](#exibindo-dados-na-view)
	4. [Diretivas](#diretivas)
		1. [Diretiva @if](#diretiva-if)
		2. [Diretiva @else](#diretiva-else)
		3. [Diretiva @elseif](#diretiva-elseif)
		4. [Diretiva @for](#diretiva-for)
		5. [Diretiva @foreach](#diretiva-foreach)
		6. [Diretiva @forelse](#diretiva-forelse)
		7. [Diretiva @empty](#diretiva-empty)
		8. [Diretiva @isset](#diretiva-isset)
		9. [Diretiva @switch](#diretiva-switch)
		10. [Diretiva @include](#diretiva-include)
		11. [Diretiva @yield](#diretiva-yield)
		12. [Diretiva @extends](#diretiva-extends)
		13. [Diretiva @section](#diretiva-section)
		14. [Diretiva @auth](#diretiva-auth)
		15. [Diretiva @guest](#diretiva-guest)
	5. [Funções de ajuda](#funções-de-ajuda)
		1. [Função route()](#route)
		2. [Função asset()](#asset)
		3. [Função auth()](#auth)
		4. [Função old()](#old)
		5. [Função request()](#request)
		6. [Função session()](#session)




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
<h1>Olá, &lbrace;&lbrace{{ $nome }}&rbrace;&rbrace</h1>
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
