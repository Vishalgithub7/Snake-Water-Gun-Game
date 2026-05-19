# Snake-Water-Gun-Game
Developed a Snake, Water, Gun game implementing game logic with conditional statements and random number generation (stdlib.h).

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int snakeWaterGun(char you, char comp) {
    // returns 1 if you win, -1 if you lose, 0 if draw
    if (you == comp) return 0;

    if (you == 's' && comp == 'w') return 1;
    else if (you == 'w' && comp == 's') return -1;

    if (you == 's' && comp == 'g') return -1;
    else if (you == 'g' && comp == 's') return 1;

    if (you == 'w' && comp == 'g') return 1;
    else if (you == 'g' && comp == 'w') return -1;
}

int main() {
    char you, comp;
    srand(time(0));
    int number = rand() % 100 + 1;

    if (number < 33) comp = 's';
    else if (number > 33 && number < 66) comp = 'w';
    else comp = 'g';

    printf("Enter 's' for Snake, 'w' for Water or 'g' for Gun: ");
    scanf("%c", &you);

    int result = snakeWaterGun(you, comp);
    printf("You chose %c and computer chose %c. ", you, comp);

    if (result == 0) printf("Game Draw!\n");
    else if (result == 1) printf("You Win!\n");
    else printf("You Lose!\n");

    return 0;
}
