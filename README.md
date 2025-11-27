# C---calculator-
#include <stdio.h>

int main() {
    int choice;
    float a, b, result;

    while (1) {
        // Menu
        printf("\n====== SIMPLE CALCULATOR ======\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        // Exit condition
        if (choice == 5) {
            printf("Exiting... Thank you!\n");
            break;
        }

        // Taking inputs
        printf("Enter first number: ");
        scanf("%f", &a);
        printf("Enter second number: ");
        scanf("%f", &b);

        switch (choice) {
            case 1:
                result = a + b;
                printf("Result = %.2f\n", result);
                break;

            case 2:
                result = a - b;
                printf("Result = %.2f\n", result);
                break;

            case 3:
                result = a * b;
                printf("Result = %.2f\n", result);
                break;

            case 4:
                if (b == 0)
                    printf("Error! Division by zero not allowed.\n");
                else {
                    result = a / b;
                    printf("Result = %.2f\n", result);
                }
                break;

            default:
                printf("Invalid choice! Please try again.\n");
        }
    }

    return 0;
}
