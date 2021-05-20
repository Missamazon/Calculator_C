# Calculator_C
My first project in C: a calculator

#include <stdio.h>
#include <stdlib.h>
#include <math.h>



int main()
{
    int x, y;
    int signe;


/*Définir les termes des opérations*/
    printf("DEFINIR LE PREMIER NOMBRE : ");
    scanf ("%d",&x);
    printf("%d\n",x);

    printf(" 1 => +; 2=> -; 3 => x; 4 => / \n DEFINIR LE SIGNE DE L'OPERATION: ");
    scanf ("%d", &signe);
    if (signe==1)
    {
        printf ("Opérateur est +. \n");
    }
    else if (signe==2)
    {
        printf ("Opérateur est -. \n");
    }
    else if (signe==3)
    {
                printf ("Opérateur est x. \n");
    }
    else if (signe==4)
    {
        printf ("Opérateur est /. \n");
    }
    else
    {
        printf ("Opérateur invalide");
        return 0;
    }



    printf("DEFINIR LE SECOND NOMBRE : ");
    scanf ("%d",&y);
    printf("%d \n",y);

/*Faire le calcul selon opérateur*/

switch (signe)
{
    case(1):
        printf("%d + %d = %d", x, y, x+y);
    break;

    case(2):
        printf("%d - %d = %d", x, y, x-y);
    break;

    case (3):
        printf("%d x %d = %d", x, y, x*y);
    break;

    case (4):
        if(y != 0)
            printf("%d : %d = %d", x, y, (float) x/y);
        else
            printf("IMPOSSIBLE A CALCULER");
    break;
default : printf ("Opérateur inconnu");
}

return 0;
}
