#include <stdio.h>
#include <math.h>

int main()
{
    int i;
    int N=1000000;
    double x;
    double xx;
    double eps=1e-15;
    
    printf("初期値を入力");
    scanf("%lf",&x);
    
    for(i=0;i<N;i++)
    {
        xx=x-(x*x-4.0)/(2.0*x);
        
        if(fabs(x-xx)<eps)
        break;
    }
    
    printf("x=%10lf\n",xx);
    return 0;
}

