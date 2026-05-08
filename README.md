# ArrayListJs
Tutorial prático sobre manipulação de coleções com listas em JavaScript utilizando os métodos map, filter e reduce.

## Manipulação de Arrays em JavaScript

### O que é um Array?

Um array é uma estrutura de dados utilizada para armazenar múltiplos valores em uma única variável.

#### Exemplo simples: 

  ```js
    const numeros = [10, 20, 30, 40, 50];
  ```

##  Método map()

### O que faz?

O método `map()` percorre todos os elementos do array e retorna um novo array transformado.

### Sintaxe

```js
array.map((item, indice, arrayOriginal) => {
    // transformação
    return elemento;
});
```

### Exemplo Prático:

```js
 const notas = [5, 7, 8, 10, 6];

 const notasAtualizadas = notas.map(nota => nota + 1);

 console.log(notasAtualizadas);
```

### Saída:

```js
  [6, 8, 9, 11, 7]
```
#### Explicação:

Nesse exemplo, o método `map()` percorre todas as notas do array e cria um novo array somando 1 ponto em cada nota.

## Método filter()

###  O que faz?

O método `filter()` cria um novo array contendo apenas os elementos que atendem a uma condição.

### Sintaxe

```js
  array.filter((elemento) => {
      // condição
  });
```

### Exemplo prático:

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

### Saída:

```js
  [
    { nome: 'Carlos', idade: 22 },
    { nome: 'Marina', idade: 19 }
  ]
```

#### Explicação:

* O método `filter()` percorre todos os elementos do array e retorna um novo array apenas com os itens que atendem à condição definida.

* No exemplo acima, o `filter()` verificou a idade de cada aluno e manteve somente aqueles com idade maior ou igual a 18.

* Os alunos menores de idade foram removidos do novo array.

## Método reduce()

### O que faz?

O método `reduce()` reduz todos os elementos do array para um único valor.

Ele é muito utilizado para:

* somar valores;
 
* calcular médias;

* agrupar dados;

* criar objetos;

* contabilizar informações.

### Sintaxe

```js
array.reduce((acumulador, elemento) => {
    return acumulador;
}, valorInicial);
```

### Exemplo Prático:

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

### Saída:

```js
5150
```

#### Explicação:

* O método `reduce()` percorre todos os elementos do array e reduz os dados para um único valor.

* No exemplo acima, o `reduce()` somou o valor de cada venda utilizando o acumulador.

* O valor inicial começou em 0 e, a cada repetição, o valor da venda foi adicionado ao total até obter o resultado final de 5150.

# Utilizando os métodos map(), filter() e reduce() em objetos.

Serão mostrados exemplos utilizando arrays de objetos.

## Método map() com Objetos.

Ele percorre cada objeto da lista e retorna uma nova estrutura de dados.

### Exemplo Prático:

```js
const alunos = [
    { nome: 'Lucas', nota: 7 },
    { nome: 'Fernanda', nota: 9 }
];

const resultado = alunos.map(aluno => {
    return {
        ...aluno,
        aprovado: aluno.nota >= 7
    };
});

console.log(resultado);
```

### Saída:

```js
[
  { nome: 'Lucas', nota: 7, aprovado: true },
  { nome: 'Fernanda', nota: 9, aprovado: true }
]
```

#### Explicação:

* Nesse exemplo, o `map()` adicionou uma nova propriedade chamada aprovado em cada objeto do array.

* Assim, foi criado um novo array contendo os dados atualizados dos alunos.

## Método filter() com Objetos

Ele verifica cada item do array e mantém apenas os elementos que satisfazem determinada regra.

### Exemplo Prático:

```js
const filmes = [
    { titulo: 'Vingadores', categoria: 'Ação' },
    { titulo: 'Toy Story', categoria: 'Animação' },
    { titulo: 'Batman', categoria: 'Ação' }
];

const filmesAcao = filmes.filter(filme => filme.categoria === 'Ação');

console.log(filmesAcao);
```

### Saída:

```js
[
  { titulo: 'Vingadores', categoria: 'Ação' },
  { titulo: 'Batman', categoria: 'Ação' }
]
```

#### Explicação:

* O `filter()` analisou a categoria de cada filme e retornou somente os filmes de ação.

* Os demais elementos foram ignorados no novo array.

## Método reduce() com Objetos

Ele executa uma operação acumulativa durante toda a passagem pelo array.

### Exemplo Prático:

```js
const estoque = [
    { produto: 'Notebook', quantidade: 3 },
    { produto: 'Mouse', quantidade: 10 },
    { produto: 'Teclado', quantidade: 5 }
];

const totalItens = estoque.reduce((total, item) => {
    return total + item.quantidade;
}, 0);

console.log(totalItens);
```

### Saída:

```js
18
```

#### Explicação:

* O `reduce()` percorreu todos os produtos do estoque e acumulou a quantidade de itens existentes.

* Ao final da execução, foi obtido o total geral de produtos armazenados.

# Conclusão:

Os métodos `map()`, `filter()` e `reduce()` são fundamentais para manipulação de arrays em JavaScript.

Cada um possui uma finalidade específica:

* `map()` - transforma os elementos de um array;
* `filter()` - seleciona elementos com base em condições;
* `reduce()` - reduz os dados para um único resultado.

Esses métodos tornam o código mais organizado, reutilizável e fácil de entender, além de seguirem conceitos da programação funcional, com eles, é possível manipular listas e objetos de forma mais eficiente, evitando estruturas complexas e deixando o desenvolvimento mais produtivo.





