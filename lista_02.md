# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let p = 10;
let q = 3;
let r = 6;

let resultado = (p % q === 1) && (r * 2 > p) || (q + r < p);
console.log(resultado);

const valores = [3, 6, 9, 12, 15];
let produto = 1;

for (let j = 0; j < valores.length; j++) {
  produto *= valores[j];
}

console.log("O produto dos valores é:", produto);


```
Qual das seguintes alternativas melhor descreve o que o código faz?

**A) O código avalia a expressão booleana, imprime `true`, calcula o produto dos números na lista e imprime o resultado no console.**

B) O código avalia a expressão booleana, imprime `false`, calcula o produto dos números na lista e imprime o resultado no console.

C) O código avalia a expressão booleana, imprime `true` e, em seguida, verifica se o número 6 está na lista.

D) O código avalia a expressão booleana, imprime `false` e ordena os valores em ordem crescente.

Alternativa: **A**
______

**2)** O código a seguir contém duas funções que calculam o limite de crédito de um cliente com base nos seus gastos e na renda mensal.

```javascript
// Versão 1 da função de análise de crédito
function analisarCredito1() {
    var compras = [2500, 1200, 800, 100];
    var totalCompras = compras[0];
    var limite = 5000;
    var status = 'aprovado';
    var saldoDisponivel = 0;
    var i = 1;

    do {
        totalCompras += compras[i];
        i++;
    } while (limite >= totalCompras && i < compras.length);

    saldoDisponivel = limite - totalCompras;

    if (saldoDisponivel < 0) {
        status = 'negado';
    }
    console.log(`Seu crédito foi ${status}. Saldo disponível: ${saldoDisponivel}.`);
}
```

```javascript
// Versão 2 da função de análise de crédito
function analisarCredito2() {
    var compras = [2500, 1200, 800, 100];
    var totalCompras = compras[0];
    var limite = 5000;
    var status = 'aprovado';
    var saldoDisponivel = 0;
    var i = 1;

    while (limite >= totalCompras && i < compras.length) {
        totalCompras += compras[i];
        i++;
    }

    saldoDisponivel = limite - totalCompras;

    if (saldoDisponivel < 0) {
        status = 'negado';
    }
    console.log(`Seu crédito foi ${status}. Saldo disponível: ${saldoDisponivel}.`);
}
```
Se ambas as funções forem executadas com os valores fornecidos, qual será a saída exibida no console?

**A) Ambas as funções exibirão: 'Seu crédito foi aprovado. Saldo disponível: 400.'**

B) analisarCredito1() exibirá: 'Seu crédito foi negado. Saldo disponível: -600.', enquanto analisarCredito2() exibirá: 'Seu crédito foi negado. Saldo disponível: -200.'

C) analisarCredito1() exibirá: 'Seu crédito foi negado. Saldo disponível: -200.', enquanto analisarCredito2() exibirá: 'Seu crédito foi aprovado. Saldo disponível: 100.'

D) Ambas as funções exibirão: 'Seu crédito foi aprovado Saldo disponível: 500.'

Alternativa: **A**
______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const idade = 21;

if (idade >= 18 && idade < 60) {
  console.log("Você é um adulto!");
} else if (idade < 18) {
  console.log("Você é menor de idade!");
} else {
  console.log("Você está na melhor idade!");
}
```
Qual das seguintes alternativas melhor descreve o comportamento do código?

A) O código verifica se a idade indica um adulto ou um idoso e exibe a mensagem correspondente.

**B) O código verifica se a idade pertence à faixa adulta. Se for, exibe "Você é um adulto!". Caso contrário, verifica se é menor de idade e exibe "Você é menor de idade!". Se nenhuma das condições anteriores for verdadeira, exibe "Você está na melhor idade!".**

C) O código verifica se a idade está entre 18 e 60 anos e, se for, imprime "Você é um adulto!". Se não estiver nesse intervalo, imprime "Você está na melhor idade!".

D) O código verifica se a idade é menor de 18, entre 18 e 60 ou acima de 60, imprimindo uma mensagem específica para cada caso.

Alternativa: **B**
______

