# software-project
#include <stdio.h>
#include <math.h>

int main() {
    float a, b, c; 
    float discriminant, root1, root2, realPart, imagPart;
    printf("Enter coefficients a, b, and c: ");
    scanf("%f %f %f", &a, &b, &c);

    discriminant = b * b - 4 * a *c;
   if (discriminant > 0) 
    {
        root1 = (-b + sqrt(discriminant)) / (2 * a);
        root2 = (-b - sqrt(discriminant)) / (2 * a);
        printf("Roots are real and distinct:\n");
        printf("Root 1 = %.2f\n", root1);
        printf("Root 2 = %.2f\n", root2);
    } else if (discriminant == 0)
    {
        root1 = -b / (2 * a);
        printf("Roots are real and repeated:\n");
        printf("Root 1 = Root 2 = %.2f\n", root1);
    } else 
    {
        realPart = -b / (2 * a);
        imagPart = sqrt(-discriminant) / (2 * a);
        printf("Roots are complex:\n");
        printf("Root 1 = %.2f + %.2fi\n", realPart, imagPart);
        printf("Root 2 = %.2f - %.2fi\n", realPart, imagPart);
    }

    return 0;
}
output
enter coefficients a, b, and c: 2 3 6
Roots are complex:
Root 1 = -0.75 + 1.56i
Root 2 = -0.75 - 1.56i