# plantinhas
Agrupador plantinhas

# Diagrama ER
```mermaid
erDiagram
  User {
    string first_name
    string last_name
    string username
    string email
    string contact
    date birthday
    string photo
  }

  Planta {
    string nome
    string foto
    string horas_sol
    string solo_ideal
    string ventilacao
    string temperatura_ideal
    string estacao_plantio
    int dias_maturidade
    string categoria
    int dificuldade
  }

  PlantaPlantio {
    float saude
    float sede
  }

  Plantio {
    date data_plantio
    date data_prevista_colheita
    string localizacao
    string espaco_disponivel
    string status
    float nota_experiencia
  }

  Problema {
    string nome
    string descricao
    string tratamento
  }

  TutorialPlantio {
    string titulo
    string descricao
    int ordem
    string foto
  }

  Tarefa {
    string descricao
    string tipo
    string frequencia
    int quantidade_total
    int quantidade_completada
    string cron
  }

  Pericia {
    string nome
    string descricao
    float multiplicador_xp
  }

  Habilidade {
    string tipo
    int xp
    int nivel
  }

  Requisitos {
  }

  PostFeed {
    string legenda
    list photos
    list qtde_likes
  }

  ComentariosPostFeed {
    string conteudo
  }

  Like {
  }

  PostForum {
    string legenda
    list photos
    int qtde_upvotes
    int qtde_downvotes
  }

  ComentariosPostForum {
    string conteudo
  }

  Upvote {
  }

  DownVote {
  }

  %% Relationships
  User ||--o{ PostFeed : creates
  User ||--o{ PostForum : creates
  User ||--o{ ComentariosPostFeed : writes
  User ||--o{ ComentariosPostForum : writes
  User ||--o{ Like : likes
  User ||--o{ Upvote : votes
  User ||--o{ DownVote : votes
  User ||--o{ Plantio : owns
  User ||--o{ Habilidade : has

  PostFeed ||--o{ ComentariosPostFeed : has
  PostFeed ||--o{ Like : receives

  PostForum ||--o{ ComentariosPostForum : has
  PostForum ||--o{ Upvote : receives
  PostForum ||--o{ DownVote : receives

  Plantio ||--o{ PlantaPlantio : links
  Planta ||--o{ PlantaPlantio : links

  Plantio ||--o{ Problema : has
  Plantio ||--o{ TutorialPlantio : uses
  Plantio ||--o{ Tarefa : schedules

  TutorialPlantio ||--o{ Tarefa : contains

  Tarefa ||--o{ Requisitos : needs
  Habilidade ||--o{ Requisitos : fulfills

  Habilidade }o--|| Pericia : belongs_to
```
