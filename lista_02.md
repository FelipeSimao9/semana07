# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina! (E não se envolva em plágio!)
- ao final, publique seu arquivo lista_02.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let x = 17
let y = 5
let z = 8

resultadoBooleano =  (x < y) && (z > x) || (x - y > z)
console.log(resultadoBooleano)

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);

```
Qual das seguintes alternativas melhor descreve o que o código faz?

B) O código avalia a expressão booleana, imprime o resultado `true`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

______

**2)** Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [3600, 950, 620, 38] em ambas funções.

```javascript
//Versão 1 da função que calcula orçamento
function calculaOrcamento(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var saldo = 0; 
    var statusSaldo =  'positivo';
    var i = 1;

    do{
        totalGastos += gastos[i];
        i++;
    } while(salario >= totalGastos && i<gastos.length)
    
    saldo = salario - totalGastos;

    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

```javascript
//Versão 2 da função que calcula orçamento
function calculaOrcamento2(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var statusSaldo =  'positivo';
    var saldo = 0;
    var i = 1;

    while(salario >= totalGastos && i<gastos.length){
        totalGastos += gastos[i];
        i++;
    }

    saldo = salario - totalGastos;
    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

D) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -100.'

______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
```

 Qual das seguintes alternativas é a descrição mais precisa do que o código faz?

D) O código verifica se o número é par, ímpar ou divisível por 3. Se for par, exibe a mensagem "O número é par!". Se for ímpar, exibe a mensagem "O número é ímpar!". Se for divisível por 3, exibe a mensagem "O número é divisível por 3!".


______

**4)** Qual será o resultado impresso no console após a execução desse código?
```javascript
//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
    var valorCompra = valorCompras[i];

    if (valorCompra <= saldo) {
        console.log("Compra " + (i+1) + " aprovada. Saldo restante: " + (saldo - valorCompra));
        saldo -= valorCompra;
    } else if (valorCompra <= saldo + limiteCredito) {
        console.log("Compra " + (i+1) + " aprovada com limite de crédito. Saldo restante: " + ((saldo + limiteCredito) - valorCompra));
        saldo = 0;
        limiteCredito -= (valorCompra - saldo);
    } else {
        console.log("Compra " + (i+1) + " negada. Saldo insuficiente e limite de crédito excedido.");
    }
}
```

Escolha a opção que responde corretamente:

B)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 aprovada com limite de crédito. Saldo restante: 0

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.

______

**5)** Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

B) Preload -> Create -> Update

______

**6)** Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

B) Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.

______

# Questões dissertativas

**7)** Implemente o pseudocódigo para o algoritmo representado no fluxograma da imagem.
![Uma imagem](assets/image.png)

inicio

//pega a idade do usuario
int idade = prompt("Insira sua idade")

//propoe uma condicao se a idade for menor de 16
IF (idade < 16) {
    entao imprima "nao pode votar!"
        //se a pessoa nao for menor de 16, cria uma nova condicao que distribui 2 grupos, maior de 18 ou menor de 18
        IF ELSE (idade >=16 e <18)
            entao imprima "voto facultativo!"
            senao imprima "voto obrigatorio!"
}

fimalgoritmo
______

**8)** Considere a implementação da classe base FormaGeometrica em um sistema de modelagem de formas geométricas. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Retangulo e Circulo, que herdam da classe FormaGeometrica, adicionando atributos específicos e métodos para calcular a área de um retângulo e de um círculo, respectivamente.

```
Classe FormaGeometrica:
    Atributos:
        - cor
 
    Método Construtor(cor):
        Define o valor do atributo cor com o valor passado como parâmetro.

    Método CalcularArea():
        # Implementação genérica para cálculo de área, a ser sobrescrita pelas subclasses.

Classe Retangulo (herda de FormaGeometrica):
    atributos:
        - comprimento
        - largura

    metodo construtor(cor, comprimento, largura):
        Chama o construtor da classe base para definir a cor e inicializa os atributos comprimento e largura.

    metodo CalcularArea():
        Retorna o valor da área do retângulo, calculado como comprimento * largura.

classe circulo (herda de FormaGeometrica):
    Atributos:
        - raio

    metodo construtor(cor, raio):
        Chama o construtor da classe base para definir a cor e inicializa o atributo raio.

    metodo CalcularArea():
        Retorna o valor da area do circulo, calculado como π * raio^2.


```

______

**9)** Você foi contratado(a) como estagiário(a) da Tesla e está participando do desenvolvimento de um programa para simular o desempenho de um carro elétrico em uma corrida. Seu objetivo é determinar em quantos minutos o carro levará para completar uma determinada distância, levando em consideração uma velocidade inicial e uma taxa de aceleração constante. No entanto, você deseja garantir que o carro não exceda uma velocidade máxima nem que a corrida demore mais do que um tempo máximo. Implemente a lógica dessa simulação em pseudocódigo.

// define as variaveis
velocidade_inicial // Velocidade inicial do carro (m/s)
taxa_aceleracao // Taxa de aceleracao do carro (m/s^2)
velocidade_maxima // Velocidade maxima permitida (m/s)
tempo_maximo // Tempo maximo para completar a corrida (s)
distancia_corrida // Distancia a ser percorrida na corrida (m)

// calcula o tempo necessario para acabar a corrida
tempo_necessario = (velocidade_maxima - velocidade_inicial) / taxa_aceleracao
tempo_necessario = max(tempo_necessario, 0) // Garante que o tempo necessario seja nao negativo

// verifica se o tempo necessario e menor ou igual ao tempo maximo
se (tempo_necessario <= tempo_maximo) {
    imprimir("O carro completara a corrida em menos de ", tempo_maximo, " segundos.")
} senao {
    imprimir("O carro nao conseguira completar a corrida dentro do tempo maximo.")
}



______

**10)** Uma matriz é uma coleção bidimensional de elementos, organizados em linhas e colunas. A seguir, é fornecida a implementação da função SomaDeMatrizes(matrizA, matrizB), que calcula a soma de duas matrizes. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação de duas matrizes.

```
Função MultiplicacaoDeMatrizes(matrizA, matrizB):
    # Verifica se o número de colunas da matrizA é igual ao número de linhas da matrizB
    Se tamanho(matrizA[0]) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser multiplicadas. Número de colunas de matrizA não é igual ao número de linhas de matrizB."
    Senão:
        linhasA <- tamanho(matrizA)
        colunasA <- tamanho(matrizA[0]) # Número de colunas de matrizA
        colunasB <- tamanho(matrizB[0]) # Número de colunas de matrizB
        matrizResultado <- novaMatriz(linhasA, colunasB)

        # Loop para percorrer cada elemento das matrizes e calcular a multiplicação
        Para i de 0 até linhasA-1 faça:
            Para j de 0 até colunasB-1 faça:
                soma <- 0
                Para k de 0 até colunasA-1 faça:
                    soma <- soma + matrizA[i][k] * matrizB[k][j]
                matrizResultado[i][j] <- soma

        Retornar matrizResultado

# Exemplo de uso da função
matrizA <- [[1, 2], [3, 4]]
matrizB <- [[5, 6], [7, 8]]

matrizMultiplicacao <- MultiplicacaoDeMatrizes(matrizA, matrizB)
Escrever("Produto das matrizes:")
ImprimirMatriz(matrizMultiplicacao)

```
