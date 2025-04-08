![image](https://github.com/user-attachments/assets/e25ea532-e1c4-42e2-8665-722a5feb16b7)# plantinhas
Agrupador plantinhas

# Diagrama ER
```mermaid
erDiagram
  User {
    string first_name
    string last_name
    string username
    string email
    string contato
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
    string origem
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
    int quantidade_completadas
    string cron
  }

  Pericia {
    string nome
    string descricao
    float multiplicador_xp
  }

  Habilidade {
    string tipo
    string api_hint
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
