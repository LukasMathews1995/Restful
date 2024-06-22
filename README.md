Santander dev week 2024

## Diagrama de Classes

````mermaid
classDiagram
  class User {
    <<DTO>>
    - string name
    - Account account
    - Feature features
    - CreditCard card
    - News news
    + getters/setters
  }

  class Account {
    <<DTO>>
    - string Number
    - string Agency
    - float Balance
    - float Limit
    + getters/setters
  }

  class Feature {
    <<DTO>>
    - string Icon
    - string Description
    + getters/setters
  }

  class CreditCard {
    <<DTO>>
    - string Number
    - float Limit
    + getters/setters
  }

  class News {
    <<DTO>>
    - string Icon
    - string Description
    + getters/setters
  }

  User "1" *-- "1" Account 
  User "1" *-- "N" Feature 
  User "1" *-- "1" CreditCard 
  User "1" *-- "N" News 
```
