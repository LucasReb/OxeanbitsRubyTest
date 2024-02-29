### Desafio para vaga de BackEnd - Foco em Ruby On Rails

![image](https://github.com/LucasReb/OxeanbitsRubyTest/assets/54152996/e231a5fc-6ba0-4ea7-8492-f6b47e1dd987)

Objetivo do Desafio:

O objetivo deste desafio é avaliar suas habilidades no desenvolvimento com o framework Ruby On Rails, bem como quaisquer integrações necessárias, a implementação de funcionalidades que executam em segundo plano de forma síncrona, a escrita de testes e a criação de uma documentação clara.

#### Requisitos:

- ruby-3.1.4
- sqlite3
- redis-server (pré requisito para rodar o sidekiq) 

Clone o projeto e ao executar:

```ruby
bundle install
rails db:migrate
rails db:seed
```
Será configurado uma aplicação rails contando com as seguintes funcionalidades:
- Usuário padrão admin@rotten e senha admin
- Página de login
- Rota para criação de novos usuários
- Rota para cadastrar novo filme
- Rotas para dar nota nos filmes
- Rota para criar filmes em massa (Sidekiq)
- Rota para dar nota aos filmes em massa (Sidekiq)
- Rota para excluir filmes e massa (Sidekiq)
- Exibi a média das notas de cada filme

#### Para rodar o código:

```ruby
redis-server (para conexão com sidekiq funcionar)
sidekiq (dentro do projeto - para habilitar workers de segundo plano)
rails s
rspec (para testar rotas)
```

#### Desafio Concluído:

Implementei rotas para importar e submeter notas de filmes em massa, utilizando Sidekiq para execução assíncrona. As rotas suportam payloads JSON para facilitar a integração e garantir uma experiência eficiente aos usuários. Os testes foram escritos com RSpec, garantindo o funcionamento correto das funcionalidades.