**4)** Qual será o resultado impresso no console após a execução do seguinte código?
```javascript
//EX04
var energiaDisponivel = 1200;
var bateriaExtra = 400;
var consumoDispositivos = [300, 600, 500, 200, 400];

for (var i = 0; i < consumoDispositivos.length; i++) {
    var consumo = consumoDispositivos[i];

    if (consumo <= energiaDisponivel) {
        console.log("Dispositivo " + (i+1) + " ligado. Energia restante: " + (energiaDisponivel - consumo));
        energiaDisponivel -= consumo;
    } else if (consumo <= energiaDisponivel + bateriaExtra) {
        console.log("Dispositivo " + (i+1) + " ligado com bateria extra. Energia restante: " + ((energiaDisponivel + bateriaExtra) - consumo));
        energiaDisponivel = 0;
        bateriaExtra -= (consumo - energiaDisponivel);
    } else {
        console.log("Dispositivo " + (i+1) + " não pode ser ligado. Energia insuficiente.");
    }
}
```

Escolha a opção que responde corretamente:

A)
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado com bateria extra. Energia restante: 700

Dispositivo 3 ligado. Energia restante: 200

Dispositivo 4 ligado com bateria extra. Energia restante: 0

Dispositivo 5 ligado. Energia restante: -200

B)
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado com bateria extra. Energia restante: 700

Dispositivo 3 ligado. Energia restante: 200

Dispositivo 4 não pode ser ligado. Energia insuficiente.

Dispositivo 5 não pode ser ligado. Energia insuficiente.

C)
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado com bateria extra. Energia restante: 700

Dispositivo 3 ligado. Energia restante: 400

Dispositivo 4 não pode ser ligado. Energia insuficiente.

**D)**
**Dispositivo 1 ligado. Energia restante: 900**

**Dispositivo 2 ligado. Energia restante: 300**

**Dispositivo 3 ligado com bateria extra. Energia restante: 200**

**Dispositivo 4 não pode ser ligado. Energia insuficiente.**

**Dispositivo 5 não pode ser ligado. Energia insuficiente.**

Alternativa: **D**
______

**5)** Qual é a principal função do método update() em um jogo desenvolvido com Phaser.js?

Escolha a opção que melhor descreve seu propósito:

A) O método update() é responsável por carregar os assets do jogo antes da cena ser exibida.

**B) O método update() é chamado continuamente a cada quadro (frame) do jogo, sendo usado para atualizar a lógica, movimentação e interações dos objetos na cena.**

C) O método update() renderiza todos os sprites na tela e garante que a física do jogo seja processada corretamente.

D) O método update() é chamado apenas uma vez após a criação da cena, sendo utilizado para configurar variáveis iniciais do jogo.

Alternativa: **B**
______

**6)** Qual é o principal objetivo do módulo Matter.js Physics em Phaser.js?

Escolha a opção que responde corretamente:

**A) Simular física avançada, incluindo corpos rígidos, colisões complexas e interação entre objetos com gravidade e forças.**

B) Gerenciar eventos de entrada do usuário, como cliques e toques na tela, permitindo movimentação de personagens.

C) Renderizar gráficos otimizados para jogos 2D e garantir uma taxa de quadros estável.

D) Criar animações automáticas para sprites e objetos interativos sem necessidade de programação de movimentação.

Alternativa: **A**
______

# Questões dissertativas

**7)** Uma loja online deseja implementar um sistema de classificação de pedidos com base no valor total da compra. O sistema deve determinar a categoria de um pedido com as seguintes regras:

```

Pedidos abaixo de R$50,00 → "Frete não disponível!"

Pedidos entre R$50,00 e R$199,99 (inclusive) → "Frete com custo adicional!"

Pedidos de R$200,00 ou mais → "Frete grátis!"
```
Implemente um pseudocódigo que receba o valor total da compra e exiba a classificação correta do frete para o cliente.

```
// Entradas do usuário
Escreva("Digite o valor total da compra: ")
valorTotal = Resposta do usuário

// Classificação do frete
Se valorTotal < 50.00 então:
    Escreva("Frete não disponível!")

Senão Se 50.00 < valorTotal < 199.00 então: 
    Escreva("Frete com custo adicional!")

Senão Se valorTotal >= 200.00 então:
    Escreva("Frete grátis!")
// Fim

```
______

**8)** Considere a implementação da classe base Veiculo em um sistema de modelagem de veículos. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Carro e Moto, que herdam da classe Veiculo, adicionando atributos específicos e métodos para calcular o consumo de combustível de um carro e de uma moto, respectivamente.

```
Classe Veiculo:
Atributos:

modelo
ano
Método Construtor(modelo, ano):

Define os valores dos atributos modelo e ano com os valores passados como parâmetro.
Método CalcularConsumo():
```
Implementação genérica para cálculo de consumo, a ser sobrescrita pelas subclasses.
Agora, implemente as classes Carro e Moto, garantindo que ambas herdem de Veiculo e possuam métodos específicos para calcular o consumo de combustível com base na quilometragem e eficiência do veículo.


