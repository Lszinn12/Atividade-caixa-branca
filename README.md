# Atividade-caixa-branca

## Descrição
O código foi desenvolvido na linguagem java, utilizando NetBeans IDE 16. O objetivo desse branch é análisar o código em função de um fluxo grafo.

## Código
![image](https://github.com/yVinii/CaixaBranca/assets/117307556/6f13fdfa-dd7c-49a7-a693-43e95713880e)

## Grafo de fluxo
![image](https://github.com/yVinii/CaixaBranca/assets/117307556/d334bc4c-352e-4082-b218-b941c3c9d122)

## Complexidade
Fazendo a conta para obter a complexidade teremos como resultado 2. Logo existem dois caminhos no código, e ambos precisam ser testados por completo.

## Possíveis fluxos
### Fluxo principal
![image](https://github.com/yVinii/CaixaBranca/assets/117307556/cf11f0ca-dfc7-4bf5-bf8a-ebd79d1f58ce)

### Fluxo de exceções
![image](https://github.com/yVinii/CaixaBranca/assets/117307556/891d77ba-fce1-4d2d-b421-5d269e1739dc)

## **Classe `User()`**

Dentro do código, há uma classe chamada `User()`, na qual é utilizada para autenticar o usuário e estebalecer uma conexão o banco de dados MySQL utilizado.

Como dito anteriormente, a classe `User()`, possui os seguintes métodos/variáveis:
- `conectarBD()`: Método que estabelece uma conexão efetiva com o banco de dados MySQL;
- `verificarUsuario(String login, String senha)`: Método que verifica as credenciais, ou seja, o login e a senha do usuário, consultando diretamente o banco de dados;
- `nome`: Variável que receberá como valor, o nome do usuário;
- `result`: Variável que receberá como valor, o resultado da autenticação, ou seja, terá como valores, **verdadeiro** para sucesso e **falso** para falha. 

### **Como usar:**

A classe `User()`, basicamente, pode ser usada para gerar uma conexão com o banco de dados MySQL, verificando o nome do usuário e a senha definida. Vejamos um exemplo a seguir:

```java
public static void main(String[] args) {
    User user = new User();
		
    System.out.println(user.conectarBD());
		
    String login = "admin";
    String senha = "123456";
		
    System.out.println(user.verificarUsuario(login, senha));
}
