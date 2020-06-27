#include<stdio.h>
#include<math.h>
int main()
{
    int n;int a[2];
    while(scanf("%d",&n)!=EOF)
    {
        int i,j,p,s;
        s=0;
     for(i=1;i<=n;i++)
     {
        p=0;
     for(j=2;j<=i/2;j++)
     {
        if(i%j==0)
        {p=1;break;}
     }
    if(p==0&&s==0)
    {
     a[1]=i;s=1;
    }
    if(p==0&&s==1)
    {
        a[2]=i;s=0;
       if(a[2]-a[1]==2)
       {
        printf("%d %d\n",a[1],a[2]);s=0;
       }
       else
       {
        a[1]=a[2];a[2]=0;s=1;
       }
    }

     }
    }
}
