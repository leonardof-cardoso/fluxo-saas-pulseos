# PulseOS

PulseOS e a base de um SaaS de gestao pensado para pequenos negocios que vivem de operacao, agenda e relacionamento com clientes.

A proposta aqui nao e ser apenas um sistema "bonito". A ideia e construir um produto com cara comercial, organizado desde o inicio e pronto para evoluir para um SaaS real.

Esse projeto foi desenhado para atender cenarios como:

- barbearias
- academias
- clinicas
- freelancers
- pequenos negocios em geral

## Visao do produto

O foco do PulseOS e reunir em um unico lugar:

- autenticacao de usuarios e empresas
- cadastro de clientes
- agendamentos
- controle de pagamentos
- dashboard operacional
- notificacoes

Tudo isso com uma interface limpa, moderna e sem cara de template generico.

## Stack

- Python
- Django
- PostgreSQL em producao
- SQLite para desenvolvimento rapido
- Django Templates
- CSS custom moderno

## Estrutura das apps
 
- `accounts`
- `clients`
- `appointments`
- `payments`
- `dashboard`
- `notifications`

## Como rodar localmente

1. Entre na pasta do projeto.
2. Crie e ative um ambiente virtual, se ainda nao existir.
3. Instale as dependencias:

```bash
pip install -r requirements.txt
```

4. Configure as variaveis de ambiente com base no arquivo `.env.example`.
5. Para desenvolvimento local simples, mantenha `USE_SQLITE=True`.
6. Rode as migracoes:

```bash
python manage.py migrate
```

7. Inicie o servidor:

```bash
python manage.py runserver
```

8. Abra no navegador:

```text
http://127.0.0.1:8000/
```

## Acesso de teste

Para facilitar a avaliacao local, existe um usuario administrativo de desenvolvimento:

- Admin: `http://127.0.0.1:8000/admin/`
- Usuario: `admin`
- Senha: `PulseAdmin123!`

Esse acesso e apenas para ambiente local de teste.

## Variaveis de ambiente

O projeto aceita as seguintes configuracoes:

- `SECRET_KEY`
- `DEBUG`
- `USE_SQLITE`
- `ALLOWED_HOSTS`
- `DB_NAME`
- `DB_USER`
- `DB_PASSWORD`
- `DB_HOST`
- `DB_PORT`

## Estado atual

Neste momento, a base inicial ja inclui:

- estrutura do projeto Django
- apps separadas por dominio
- template base
- home inicial com direcao visual moderna
- configuracao pronta para banco local e futura evolucao

## Proximos passos

As proximas etapas naturais do produto sao:

- autenticacao completa
- multi-tenant por empresa
- CRUD de clientes
- sistema de agendamento
- dashboard com dados reais
- pagamentos e notificacoes
