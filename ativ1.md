# Atividade 1 — FocoEstudos

1. Quais tabelas foram definidas inicialmente?

Pensei em 4 tabelas principais:
- users: guarda os dados de login e cadastro.
- subjects: guarda as matérias que a pessoa vai estudar.
- notes: guarda os textos e resumos das abas de anotações.
- study_sessions: guarda o tempo de cada sessão do cronômetro.

2. Foram utilizadas migrations? Se sim, quantas e qual a descrição de cada uma?

Sim, fiz 4 migrations em arquivos .sql separados:
- 001_create_users.sql: cria a tabela de usuários.
- 002_create_subjects.sql: cria a tabela das matérias.
- 003_create_notes.sql: cria a tabela das anotações.
- 004_create_study_sessions.sql: cria a tabela para salvar os tempos do cronômetro.

3. Qual é o caminho do arquivo que gera a seed do banco?

backend/app/database/seed.py

4. Quais endpoints serão implementados inicialmente? Justifique.

- POST /users — criar conta.
- POST /auth/login — fazer login.
- GET /subjects — listar as matérias.
- GET /notes — listar todas as anotações.
- POST /notes — criar uma anotação nova.
- PUT /notes/:id — editar uma anotação.
- DELETE /notes/:id — excluir uma anotação.
- POST /study-sessions — salvar o tempo de uma sessão.
- GET /study-sessions/total — ver o total de tempo estudado.

Justificativa: Comecei por esses porque eles são o básico para o app funcionar. O usuário precisa conseguir logar, gerenciar os resumos e salvar o tempo do cronômetro antes de qualquer outra funcionalidade extra.

5. Está sendo utilizado algum framework para escrever os endpoints? Se sim, qual?

Sim. Vou usar o FastAPI (Python) para criar os endpoints da API. Pro banco de dados, vou usar o SQLAlchemy como ORM para conversar com o PostgreSQL.
