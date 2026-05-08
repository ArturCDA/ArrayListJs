# ArrayListJs
Tutorial prático sobre manipulação de coleções com listas em JavaScript utilizando os métodos map, filter e reduce.

## Manipulação de Arrays em JavaScript

🔹 ### O que é um Array?

Um array é uma estrutura de dados utilizada para armazenar múltiplos valores em uma única variável.

🔥Exemplo simples: 
  ```js
    const numeros = [10, 20, 30, 40, 50];
  ```

 🔹##  Método map()

✅  ### O que faz?

O método `map()` percorre todos os elementos do array e retorna um novo array transformado.

📌 ### Sintaxe

```js
array.map((item, indice, arrayOriginal) => {
    // transformação
    return elemento;
});
```

💻 ### Exemplo Prático:

```js
 const notas = [5, 7, 8, 10, 6];

 const notasAtualizadas = notas.map(nota => nota + 1);

 console.log(notasAtualizadas);
```

🖥️ ### Saída:
```js
  [6, 8, 9, 11, 7]
```
📚 #### Explicação:

Nesse exemplo, o método `map()` percorre todas as notas do array e cria um novo array somando 1 ponto em cada nota.

🔹## Método filter()

✅###  O que faz?

O método `filter()` cria um novo array contendo apenas os elementos que atendem a uma condição.

📌### Sintaxe

```js
  array.filter((elemento) => {
      // condição
  });
```

💻### Exemplo prático:

```js
  const alunos = [
      { nome: 'Ana', idade: 17 },
      { nome: 'Carlos', idade: 22 },
      { nome: 'Marina', idade: 19 },
      { nome: 'Pedro', idade: 15 }
  ];
  
  const maioresDeIdade = alunos.filter(aluno => aluno.idade >= 18);
  
  console.log(maioresDeIdade);
```

🖥️### Saída:
```js
  [
    { nome: 'Carlos', idade: 22 },
    { nome: 'Marina', idade: 19 }
  ]
```

📚#### Explicação:

*O método `filter()` percorre todos os elementos do array e retorna um novo array apenas com os itens que atendem à condição definida.

*No exemplo acima, o `filter()` verificou a idade de cada aluno e manteve somente aqueles com idade maior ou igual a 18.

*Os alunos menores de idade foram removidos do novo array.

🔹## Método reduce()

✅### O que faz?

O método `reduce()` reduz todos os elementos do array para um único valor.

Ele é muito utilizado para:

*somar valores;
*calcular médias;
*agrupar dados;
*criar objetos;
*contabilizar informações.

📌### Sintaxe

```js
array.reduce((acumulador, elemento) => {
    return acumulador;
}, valorInicial);
```

💻### Exemplo Prático:

```js
const vendas = [
    { produto: 'Notebook', valor: 3500 },
    { produto: 'Mouse', valor: 150 },
    { produto: 'Teclado', valor: 300 },
    { produto: 'Monitor', valor: 1200 }
];

const totalVendas = vendas.reduce((acumulador, venda) => {
    return acumulador + venda.valor;
}, 0);

console.log(totalVendas);
```

🖥️### Saída:

```js
5150
```

📚#### Explicação:

*O método `reduce()` percorre todos os elementos do array e reduz os dados para um único valor.

*No exemplo acima, o `reduce()` somou o valor de cada venda utilizando o acumulador.

*O valor inicial começou em 0 e, a cada repetição, o valor da venda foi adicionado ao total até obter o resultado final de 5150.

*O valor inicial começou em 0 e, a cada repetição, o valor da venda foi adicionado ao total até obter o resultado final de 5150.
