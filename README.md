![banner](https://i.postimg.cc/kgqnr1Z1/banner-desafio2-vnw.png)

<p align="center">
  <img alt="Repository size" src="https://img.shields.io/github/repo-size/hamomgs/calculation-utils" />
  
  <a href="https://github.com/hamomgs/calculation-utils/commits/main">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/hamomgs/calculation-utils" />
  </a>
  
  <img alt="License" src="https://img.shields.io/badge/license-MIT-brightgreen" />

  <a href="https://www.linkedin.com/in/hamomgs/">
    <img alt="Feito por Hamom Silva" src="https://img.shields.io/badge/feito-por%20Hamom%20Silva-2c938c">
  </a>
</p>

Desafio da escola [Vai na Web](https://www.linkedin.com/company/vainaweb/): Criar uma biblioteca (lib) em Java sem instanciar objetos, utilizando apenas a classe para realizar operações matemáticas diversas. O objetivo é empacotar o código realizado em um arquivo JAR para facilitar a reutilização.

## 📚 Sobre a Biblioteca

A biblioteca `CalculationUtils` oferece uma variedade de operações matemáticas básicas e avançadas em Java. Ela foi projetada para ser fácil de usar, permitindo que os usuários realizem cálculos sem a necessidade de instanciar objetos.

## 🌟 Desafios Encontrados

- Permitir que o usuário some, subtraia, multiplique e divida quantos números desejar.

  - Para lidar com a necessidade de permitir que o usuário realize operações com quantos números desejar, busquei pelas melhores práticas em Java. Com conhecimento prévio em JavaScript, pesquisei pela existência do recurso de parâmetros rest, que permite representar um número indefinido de argumentos como um array no parametro, no Java. Pesquisando, encontrei a solução utilizando parâmetros varargs (variadic arguments). Os parâmetros varargs também são usados para definir um parâmetro que pode receber um número indefinido de argumentos. Com o uso de um loop `for` e `for-each`, consegui iterar sobre os argumentos e realizar as operações desejadas.

    ```Java
      // Exemplo de uso:
      double soma = Calculadora.somar(1, 2, 3, 4, 5);
      System.out.println(soma); // Saída: 15
    ```

- Trazer um pouco mais de carinho e personalização para a biblioteca ao considerar erros simples e comuns ao fazer o cálculo de alguns métodos, como passar apenas um argumento para a divisão ou tentar dividir por zero.

  -  Para tornar a biblioteca mais amigável e evitar erros comuns, implementei verificações e mensagens descritivas de erro. Utilizei estruturas condicionais para identificar situações como passar apenas um argumento para a divisão (que requer no mínimo dois números) e tentar dividir por zero (que é indefinido). Além disso, lancei exceções com mensagens informativas para indicar claramente quando ocorre um erro.

      ```Java
        // Exemplo de uso:
        try {
          double divisao = Calculadora.dividir(10, 0, 2);
          System.out.println(divisao);
        } catch (IllegalArgumentException e | ArithmeticException e) {
          System.err.println("Erro: " + e.getMessage()); // Saída: Erro: Não é possível dividir por zero.
        }
      ```

## ⚙️ Funcionalidades Principais

A biblioteca inclui as seguintes funcionalidades:

### ➗ Operações Aritméticas Básicas

- Soma
- Subtração
- Multiplicação
- Divisão

### ⏹️ Operações Aritméticas Avançadas

- Potenciação
- Radiciação

### 🔄 Trigonometria

- Seno
- Cosseno
- Tangente

### 🔢 Logaritmos

- Logaritmo Natural
- Logaritmo na Base 10

### 📏 Cálculos de Área, Perímetro e Volume

- Área do Retângulo, Triângulo, etc.
- Perímetro do Retângulo, Triângulo, etc.
- Volume do Cubo, Pirâmide, etc.

### 💹 Cálculos de Juros

- Juros Simples
- Juros Compostos

## 🌐 Exemplos de Uso

Aqui estão alguns exemplos básicos de como usar a biblioteca:

```Java
import br.com.vainaweb.lib.Calculadora;

public class Main {
    public static void main(String[] args) {
        // Operações Básicas
        double soma = Calculadora.somar(1, 2, 3, 4, 5);
        System.out.println("Soma: " + soma); // Soma: 15.0

        // Potenciação
        double potencia = Calculadora.potencia(2, 3);
        System.out.println("Potência: " + potencia); // Potência: 8.0

        // Trigonometria
        double seno = Calculadora.seno(30);
        System.out.println("Seno: " + seno); // Seno: 0.49999999999999994
    }
}
```

Para mais detalhes e exemplos, consulte a [Documentação](https://hamomgs.notion.site/Home-6a8cec60c268489cacac84afe61c6b6d?pvs=4).

## 🎯 Possíveis Melhorias

- [ ] Implementar outras operações aritméticas.
- [ ] Refatorar e organizar métodos em diferentes classes. Exemplos de classes: Financas, CalculosGeometricos, OperacoesBasicas, etc.
- [ ] Adicionar mais validações de entrada e mensagens de erro.

## 🛠️ Tecnologias

| Tecnologia  | Versão |
| ------------- | ------- |
| [Java SE](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) | JDK 17.0.9 |

## 🧑‍🏫 Instrutor e Facilitador

<table>
  <tr>
    <td align="center"><a href="https://www.linkedin.com/in/samuel-silveriom/"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/103957897?v=4" width="100px;" alt=""/><br /><sub><b>Samuel Silvério</b></sub></a><br /><a href="https://github.com/Samuel-prata" title="Samuel Silvério">🧑‍🏫</a></td>
    <td align="center"><a href="https://www.linkedin.com/in/leno-rafael-85a2ab1ba/"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/73203800?v=4" width="100px;" alt=""/><br /><sub><b>Leno Rafael</b></sub></a><br /><a href="https://github.com/lenors" title="Leno Rafael">🧑‍🏫</a></td>
  </tr>
</table>

## 🤝  Como Contribuir

1. Faça um fork do projeto.
2. Crie uma nova branch com as suas alterações: `git checkout -b my-feature`
3. Salve as alterações e crie uma mensagem de commit contanto o que você fez: `git commit -m "feature: My new feature"`
4. Envie as alterações: `git push origin my-feature`

## 💚 Agradecimentos

> Referências, fontes, ferramentas e recursos utilizados não só na biblioteca, mas também na [Documentação](https://hamomgs.notion.site/Home-6a8cec60c268489cacac84afe61c6b6d?pvs=4) do desafio.

- [Documentação Classe Math](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html)
- [W3Schools](https://www.w3schools.com/java/default.asp)
- [Mundo Escola](https://mundoeducacao.uol.com.br/)
- [Brasil Escola](https://brasilescola.uol.com.br/)
- [Notion](https://notion.so)
- [Canva](https://www.canva.com/)
- [FlatIcon](https://www.flaticon.com/)

## 🧙‍♂️ Autor

<table>
  <tr>
    <td align="center">
      <a href="https://www.linkedin.com/in/hamomgs/">
        <img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/88857655?v=4" width="100px;" alt="" />
        <br />
        <sub><b>Hamom Silva</b></sub>
      </a>
      <br />
      <a href="https://github.com/hamomgs" title="Hamom Silva">👨‍💻</a>
    </td>
  </tr>
</table>

## 📃 Licença

Esse projeto esta sob a licença [MIT](https://github.com/hamomgs/calculation-utils/blob/main/LICENCE).