```
Classe Veiculo:
    Atributos:
        modelo: Texto
        ano: Número Inteiro
    
    Construtor(modelo: Texto, ano: Número Inteiro):
        this.modelo = modelo
        this.ano = ano
    
    Método CalcularConsumo():
        // Método genérico a ser sobrescrito
        Retornar 0

Classe Carro herda Veiculo:
    Atributos:
        eficienciaCarro: Número Real  // km/l
        cilindradas: Inteiro
    
    Construtor(modelo: Texto, ano: Número Inteiro, eficienciaCarro: Número Real, cilindradas: Número Inteiro):
        super.Construtor(modelo, ano)  // Chama construtor da classe pai
        this.eficienciaCarro = eficienciaCarro
        this.cilindradas = cilindradas
    
    Método CalcularConsumo(quilometragem: Real): Número Real
        // Calcula litros necessários para percorrer a distância
        consumo = quilometragem / eficienciaCarro
        Retornar consumo

Classe Moto herda Veiculo:
    Atributos:
        eficienciaMoto: Real  // km/l
        possuiPartidaEletrica: Booleano
    
    Construtor(modelo: Texto, ano: Número Inteiro, eficienciaMoto: Número Real, partidaEletrica: Booleano):
        super.Construtor(modelo, ano)  // Chama construtor da classe pai
        this.eficienciaMoto = eficienciaMoto
        this.possuiPartidaEletrica = partidaEletrica
    
    Método CalcularConsumo(quilometragem: Real): Número Real
        // Calcula litros necessários para percorrer a distância
        consumo = quilometragem / eficienciaMoto
        
        // Moto com partida elétrica tem 5% melhor eficiência
        Se possuiPartidaEletrica então
            consumo = consumo * 0.95
        
        Retornar consumo

// Criando instâncias
meuCarro = novo Carro("Sedan", 2022, 12.5, 1600)
minhaMoto = novo Moto("Esportiva", 2023, 30.0, verdadeiro)

// Calculando consumos
consumoCarro = meuCarro.CalcularConsumo(300)  // 300km
consumoMoto = minhaMoto.CalcularConsumo(300)  // 300km

// Exibindo resultados
Escreva("Consumo do carro: " + consumoCarro + " litros")
Escreva("Consumo da moto: " + consumoMoto + " litros")

```

______

**9)** Você é um cientista da NASA e está ajudando no desenvolvimento de um sistema de pouso para sondas espaciais em Marte. Seu objetivo é calcular o tempo necessário para que a sonda reduza sua velocidade até um nível seguro para pouso, considerando uma velocidade inicial de entrada na atmosfera marciana e uma taxa de desaceleração constante causada pelo atrito atmosférico e retrofoguetes.

Entretanto, a sonda não pode ultrapassar um tempo máximo de descida para evitar desvios orbitais, nem pode desacelerar além de um limite mínimo, pois isso poderia causar instabilidade no pouso.

Implemente a lógica dessa simulação em pseudocódigo, considerando a seguinte equação para atualização da velocidade:

Considere a fórumla de atualização velocidade:
```
    velocidade = velocidadeInicial - desaceleracao * tempo
```
Seu programa deve determinar quanto tempo será necessário para que a sonda atinja uma velocidade segura de pouso, sem ultrapassar os limites estabelecidos.

```
Algoritmo CalculoTempoPousoMarte
    // Constantes do sistema
    Constante VELOCIDADE_SEGURA = 5.0          // em km/s
    Constante TEMPO_MAXIMO = 300.0             // em segundos
    Constante DESACELERACAO_MINIMA = 0.3       // em km/s²
    Constante DESACELERACAO_MAXIMA = 1.5       // em km/s²

    // Variáveis de entrada
    velocidadeInicial: Número Real
    desaceleracao: Número Real

    // Variáveis de cálculo
    tempoPouso: Número Real
    velocidadeFinal: Número Real

    // Entrada de dados
    Escreva("Digite a velocidade inicial de entrada (km/s): ")
    Leia(velocidadeInicial)

    Escreva("Digite a taxa de desaceleração (entre ", DESACELERACAO_MINIMA, " e ", DESACELERACAO_MAXIMA, " km/s²): ")
    Leia(desaceleracao)

    // Validação da desaceleração
    Se desaceleracao < DESACELERACAO_MINIMA OU desaceleracao > DESACELERACAO_MAXIMA Então
        Escreva("ERRO: Desaceleração fora dos limites permitidos!")
        Interrompa
    Fim Se

    // Cálculo do tempo necessário
    tempoPouso = (velocidadeInicial - VELOCIDADE_SEGURA) / desaceleracao

    // Verificação dos limites
    Se tempoPouso > TEMPO_MAXIMO Então
        Escreva("ALERTA: Tempo de pouso (", tempoPouso, "s) excede o máximo permitido!")
        Escreva("A sonda pode sofrer desvios orbitais.")
    Senão
        // Cálculo da velocidade final
        velocidadeFinal = velocidadeInicial - (desaceleracao * tempoPouso)

        // Verificação de velocidade segura
        Se velocidadeFinal <= VELOCIDADE_SEGURA Então
            Escreva("SUCESSO: Tempo de pouso calculado = ", tempoPouso, " segundos")
            Escreva("Velocidade final = ", velocidadeFinal, " km/s (nível seguro)")
        Senão
            Escreva("FALHA CRÍTICA: Sistema não conseguiu reduzir para velocidade segura!")
        Fim Se
    Fim Se
Fim Algoritmo
```
______

