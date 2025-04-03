# Atividade: Documentação de Código
### Aluno: Rhyan Pablo (3º DS B)



## Código em HTML para calcular fatorial e verificar se o número é primo





``` html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fatorial e Número Primo</title>
</head>

<body>
<h2>Calculadora de Fatorial e Verificador de Número Primo</h2>
<label for="numero">Digite um número:</label>
    <input type="number" id="numero">
    <button onclick="calcular()">Calcular</button>
        <p id="resultado"></p>
<script>
//Função do calculo do Fatorial
function calcularFatorial(n) {
    if (n === 0) {
    return 1;
}else {
    return n * calcularFatorial(n - 1);
}
}
//Função para verificar se o número é primo
function verificarNumeroPrimo(numero) {
    if (numero <= 1) {
    return false;
}
for (let i = 2; i < numero; i++) {
    if (numero % i === 0) {
    return false;
}
}

return true;
}
//função "Calcular" para chamar as funções com o escopo dado
function calcular() {
    let numero = parseInt(document.getElementById("numero").value);
    let fatorial = calcularFatorial(numero);
    let primo = verificarNumeroPrimo(numero);
    document.getElementById("resultado").innerHTML ="O fatorial de " + numero + " é " + fatorial + "<br>" + "O número " + numero + (primo ? " é primo." : " não é primo.");
}
</script>
</body>
</html>
```

1. O que mudou no código após a formatação e adição de comentários?

>Após as mudanças o código ficou na identação ideal da linguagem, e facilitou a compreensão do mesmo.


2. Como a rastreabilidade auxilia na compreensão e manutenção do código?

>Com a restreabilidade, fazer mudanças para no código se torna mais rápido tendo em vista que é fácil localizar as funções ou parte necessária do código.


3. Quais práticas você considera essenciais para garantir um código bem
documentado?

>Para um código bem documentado são necessários: Comentários, Identação, Escolher nomes autoexplicativos para as funções e variáveis etc.

4. Qual a importância do uso do Markdown na documentação do código?

>Ele ajuda a documentar a função principal de todo o código, assim, é possível saber o que o código fará antes mesmo de usar.

5. Como a padronização e boas práticas de projeto facilitam a manutenção e
escalabilidade de sistemas?

> Tornam o código mais modular e compreensível

