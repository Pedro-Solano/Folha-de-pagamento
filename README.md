# Simulação de uma folha de pagamento.

Projeto da disciplina Programação e Desenvolvimendo de Software 2, do curso de bacheraldo em Sistemas da Informação da Universidade Federal de Minas Gerais - UFMG.

## Objetivo

O exercício utiliza uma hierarquia de herança contendo tipos de empregados em um aplicativo que simula a folha de pagamento de uma empresa. 

## Implementação

Na hierarquia, cada empregado tem uma função "salario" para calcular o salário semanal do empregado, funções essa que variam conforme o tipo de empregado. EmpregadoSalariado, por exemplo, recebe um salário fixo independentemente do número de horas trabalhadas, enquanto EmpregadoPorHora é pago por hora e tambem recebe o pagamento de horas extras. A classe EmpregadoComissionado é utilizada para representar os empregados que recebem uma porcentagem de suas vendas. A classe EmpregadoComissionadoBase é utilizada para representar empregados que recebem um salário-base mais uma porcentagem de duas vendas.

A classe abstrata Empregado fornece as funções "salario" e "imprime", além das várias funções get e set que manipulam membros de dados da classe. A função-membro "salario" é declarada como virtual pura, uma vez que cada tipo de funcionário tem sua forma específica de pagamento. Um funcionário possui um nome, sobrenome, o número do cpf, e sua data de nascimento. É utilizado uma classe Data para representar a data de nascimento de um funcionário. 

No main é simulado o processamento da folha de pagamento. Cria-se um vector de ponteiros Empregado para armazenar os funcionários. No loop, calcula-se a folha de pagamento para cada Empregado de forma polimórfica e adiciona-se um bônus de 100 reais ao pagamento do funcionário, caso seja seu mês de aniversário. Além disso, é fornecido um aumento de 10% ao salário dos funcionários EmpregadoComissionadoBase.

## Saída
A saída do programa é impressa na tela e mostra os atributos de cada funcionário, bem como o salário recebido no mês.

## Compilação:
Deve ser utilizado o comando "make" na linha de comando dentro da pasta onde está armezado o arquivo makefile e os demais arquivos de código. Esse comando irá gerar o executável "pagamento".
