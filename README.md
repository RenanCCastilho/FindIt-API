# Find It API

![Java](https://img.shields.io/badge/Java-17-ED8B00?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.1-6DB33F?logo=springboot&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle_DB-F80000?logo=oracle&logoColor=white)

API REST do **Find It**, um app para encontrar estabelecimentos de serviço próximos, como barbearias, salões e fretes, e agendar horários com eles. Com ela, o usuário vê a distância de cada empresa, marca favoritos e gerencia seus agendamentos.

📄 Apresentação do projeto: [`FindIT.pdf`](FindIT.pdf) · 🎬 Vídeo: [YouTube](https://youtu.be/X9xjomWAvEI)

## Funcionalidades

- CRUD de **empresas** (nome, segmento, endereço, distância em km e favorito)
- CRUD de **usuários** (nome, telefone, e-mail e CPF)
- CRUD de **agendamentos** vinculados a uma empresa, com data e hora
- Exceções de domínio para recursos não encontrados
- CORS configurado para o front-end

## Endpoints

| Recurso | Rota base | Operações |
|---|---|---|
| Empresas | `/api/empresas` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |
| Usuários | `/api/usuarios` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |
| Agendamentos | `/api/agendamentos` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |

**Exemplo — criar agendamento**

```json
POST /api/agendamentos
{
  "empresa": { "id": 6 },
  "dataHora": "10-09-2023 16:00:00"
}
```

## Como executar

```bash
cd Findit
export DB_USERNAME=seu_usuario
export DB_PASSWORD=sua_senha
./mvnw spring-boot:run
```

A API sobe em `http://localhost:8080`.

## Equipe

| RM | Nome |
|---|---|
| 93451 | Felipe Cardenaz de Melo |
| 94489 | Raphael Rezende Silveira Junior |
| 94394 | Renan Castilho Costa |
| 92979 | Ricardo dos Santos Altavista |

---

Projeto acadêmico desenvolvido na **FIAP** (Challenge, 2023).
