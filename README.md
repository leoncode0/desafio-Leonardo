--Códigos estão abaixo do enunciado do desafio e foram feitos em JS--

# Desafio
Faça um programa que vai ler um numero do usuario, esse numero será o numero de linhas da saida

A saida será uma sequencia em zig zag de caracteres, onde ele vai pra direita 5 vezes, depois pra esquerda até o começo, e repetir. Por exemplo, suponha entrada 10, a saida seria

```
#
 #
  #
   #
    #
   #
  #
 #
#
```

Isso se repetirá infinitamente (teoricamente), pode usar o caracter que quiser e a linguagem que quiser:




# Codigo para web com input
```
//Versao do codigo para rodar na web com input

const linhas = parseInt(prompt ('Insira o numero desejado'))
let posicaoCaracter = 0
let sentido = 1    // 1 é positivo e -1 é negativo


let zigZag = () => {
    for (let i=1; i<linhas; i++){
        console.log(' '.repeat(posicaoCaracter)+'#')
        posicaoCaracter = posicaoCaracter + sentido;

        if (posicaoCaracter === 0 || posicaoCaracter === 4){
            sentido = sentido *(-1)
        }

}
}

console.log(zigZag())

```



# Codigo para leitor VSCode

```
//Versao para VSCode

let posicaoCaracter = 0
let sentido = 1    // 1 é positivo e -1 é negativo


let zigZag = (linhas) => {
    for (let i=1; i<linhas; i++){
        console.log(' '.repeat(posicaoCaracter)+'#')
        posicaoCaracter = posicaoCaracter + sentido;

        if (posicaoCaracter === 0 || posicaoCaracter === 4){
            sentido = sentido *(-1)
        }

}
}

console.log(zigZag(12))
```



