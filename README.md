# movimenta-o-xadrez-em-c
#include <stdio.h>

// uso da recursividade na prática:
void rainhamov1(int r) {
    if (r > 0) {
        printf("A rainha andou 1 casa/casas para a esquerda\n");
        rainhamov1(r - 1);
    }
}

int main() {

    int r = 8;
    int bispo = 1;
    int torre;
    int movimentocompleto1 = 1;

    // movimentação da rainha
    rainhamov1(r);

    // movimentação do bispo
    do {
        printf("O Bispo se movimentou %d casa/casas na diagonal direita!\n", bispo);
        bispo++;
    } while (bispo <= 5);

    // movimentação da torre
    for (torre = 1; torre <= 5; torre++) {
        printf("A torre se movimentou uma casa/casas para a direita\n");
    }

    // movimentação cavalo:
    while (movimentocompleto1--) {
        for (int cavalo = 0; cavalo < 2; cavalo++) {
            printf("O cavalo foi para Cima\n");
        }
        printf("O cavalo foi para a Direita\n");
        printf("O cavalo se movimentou uma vez!!!");
    }

    return 0;
}
