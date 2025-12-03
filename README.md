# Project-7-
Rock–Paper–Scissors
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int player, comp;

    printf("0 = Rock, 1 = Paper, 2 = Scissors\n");
    printf("Enter your choice: ");
    scanf("%d", &player);

    srand(time(0));
    comp = rand() % 3;

    printf("Computer chose: %d\n", comp);

    if (player == comp)
        printf("Draw!\n");
    else if ((player == 0 && comp == 2) ||
             (player == 1 && comp == 0) ||
             (player == 2 && comp == 1))
        printf("You Win!\n");
    else
        printf("You Lose!\n");

    return 0;
}