**10)** Em um sistema de análise financeira, as operações de investimento de uma empresa podem ser representadas por matrizes, onde cada linha representa um tipo de investimento e cada coluna representa um período de tempo.

A seguir, é fornecida a implementação da função SomarMatrizesInvestimento(matrizA, matrizB), que soma os valores de duas matrizes de investimento. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação das matrizes de investimento, determinando como os investimentos afetam os resultados ao longo do tempo.

```
Função SomarMatrizesInvestimento(matrizA, matrizB):  
    # Verifica se as matrizes têm o mesmo número de linhas e colunas  
    Se tamanho(matrizA) ≠ tamanho(matrizB) então:  
        Retornar "As matrizes não podem ser somadas. Elas têm dimensões diferentes."  
    Senão:  
        linhas <- tamanho(matrizA)  
        colunas <- tamanho(matrizA[0])  
        matrizResultado <- novaMatriz(linhas, colunas)  

        # Loop para percorrer cada elemento das matrizes e calcular a soma  
        Para i de 0 até linhas-1 faça:  
            Para j de 0 até colunas-1 faça:  
                matrizResultado[i][j] <- matrizA[i][j] + matrizB[i][j]  

        Retornar matrizResultado  

# Exemplo de uso da função  
investimentosAno1 <- [[1000, 2000], [1500, 2500]]  
investimentosAno2 <- [[1200, 1800], [1300, 2700]]  

totalInvestimentos <- SomarMatrizesInvestimento(investimentosAno1, investimentosAno2)  
Escrever("Total de investimentos acumulados:")  
ImprimirMatriz(totalInvestimentos)  
```
Agora, implemente a função MultiplicarMatrizesInvestimento(matrizA, matrizB), que multiplica as duas matrizes, simulando o efeito de diferentes fatores de crescimento e impacto financeiro nos investimentos ao longo do tempo.

```javascript
function multiplicarMatrizesInvestimento(matrizA, matrizB) {
    // Verifica se o número de colunas de A é igual ao número de linhas de B
    if (matrizA[0].length !== matrizB.length) {
        return "As matrizes não podem ser multiplicadas. Número de colunas de A difere do número de linhas de B."; 
    }

    const linhasA = matrizA.length;
    const colunasA = matrizA[0].length;
    const colunasB = matrizB[0].length;
    const matrizResultado = new Array(linhasA);

    // Calcula cada elemento da matriz resultado
    for (let i = 0; i < linhasA; i++) {
        matrizResultado[i] = new Array(colunasB);
        for (let j = 0; j < colunasB; j++) {
            let somaProdutos = 0;
            // Calcula o produto escalar da linha i de A com a coluna j de B
            for (let k = 0; k < colunasA; k++) {
                somaProdutos += matrizA[i][k] * matrizB[k][j];
            }
            matrizResultado[i][j] = somaProdutos;
        }
    }

    return matrizResultado;
}

// Imprime matrizes
function imprimirMatriz(matriz) {
    for (let i = 0; i < matriz.length; i++) {
        console.log(matriz[i].join(" "));
    }
}

// Exemplo de uso da função
const fatoresCrescimento = [[1.2, 0.8], [0.9, 1.1]];  // Matriz de fatores de crescimento
const investimentosIniciais = [[1000, 2000], [1500, 2500]];  // Matriz de investimentos

const investimentosProjetados = multiplicarMatrizesInvestimento(investimentosIniciais, fatoresCrescimento);
console.log("Projeção de investimentos após aplicação dos fatores de crescimento:");
imprimirMatriz(investimentosProjetados);
```
