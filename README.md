# A-number-guessing-game
#include <stdio.h>
#include <stdlib.h>   
#include <time.h>   

int main() {
    srand(time(0));
    int random_number = (rand() % 100) + 1;
    int no_of_guesses=0;
    int guessednumber;
    do{
         printf("Guess the number:");
         scanf("%d",&guessednumber);
         if(guessednumber>random_number){
            printf("Lower number please!\n");
         }
         else if(guessednumber<random_number){
            printf("Higher number please!\n");
         }
         else{
            printf("Congrats! You have guessed the right number.");
         }
         no_of_guesses++;
    }while(guessednumber!=random_number);

    printf("You guessed the number in %d guesses",no_of_guesses);
    return 0;
}
