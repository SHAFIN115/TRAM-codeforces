# TRAM-codeforces
#include<stdio.h>
int main()
{
    int i,n,largest,j;
    int a[100000]={},b[100000]={},e[100000]={};
    scanf("%d",&n);
    for(i=0;i<n;i++)
        scanf("%d %d",&a[i],&b[i]);
    e[0]=a[0]+b[0];
    for(i=1;i<n;i++)
        e[i]=(e[i-1]-a[i])+b[i];
    largest=e[0];
    for (j=0;j<n;j++)
    {
      if (largest<=e[j])
               largest=e[j];
    }
    printf("%d",largest);
    return 0;

}
