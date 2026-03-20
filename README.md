# pwiii-enzo-silva
Aula de programação de Web III com o professor João Siles

# Guia de Instalação - Laravel 12.x

O Laravel é um framework de aplicação web com sintaxe expressiva e elegante, projetado para ser progressivo e crescer junto com as necessidades do desenvolvedor. Este guia detalha o processo de instalação e configuração inicial baseado na documentação oficial.

# 📋 Pré-requisitos

Antes de criar seu projeto, certifique-se de que sua máquina possui:

-   **PHP**
-   **Composer**
-   **Laravel Installer**
-   **Node e NPM** (ou Bun) para compilar ativos do frontend.

**Dica:** Se você não possui PHP ou Composer, utilize os comandos recomendados pelo site `php.new` para automatizar a instalação no macOS, Windows ou Linux. Após a execução, reinicie seu terminal.

Se já possuir o PHP e o Composer, instale o instalador globalmente:

```
composer global require laravel/installer

```

# 🚀 Criando a Aplicação

## Para iniciar um novo projeto, utilize o instalador do Laravel. Ele iniciará um processo interativo para configurar:

1.  Framework de testes preferido.
2.  Banco de dados inicial.
3.  Starter Kit (opcional), para scaffolding de autenticação.

```
laravel new nome-do-projeto

```

# ⚙️ Configuração Inicial

Servidor de Desenvolvimento

Após criar a aplicação, navegue até o diretório e execute o script para iniciar o servidor local, o worker de filas e o servidor Vite simultaneamente:

```
cd nome-do-projeto
composer run dev

```

A aplicação estará acessível em `http://localhost:8000`.

## Ambiente e Banco de Dados

-   **Arquivo .env:** As configurações variam entre ambientes local e produção e são armazenadas no arquivo `.env` na raiz do projeto. **Nunca envie este arquivo para o controle de versão**, pois ele contém credenciais sensíveis.
-   **SQLite:** Por padrão, o Laravel utiliza SQLite e cria automaticamente o arquivo `database/database.sqlite` com as migrações iniciais já executadas.
-   **Outros Bancos:** Para usar MySQL ou PostgreSQL, atualize as variáveis `DB_*` no seu arquivo `.env` e execute as migrações manualmente.

# 🛠️ Alternativa: Laravel Herd

Para uma experiência nativa e ultra rápida no macOS ou Windows, recomenda-se o **Laravel Herd**.

-   Inclui PHP, Nginx e ferramentas de linha de comando (`composer`, `laravel`, `node`, etc.).
-   No **macOS**, o instalador configura o Nginx para rodar em segundo plano e usa o domínio `.test` para pastas dentro de `~/Herd`.
-   No **Windows**, o diretório padrão é `%USERPROFILE%\Herd`.

# 🤖 Suporte a IA

O Laravel é otimizado para desenvolvimento assistido por IA devido às suas convenções rígidas. Para potencializar isso, você pode instalar o **Laravel Boost**, que fornece contexto específico do framework para agentes de IA.

```
composer require laravel/boost --dev
php artisan boost:install

```

--------------------------------------------------------------------------------