# API Java do Santander Dev Week
Java RESTful API criada para a Santander Dev Week construída em Java 17 com Spring Boot 3.


# Principais Tecnologia

- Java 17 : Utilizaremos a versão LTS mais recente do Java para tirar vantagem das inovações que essa linguagem robusta e amplamente utilizada oferece;

- Spring Boot 3 : Trabalharemos com a mais nova versão do Spring Boot, que maximiza a produtividade do desenvolvedor por meio de suas poderosas metas de autoconfiguração;

- Spring Data JPA : Exploraremos como essa ferramenta pode simplificar nossa camada de acesso aos dados, facilitando a integração com bancos de dados SQL;

- OpenAPI (Swagger) : Vamos criar uma documentação de API eficaz e fácil de entender usando OpenAPI (Swagger), perfeitamente alinhada com a alta produtividade que o Spring Boot oferece;

- Ferrovia : facilita a implantação e monitoramento de nossas soluções na nuvem, além de oferecer diversos bancos de dados como serviço e pipelines de CI/CD.

## [LINK DO FIGMA](https://www.figma.com/file/0ZsjwjsYlYd3timxqMWlbj/SANTANDER---Projeto-Web%2FMobile?type=design&node-id=1421-432&mode=design)

O Figma foi utilizado para a abstração do domínio desta API, sendo útil na análise e projeto da solução.

## Diagram de Classes

```mermaid
classDiagram
  class User {
    - name: String
    - account: Account
    - features: List<Feature>
    - card: Card
    - news: List<News>
  }

  class Account {
    - Number: String
    - Agency: String
    - balance: Double
    - limit: Double
  }

  class Feature {
    - icon: String
    - description: String
  }

  class Card {
    - number: String
    - limit: Double
  }

  class News {
    - icon: String
    - description: String
  }

  User "1" *-- "1"Account
  User "1" *-- "N"Feature
  User "1" *-- "1" Card
  User "1" *-- "N" News
```
