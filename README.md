1 

    #include <stdio.h>
    int main() {
    int numero;

        printf("Digite um número inteiro: ");
    scanf("%d", &numero);

    if (numero % 2 == 0) {
        printf("O número %d é par.\n", numero);
    } else {
        printf("O número %d é ímpar.\n", numero);
    }

    return 0;
}




2

    #include <stdio.h>
    int main() {
    int N, soma = 0;

    // Solicita ao usuário que insira um número N
    printf("Digite um número inteiro positivo N: ");
    scanf("%d", &N);

    // Verifica se o número é positivo
    if (N < 1) {
        printf("Por favor, insira um número positivo.\n");
        return 1; // Encerra o programa com código de erro
    }

    // Calcula a soma de 1 a N
    for (int i = 1; i <= N; i++) {
        soma += i;
    }

    // Exibe o resultado
    printf("A soma dos números de 1 a %d é %d.\n", N, soma);

    return 0;
}



3

    #include <stdio.h>
    #include <stdbool.h>
    bool ehPrimo(int num) {
    if (num <= 1) return false;
    if (num <= 3) return true;
    if (num % 2 == 0 || num % 3 == 0) return false;
    for (int i = 5; i * i <= num; i += 6) {
        if (num % i == 0 || num % (i + 2) == 0) return false;
    }
    return true;
    }

    int main() {
    int numero;

    printf("Digite um número inteiro: ");
    scanf("%d", &numero);

    if (ehPrimo(numero)) {
        printf("O número %d é primo.\n", numero);
    } else {
        printf("O número %d não é primo.\n", numero);
    }

    return 0;
    }

4

    #include <stdio.h>
    int main() {
    int numero;

    printf("Digite um número inteiro: ");
    scanf("%d", &numero);

    printf("Tabela de multiplicação de %d:\n", numero);
    for (int i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", numero, i, numero * i);
    }

    return 0;
    }

5                 

    #include <stdio.h>
    #include <string.h>
    int main() {
    char str[100];
    int length, i;

    printf("Digite uma string: ");
    fgets(str, sizeof(str), stdin);

    length = strlen(str);
    if (str[length - 1] == '\n') {
        str[length - 1] = '\0';
        length--;
    }

    printf("String invertida: ");
    for (i = length - 1; i >= 0; i--) {
        printf("%c", str[i]);
    }
    printf("\n");

    return 0;
    }

6

    #include <stdio.h>

    int fatorial(int n) {
    if (n == 0 || n == 1) {
        return 1;
    }
    return n * fatorial(n - 1);
    }

    int main() {
    int numero;

    printf("Digite um número inteiro não negativo: ");
    scanf("%d", &numero);

    if (numero < 0) {
        printf("Número inválido. O número deve ser não negativo.\n");
        return 1;
    }

    printf("O fatorial de %d é %d.\n", numero, fatorial(numero));

    return 0;
    }
7

    #include <stdio.h>

    int main() {
    int array[10];
    int i, maior, menor;

    printf("Digite 10 números inteiros:\n");
    for (i = 0; i < 10; i++) {
        scanf("%d", &array[i]);
    }

    maior = menor = array[0];

    for (i = 1; i < 10; i++) {
        if (array[i] > maior) {
            maior = array[i];
        }
        if (array[i] < menor) {
            menor = array[i];
        }
    }

    printf("O maior valor é %d.\n", maior);
    printf("O menor valor é %d.\n", menor);

    return 0;
    }

8

     #include <stdio.h>

    #define N 10

    void bubbleSort(int array[], int n) {
    int i, j, temp;
    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < n - i - 1; j++) {
            if (array[j] > array[j + 1]) {
                // Troca array[j] e array[j + 1]
                temp = array[j];
                array[j] = array[j + 1];
                array[j + 1] = temp;
            }
        }
    }
    }

    int main() {
    int array[N];
    int i;

    printf("Digite %d números inteiros:\n", N);
    for (i = 0; i < N; i++) {
        scanf("%d", &array[i]);
    }

    bubbleSort(array, N);

    printf("Array ordenado em ordem crescente:\n");
    for (i = 0; i < N; i++) {
        printf("%d ", array[i]);
    }
    printf("\n");

    return 0;
    }

9

    #include <stdio.h>

    int main() {
    float celsius, fahrenheit;

    printf(": ");
    scanf("%f", &celsius);

    fahrenheit = (celsius * 9 / 5) + 32;

    printf(" %.2f.\n", fahrenheit);

    return 0;
    }

10

    #include <stdio.h>
    #include <ctype.h>

    int contarVogais(const char *str) {
    int count = 0;
    char ch;
    while ((ch = *str++) != '\0') {
        ch = tolower(ch);
        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
            count++;
        }
    }
    return count;
    }

    int main() {
    char str[100];

    printf("Digite uma string: ");
    fgets(str, sizeof(str), stdin);

    int numVogais = contarVogais(str);

    printf("Número de vogais na string: %d\n", numVogais);

    return 0;
    }
