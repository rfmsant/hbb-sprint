# HBB Sprint

Quadro de tarefas da HBB até ao go-live (8 mar 2027). Site estático (GitHub Pages) com Firebase (login Google + Firestore).

## Configurar (cerca de 15 minutos)

1. **Criar o projeto Firebase**: console.firebase.google.com → Adicionar projeto (ex.: hbb-sprint). Pode desativar o Google Analytics.
2. **Login Google**: Authentication → Começar → Método de início de sessão → Google → Ativar.
3. **Firestore**: Firestore Database → Criar base de dados → modo de produção → localização **europe-west** (ex.: eur3).
4. **Regras**: Firestore → Regras → colar o conteúdo de firestore.rules → Publicar.
5. **Quem tem acesso**: Firestore → Dados → Iniciar coleção **members**. Para cada pessoa, um documento com o **ID = email Google** (ex.: rui@gmail.com) e um campo **name** (texto) com o primeiro nome: Rui, Xavi, Flor, Margarida. O primeiro nome tem de ser igual ao "Responsável" das tarefas, para o filtro "Minhas" funcionar.
6. **App web**: Definições do projeto → As tuas apps → ícone </> → registar (sem Hosting) → copiar o objeto firebaseConfig para firebase-config.js.
7. **Domínio autorizado**: Authentication → Definições → Domínios autorizados → Adicionar **rfmsant.github.io** (e mais tarde o domínio da HBB).
8. **Publicar no GitHub**: criar um repositório (ex.: hbb-sprint), enviar estes ficheiros, Settings → Pages → Branch main / root. O site fica em https://rfmsant.github.io/hbb-sprint/.
9. **Primeira entrada**: entrar com Google; com a base vazia aparece o botão "Importar as 57 tarefas do backlog". Depois de importar, pode apagar seed-tasks.json do repositório.

## Notas
- A configuração do Firebase não é secreta; quem controla o acesso são as regras + a coleção members. Os emails ficam só no Firestore, não no repositório.
- O plano gratuito do Firebase (Spark) chega com folga para isto.
- Telemóvel: separadores por estado (deslizar para o lado muda de coluna), botão → avança a tarefa, + Tarefa em baixo. No telemóvel pode "Adicionar ao ecrã principal".
