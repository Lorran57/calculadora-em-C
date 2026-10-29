# calculadora-em-C
Calculadora simples utilizando C

#include <stdio.h>
int main(){
float num1, num2, resultado;// variáveis para os números e o resultado 
    int opcao;      //opção escolhida pelo usuario
    // Entrada de dados
    printf("Digite o primeiro nome: ");
    scanf("%f", &num1);
    printf("Digite o segundo nome: ");
    scanf("%f", &num2);
    // Menu de Operações
    printf("\nEscolha uma operacao:\n");
    printf("1 - Adicao\n");
    printf("2 - Subtracao\n");
    printf("3 - Multiplicacao\n");
    printf("4 - Divisão\n");
    printf("opcao: ");
    scanf("%d", &opcao);
    // Estrutura switch/case para decidir a operação
    switch (opcao) {
        case 1: 
        resultado = num1 + num2;
    printf("\nResultado: %.2f + %.2f = %.2f\n", num1, num2, resultado);
            break;
        case 2:
            resultado = num1 - num2;
    printf("\nResultado: %.2f - %.2f = %.2f\n", num1, num2, resultado);
            break;
        case 3:
            resultado = num1 * num2;
    printf("\nResultado: %.2f * %.2f = %.2f\n", num1, num2, resultado);
            break;
        case 4:
            if (num2 != 0) {// verifica Divisão por zero
                resultado = num1 / num2;
    printf("\nResultado: %.2f / %.2f = %.2f\n", num1, num2, resultado);
            } else {
                printf("\nErro: Divisão por zero nao permitida. \n");
            }
            break;
        default:
            printf("\nOpcao invalida. tente novamente. \n");
            break; 
        }
}
