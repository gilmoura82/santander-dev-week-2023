# Santander Dev Week 2023
Java Restful API criada para a Santander Dev Week

## Diagrama de Classes

``` mermaid
classDiagram
    class Usuario {
        - nome: String
        - conta: Conta
        - features: Feature[]
        - cartao: Cartao
        - news: News[]
    }

    class Conta {
        - numero: String
        - agencia: String
        - saldo: Number
        - limite: Number
    }

    class Feature {
        - Icon: String
        - descricao: String
    }

    class Cartao {
        - numCartao: String
        - limiteCartao: Number
    }

    class News {
        - newsIcon: String
        - newsDescricao: String
    }

    Usuario "1" *--> "1" Conta
    Usuario "1" *--> "1..N" Feature
    Usuario "1" *--> "1" Cartao
    Usuario "1" *--> "N" News

```
