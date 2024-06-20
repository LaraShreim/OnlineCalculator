/*the function of this program it to create a command line Calculator by entering one of the 5 types of 
mathmatical expression we will use, then we choose the type of operation depending on the type of the expression we used,
then the output will be printed out.
we will both the while loop statement and the switch statement for this program.*/



#include <stdio.h> // C Standard Library for input/output functions
#include <stdlib.h>
#include <math.h>
int main()
{
    char letter;//used to input in scanner by the user
    char operation;//used to input the operation and its type.
    float num1;//input first number in the calculator.
    float num2;//input second number in the calculator.
    float answer;//the output after the calculation of the 2 inputs num1 and num2.
    int x=0;//used for the if functions
    float memoryslots[5] = {0.00}; //to determine the length of the memory slot
    char memory;//store the 5 memory slots
    float n;//used for the scanf functions
    char userinput1[100];//used for calculation of the memory slots of first number
    char userinput2[100]; //used for calculation of the memory slots of second number
    char Option2;//input operation but for the memory slots
    char Input2;//input of the mempry slots
    
    /*we print the welcome statement include the name of the develope and date of the program */ 
    printf("Welcome to my command-line calculator (CLC)\n");
    printf("Developer: Lara Shreim\n");
    printf("Version: Assignment 1\n");
    printf("Date:10/20/2023\n");
    printf("-----------------------------------------------------------------------------\n");
    /*then we print the five outputs and the function of each of the output*/
    printf("Select one of the following items:\n");
    printf("B)-Binary Mathmatical Operations, such as addition and subtraction.\n");
    printf("U)-Unary Mathmatical Operations, such as square root, and log.\n");
    printf("A)-Advances Mathmatical Operations, using variables, arrays.\n");
    printf("V)-Define variables and assign them values.\n");
    printf("E)-Exit\n");
    printf("-----------------------------------------------------------------------------\n");
    printf("Please select your option (B, U, A, V, E):\n");
    /* this loop will not break as long as the choice variable does not equal to E which is the exit output*/
    while(letter!='E')
{    
    /*then scan the choice as an input in the switch statement */    
    scanf(" %c", &letter);
    
    /*start the switch statement of choice between (B, U, A, V, and E)*/
    switch (letter)
    {
        case'B'://the first case in the switch statement
            
            printf("\n(+) stands for addition.\n");
            printf("(-) stands for subtraction.\n");
            printf("(*) stands for multiplitication.\n");
            printf("(/) stands for division.\n");
            printf("(P) stands for power.\n");
            printf("(X) stands for Maximum.\n");
            printf("(I) stands for Minimum.\n");
            printf("-----------------------------------------------------------------------------\n");
            puts("Please enter the first number: ");
        x = scanf("%f", &num1);

        if(x!= 1){ 
            break;
        }

        puts("Please enter the operation ( +, -, *, /, %%, P, X, I ): "); 
        scanf(" %c", &operation);

        if(operation == '+' || operation == '-' || operation == '*' || operation == '/' || operation == '%' || operation == 'P' || operation == 'X' || operation == 'I'){

        } 

        else{
            break;
        }

        puts("Please enter the second number: ");
        x = scanf("%f", &num2); 

        if(x!= 1){ 
            break;
        }

    
        switch(operation){

            case '+' : //addition case
            answer = num1 + num2;
            printf("The answer is %f\n", answer);
            puts("Please select your option (B, U, A, V, E):\n");
            break;
            
            case '-' : //substraction case
            answer = num1 - num2;
            printf("The answer is %f\n", answer);
            puts("Please select your option (B, U, A, V, E):\n");
            break;

            case '*' : //multiplication case
            answer = num1 * num2;
            printf("The answer is %f\n", answer);
            puts("Please select your option (B, U, A, V, E):\n");
            break;

            case '/' : //division case
            if(num2 == 0) {
                
                printf("invalid\nPlease select your option (B, U, A, V, E):\n");
                break;
            }
            answer = num1 / num2;
            printf("The answer is %f\n", answer);
            puts("Please select your option (B, U, A, V, E):\n");
            break;

            case '%' : //remainder case
            answer = fmod(num1,num2); 
            printf("The answer is %f\n", answer);
            puts("Please select your option (B, U, A, V, E):\n");
            break;

            case 'P' : //power case
            answer = pow(num1,num2);
            printf("The answer is %f\n", answer);
            puts("Please select your option (B, U, A, V, E):\n");
            break;
            
            case 'X' : //maximum number case
            if(num1 > num2){
                answer = num1;
            }

            else{
                answer = num2;
            }

            printf("The answer is %f\n", answer);
            puts("Please select your option (B, U, A, V, E):\n");
            break;


            case 'I'://minimum number case
            if(num1 < num2){
                answer = num1;
            }

            else{
                answer = num2;
            }
            printf("The answer is %f\n", answer);
            puts("Please select your option (B, U, A, V, E):");
            break;

            default : puts("that is not a valid operation");
            puts("Please select your option (B, U, A, V, E):\n");
            break;
        }
    break;
        case'U':
        
        printf("(S) stands for square root\n");
        printf("(L) stands for logarithm base e\n");
        printf("(E) stands for exponentiation\n");
        printf("(C) stands for cieling of number\n");
        printf("(F) stands for floor of number\n");
        printf("------------------------------------------\n");
        puts("Please enter the operation (S, L, E, C, F ):");
        scanf(" %c", &operation); 

        if(operation == 'S' || operation == 'L' || operation == 'E' || operation == 'C' || operation == 'F'){
                
        }

        else{
            break;
        }

        puts("Please enter a number: "); 
        x = scanf("%f", &num1); 

        if(x!= 1){ 
            break;
        }
        
        switch(operation){ 

            case 'S': //square root case
                answer = sqrt(num1);
                printf("The answer is %f\n", answer);
                puts("Please select your option (B, U, A, V, E):\n");
                break;

            case 'L': //logarithm case
                answer = log(num1);
                printf("The answer is %f\n", answer);
                puts("Please select your option (B, U, A, V, E):\n");
                break;

            case 'E': // e function case
                answer = exp(num1);
                printf("The answer is %f\n", answer);
                puts("Please select your option (B, U, A, V, E):\n");
                break;

            case 'C': //ceiling case
                answer = ceil(num1);
                printf("The answer is %f\n", answer);
                puts("Please select your option (B, U, A, V, E):\n");
                break;

            case 'F': //floor case
                answer = floor(num1);
                printf("The answer is %f\n", answer);
                puts("Please select your option (B, U, A, V, E):\n");
                break;

            default : 
                puts("that is not a valid operation");
                puts("Please select your option (B, U, A, V, E):\n");
                break;

        }

        break;
        case 'V' : 
        printf("\nYour current memory slots: \n");
        for(int i = 0; i < 5; i++){ 
            printf("%c: %f\n", 'a' + i, memoryslots[i]);
        }


            printf(" choose which slot you would like to change : ");
            scanf(" %c", &memory); 

            if(memory == 'a' || memory == 'b' || memory == 'c' || memory == 'd' || memory == 'e' ){ 

        }

        else{
            break;
        }

            printf("What digit would you like to enter ? : ");
            x = scanf(" %f", &num1);

            if(x!= 1){ 
                break;
            }
        

        switch(memory){ /*5 memory slots all initialized to zero but the user 
                          can input a number in any of the 5 memory slots*/

            case 'a':
                memoryslots[0] = num1; 
                break;

            case 'b':
                memoryslots[1] = num1;
                break;

            case 'c':
                memoryslots[2] = num1;
                break;

            case 'd':
                memoryslots[3] = num1;
                break;

            case 'e':
                memoryslots[4] = num1;
                break;

            default: 
                puts("invalid slot!");
                puts("Please select your option (B, U, A, V, E):\n");
                break;


        }
        puts("Please select your option (B, U, A, V, E):\n");
        break;

    case 'A':/*use the memoryslots array variable to calculate
                  binary and unary functions*/

        printf("Please select option (B, U, E): ");//3 options available
        scanf(" %c", &Option2);

            switch(Option2){ 

            case 'B' :

            printf("Please enter first number (A,B,C,D,E for storage variables): ");
            scanf(" %s", userinput1);

            if(userinput1[0]=='A') { 
                 num1 = memoryslots[0];
            }

            else if(userinput1[0]=='B') {
                 num1 = memoryslots[1];
            }

            else if(userinput1[0]=='C') {
                 num1 = memoryslots[2];
            }

            else if(userinput1[0]=='D') {
                 num1 = memoryslots[3];
            }

            else if(userinput1[0]=='E') {
                num1 = memoryslots[4];
            }

            else {
                num1 = atof(userinput1);
            }

            printf("Please enter an operation (+,-,*,/,%%,P,X,I) : ");
            scanf(" %c", &operation); 

            printf("Please enter second number (A,B,C,D,E for storage variables): ");
            scanf(" %s", userinput2);

            if(userinput2[0]=='A') {
                 num2 = memoryslots[0];
            }

            else if(userinput2[0]=='B') {
                 num2 = memoryslots[1];
            }

            else if(userinput2[0]=='C') {
                 num2 = memoryslots[2];
            }

            else if(userinput2[0]=='D') {
                num2 = memoryslots[3];
            }

            else if(userinput2[0]=='E') {
                num2 = memoryslots[4];
            }

            else {
                num2 = atof(userinput2);
            }

            switch(operation){
            case '+' : 
            answer = num1 + num2;
            printf("The answer is %f\n", answer);
            break;
            
            case '-' : 
            answer = num1 - num2;
            printf("The answer is %f\n", answer);
            break;

            case '*' : 
            answer = num1 * num2;
            printf("The answer is %f\n", answer);
            break;

            case '/' : 
            if(num2 == 0) {
                printf("Invalid\n");
                break;
            }
            answer = num1 / num2;
            printf("The answer is %f\n", answer);
            break;

            case '%' : 
            answer = fmod(num1,num2); 
            printf("The answer is %f\n", answer);
            break;

            case 'P' : 
            answer = pow(num1,num2);
            printf("The answer is %f\n", answer);
            break;

            case 'X' : 
            if(num1 > num2){
                answer = num1;
            }

            else{
                answer = num2;
            }

            printf("The answer is %f\n", answer);
            break;
            
            case 'I':
            if(num1 < num2){
                answer = num1;
            }

            else{
                answer = num2;
            }
            printf("The answer is %f\n", answer);
            break;
            
            default : puts("that is not a valid operation");
            break;

            }

            puts("Please select your option (B, U, A, V, E)");

            break;

            case 'U' :

                puts("Please enter the operation ( S(sqrt), L(logarithm), E(e^x), C(ceiling), F(floor)");
                scanf(" %c", &operation);

                printf("Please enter first number (a,b,c,d,e for storage variables): ");
                scanf(" %s", userinput1);
                
                if(userinput1[0]=='A') { 
                    num1 = memoryslots[0];
                }

                else if(userinput1[0]=='B') {
                     num1 = memoryslots[1];
                }

                else if(userinput1[0]=='C') {
                    num1 = memoryslots[2];
                }

                else if(userinput1[0]=='D') {
                    num1 = memoryslots[3];
                }

                else if(userinput1[0]=='E') {
                    num1 = memoryslots[4];
                }

                else {
                    num1 = atof(userinput1);
                }

                switch(operation){ 

                case 'S':
                    answer = sqrt(num1);
                    printf("The answer is %f\n", answer);
                    puts("Please select your option (B, U, A, V, E)");
                    break;

                case 'L':
                    answer = log(num1);
                    printf("The answer is %f\n", answer);
                    puts("Please select your option (B, U, A, V, E)");
                    break;

                case 'E':
                    answer = exp(num1);
                    printf("The answer is %f\n", answer);
                    puts("Please select your option (B, U, A, V, E)");
                    break;

                case 'C':
                    answer = ceil(num1);
                    printf("The answer is %f\n", answer);
                    puts("Please select your option (B, U, A, V, E)");
                    break;

                case 'F':
                    answer = floor(num1);
                    printf("The answer is %f\n", answer);
                    puts("Please select your option (B, U, A, V, E)");
                    break;

                default : 
                    puts("that is not a valid operation");
                    puts("Please select your option (B, U, A, V, E)");
                    break;
                }

                break;

            case 'E' :
            puts("Please select your option (B, U, A, V, E)");
            break; 

            default:
            break;
        }

        break;
        case'E'://if the user insert E the calculator will exit with a goodbye message
        printf("Thanks for using my Simple Calculator. Hope to see you soon again, Goodbye!");
        break;
        
        /*if we insert the other 3 options which are U, A, and V, or any other
        value that is not related to the function, the the default answer will be the following*/ 
        default:
               
                printf("invalid");
                puts("\nPlease select your option (B, U, A, V, E):");
                break;
    }
    
}
    

}


