
Lista 01 de Exercícios de JavaScript
Professor: Sérgio Monteiro, D.Sc.
1. Cálculo de Média:
 Escreva um programa que receba três notas de um aluno e calcule a média. Se a média for maior ou
igual a 7, exiba "Aprovado", caso contrário, exiba "Reprovado".

const nota1 = parseFloat(prompt("Digite a primeira nota: "))
const nota2 =parseFloat (prompt("Digite a segunda nota: "))
const nota3 = parseFloat(prompt("Digite a terceira nota: "))
const media = (nota1 + nota2 + nota3) / 3
if (media >=7){
    alert("Aprovado")
}else{
    alert("Reprovado")
}



2. Verificador de Número Par ou Ímpar:
 Escreva uma função que receba um número como entrada e determine se é par ou ímpar. Exiba uma
mensagem indicando o resultado.

const n = parseFloat(prompt("Digite um número: "))
if (n%2===0){
    alert("O número é par");
}else{
 alert(" O número é impar");
}




3. Calculadora de Fatorial:
 Crie uma função que receba um número como entrada e calcule o fatorial desse número. Utilize um
loop para realizar os cálculos.

let num = parseInt(prompt("Digite um número: "))
let fatorial = 1
for(let i = 1; i <= num; i++){
   fatorial *= i
}
alert("O fatoria de " + num + " é " + fatorial)



4. Verificador de Ano Bissexto:
 Escreva um programa que verifique se um ano fornecido pelo usuário é bissexto ou não. Um ano é
bissexto se for divisível por 4, exceto os anos que são divisíveis por 100, a menos que sejam divisíveis
por 400.

var ano = parseFloat(prompt("Digite o ano: "))
if ((ano % 4 === 0 && ano % 100!==0)||( ano %400 === 0)){
   alert("Bissexto")
}else{
   alert("Não bissexto")
}



5. Contador de Vogais:
 Escreva uma função que receba uma string como entrada e conte o número de vogais (a, e, i, o, u) na
string. Exiba o resultado.

    var palavra = prompt("Digite uma palavra:");
    var contador = 0
    for (var i = 0; i < palavra.length; i++) {
        if ('aeiou'.includes(palavra[i])) {
            contador++
        }
    }
    alert("Número de vogais: " + contador)





6. Calculadora de IMC:
 Crie um programa que calcule o Índice de Massa Corporal (IMC) de uma pessoa. O IMC é calculado
pela fórmula: peso / (altura altura). Exiba uma mensagem indicando se a pessoa está abaixo do peso,
com peso normal, com sobrepeso ou obesa, de acordo com a tabela de classificação do IMC.

let peso = parseFloat(prompt ("Digite seu  peso (kg)":))
let altura = parseFloat(prompt("Digite sua altura: "))
let imc = peso/(altura*altura)
let indicador 
if (imc < 18.5){
   alert ("Abaixo peso ")
}else if (imc >= 18.5 && imc < 24.9){
   alert ("Peso normal ")
}else if (imc >= 25 && imc < 29.9){
   alert ("Sobrepeso")
}else{
   alert("Obesidade ")
}


7. Conversor de Temperatura:
 Escreva um programa que converta uma temperatura de Celsius para Fahrenheit ou vice-versa.
Permita que o usuário escolha qual conversão deseja fazer e exiba o resultado.

var opcao = prompt("Digite 1 para conventer de Celsius para Fahrenheit ou digite 2 para converter de Fahrenheit para Celsius:")
if (opcao === "1"){
   var cels = parseFloat(prompt("Digite a temperatura em Celsius: "))
   var fahr = (cels * 9/5) + 32
   alert(cels + "°C é igual a " + fahr.toFixed(2) + "°F")
}else if (opcao === "2"){
var fahr = parseFloat(prompt("Digite a temperatura em Fahrenheit: "))
var cels = (fahr - 32) * 5/9
 alert(fahr + "°F é igual a " + cels.toFixed(2) + "°C")
}




8. Simulador de Jogo de Dados:
 Crie um programa que simule um jogo de dados. O usuário deve jogar um dado duas vezes e o
programa deve somar os resultados. Se a soma for igual a 7 ou 11, exiba "Você ganhou!", caso contrário,
exiba "Você perdeu!".

function jogarDados() {
    
    function lancarDado() {
        return Math.floor(Math.random() * 6) + 1;
    }
    var dado1 = lancarDado();
    var dado2 = lancarDado();

    var soma = dado1 + dado2;
    alert("Você tirou " + dado1 + " no primeiro dado e " + dado2 + " no segundo dado.");

    if (soma === 7 || soma === 11) {
        alert("Soma: " + soma + ". Você ganhou!");
    } else {
        alert("Soma: " + soma + ". Você perdeu!");
    }
}

jogarDados();






9. Lista de Tarefas:
 Implemente um programa que permita ao usuário adicionar, remover e listar tarefas. Utilize um objeto
para representar cada tarefa, contendo um identificador único e uma descrição.





  

10. Calculadora de Juros Compostos:
Escreva um programa que calcule o montante final de um investimento com juros compostos. O
programa deve receber o principal (valor inicial), a taxa de juros anual e o número de anos de
investimento. Use a fórmula:
𝑀 = 𝑃(1 + 𝑟)
𝑛
onde M é o montante final, P é o principal, r é a taxa de juros anual e n é o número de anos.

    let P = parseFloat(prompt("Digite o valor inicial (principal):"));
    let r = parseFloat(prompt("Digite a taxa de juros anual (%):")) / 100;
    let n = parseInt(prompt("Digite o número de anos:"));

    let M = P * (1 + r) ** n; 

    alert(`O montante final após ${n} anos é: R$ ${M.toFixed(2)}`);
