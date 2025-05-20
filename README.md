# 🎬 API de Filmes Filmados em San Francisco

Esta é uma API REST desenvolvida em **Java** com **Spring Boot**, utilizando **Spring WebFlux**, **Lombok**, **DevTools** e empacotada como um **JAR** via **Maven**. A API coleta informações de uma fonte externa sobre filmes que foram filmados na cidade de **San Francisco**.

## 🚀 Tecnologias Utilizadas

- Java 17+
- Spring Boot
- Spring Web
- Spring WebFlux
- Lombok
- Spring DevTools
- Maven

## 📦 Como Executar o Projeto

Certifique-se de ter o **Java 17+** e o **Maven** instalados.

```bash
git clone https://github.com/seuusuario/sanfrancisco-movies-api.git
cd spring.boot.desafio.uber
mvn clean install
java -jar target/spring.boot-desafio-uber-0.0.1-SNAPSHOT.jar
```


📌 Endpoints da API
GET /movies
Retorna a lista de filmes filmados em San Francisco. É possível filtrar pelo nome do filme usando o parâmetro title.

Exemplo de Requisição:

```
GET /movies?title=Vertigo
Exemplo de Resposta:

[
  {
    "title": "Vertigo",
    "releaseYear": "1958",
    "locations": "Alfred Hitchcock",
    "actor_1": "Golden Gate Bridge"
    "actor_2": "Golden Gate Bridge"
    "actor_3": "Golden Gate Bridge"
  }
]

```

GET /movies/autocomplete
Retorna a lista de filmes com um autocomplete baseado nas tres primeiras letras que o usuario informar
query: as iniciais do título do filme
Exemplo de Requisição:

```
GET /movies/autocomplete?query=Ver
Exemplo de Resposta:

[
  "Vertigo",
  "Veronika Decides to Die"
]
🔧 Configurações
```

### As configurações da API externa e portas estão definidas em src/main/resources/application.yml.

💡 Observações

- A API utiliza WebClient do Spring WebFlux para realizar chamadas assíncronas à API externa.
- Lombok é usado para reduzir boilerplate de código.
- Spring DevTools está incluído para facilitar o desenvolvimento com recarga automática.
