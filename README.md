# API de Usuários

API de Usuários desenvolvida como desafio técnico para o cargo de desenvolvedor PHP.

## 🚀 Começando

Essas instruções permitirão que você obtenha uma cópia do projeto em operação na sua máquina local para fins de desenvolvimento e teste.

### 📋 Pré-requisitos

De que coisas você precisa para instalar o software e como instalá-lo?

```
PHP 8.0 ou superior
Banco de Dados MySQL 8 ou superior
Você também pode rodar a partir do Docker, basta rodar dentro do diretório da aplicação o comando 'docker-compose up -d' para levantar todo o ambiente necessário
```

## 📦 Implantação

Basta clonar o projeto para para um diretório de sua preferência e inicializar o servidor embutido do próprio Laravel para levantar a aplicação. <br/>
Em seguida faça um cópia do arquivo '.env.example' com o nome '.env', e adicione as credenciais do banco de dados que você instalou. <br/>
Rode o comando 'composer install' para instalar as dependências da aplicação. <br/>
Rode o comando 'php artisan migrate' para rodar as migrations de versionamento do banco de dados. <br/>
Rode o comando 'php artisan key:generate' para gerar a chave de segurança da aplicação. <br/>

## 💻 Usando a Aplicação (Lista de end-points)

Rotas públicas:

- Registrar novo usuário: http://localhost:8000/api/register (POST) <br/>

```

{
    "name": "Fulano",
    "email": "fulano@example.com",
    "password": "senha1234"
}

```

- Logar na API: http://localhost:8000/api/login (POST)

```

{
    "email": "paulo@example.com",
    "password": "senha1234"
}

```

OBS: Após logar você receberá um token como resposta que deverá ser usado nas requisições para todas as rotas protegidas (Bearer Token).

Rotas protegidas:

- Buscar todos os usuários: http://localhost:8000/api/users (GET)
- Buscar usuário por ID: http://localhost:8000/api/users/{id} (GET)
- Alterar usuário: http://localhost:8000/api/users/{id} (PUT)

```

{
    "name": "Fulano de Tal",
    "email": "fulano_de_tal@example.com",
    "password": "senha12345678"
}

```

- Deletar usuário: http://localhost:8000/api/users/{id} (DELETE)
- Sair (revogar autenticação): http://localhost:8000/api/logout (POST)

## 🛠️ Construído com

* [Laravel](https://laravel.com/) - Framework utilizado
