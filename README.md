
#include <stdio.h>
#include <locale.h>
#include <conio.h>
int main()
{
   double x1,x2,delta,y;
    unsigned int i=1,N;
    unsigned char A;
    printf("Enter variant (1 or 2): \n");
    scanf("%c",&A);


    if(A=='1')
    {
      printf("x1=");
       scanf("%lf", &x1);

      printf("x2=");
        scanf("%lf", &x2);

      printf("N \n");
        scanf("%d",&N);

       printf("x1: %.2lf\nx2: %.2lf\nN: %d\n",x1,x2,N );
       printf("**********************************\n");
       printf("\t* N * X * F(X) *\t\n");
       printf("**********************************\n");

        for(i; i<=N; i++)
       {
        y=x1*5;
        printf("\t| %d| %.2lf| %.2lf|\t\n",i,x1,y);
        printf("+----------+----------+----------+\n");
        x1=(x1-x2)/(N-1);
       }
    }



   else if(A=='2')
   {

    printf("x1=");
     scanf("%lf", &x1);

    printf("x2=");
      scanf("%lf", &x2);

    printf("delta= ");
     scanf("%lf",&delta);

    printf("x1: %.2lf\delta: %.2lf\x2: %.2lf\n", x1,x2,delta );
    printf("**********************************\n");
    printf("\t* delta * X * F(X) *\t\n");
    printf("**********************************\n");

    for(i; i<=x2; i++)
    {
        y=x1*5;
        printf("\t| %d| %.2lf| %.2lf|\t\n",i,x1,y);
        printf("+----------+----------+----------+\n");
        x1=(x1-x2)/(delta+1);
    }
   }
return 0;
}
