# BasicCodes
#include <stdio.h>
#include <stdlib.h>
#include<time.h>
int main()
{
printf("COIN TOSS\n");
float ph=0.0,pt=0.0,pe=0.0;
float i,e,n,h=0.0,t=0.0;
int q;
h=0;t=0;e=0;
printf("Enter no. of trials\n");
scanf("%f",&n);
srand(time(0));
for(i=0;i<n;i++)
{
q=0;
q=rand();
// printf("%d\n",q);
if(q<1000)
{
e=e+1;
}
else
{
if((q%2)==0)
{
h=h+1;
}
else
t=t+1;
}
}
ph=(h/n)*100;
pt=(t/n)*100;
pe=(e/n)*100;
printf("For %f coin tosses \nProbablity of getting heads is %f \nProbablity
of getting tails is %f\nProbablity of null event is %f \nTotal Probablity is %f
",n,ph,pt,pe,(ph+pt+pe));
return 0;
}
