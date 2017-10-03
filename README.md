# quadraticequation

#include<stdio.h>
#include<math.h>
#include<stdlib.h>
int main()
{
    float a,b,c;
    float root1,root2,imagp,realp,disc;
    printf("To find the roots of a non-zero equation\n");
    printf("Enter value of a,b,c\n");
    scanf("%f%f%f",&a,&b,&c);
    disc=(b*b)-(4*a*c);
    if(a*b*c==0)
    {
        printf("Enter non-zero co-efficients");
        exit(0);
    }
    if (disc==0)
    {
            printf("Roots are real and equal\n");
            root1=-b/2*a;
            printf("root1=root2=%f",root1);
    }
    else if(disc>0)
    {
            printf("Roots are real and disinct\n");
            root1 = -b+sqrt(disc)/(2*a);
            root2 = -b-sqrt(disc)/(2*a);
            printf("root1=%f\n root2=%f",root1,root2);
    }
    else
    {
            printf("Roots are imaginary\n");
            realp=-b/2*a;
            imagp=-sqrt(abs(disc))/(2*a);
            printf("Real root=%f\n Imaginary root=%f\n",realp,imagp);
    }
}
