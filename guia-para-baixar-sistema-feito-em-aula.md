# Passo a passo para baixar o sistema de Blog que está sendo feito em sala de aula usando o framework Laravel

Para você baixar o sistema de Blog que está sendo feito em sala de aula, você deverá seguir os seguintes passos:

## 1. Escolha uma pasta onde você irá baixar o sistema

Na nossa aula, usamos a pasta `C:\xampp\` para criar uma nova pasta para guardar o sistema. Você pode escolher qualquer pasta, mas é importante que você lembre onde você salvou o sistema.


## 2. Baixe o sistema usando o Git

Para baixar o sistema, abra o terminal onde você deseja baixar o sistema (na sua pasta) e digite o seguinte comando:

```bash

git clone https://github.com/Gabriel-stack/blog-de-noticia-em-sala.git
```

## 3. Instale as dependências do sistema

O código acima irá criar uma pasta chamada `blog-de-noticia-em-sala`. Abra esta pasta no vscode e abra o terminal do vscode. No terminal, digite o seguinte comando:

```bash
composer install
```

## 4. Crie o arquivo `.env`

O arquivo env é importante para o funcionamento do sistema. Para criar o arquivo, digite o seguinte comando no terminal do vscode:

```bash
cp .env.example .env
```

## 5. Gere a chave do sistema

Para gerar a chave do sistema, digite o seguinte comando no terminal do vscode:

```bash

php artisan key:generate
```

## 6. Rode o sistema

Para rodar o sistema, digite o seguinte comando no terminal do vscode:

```bash
php artisan serve
```