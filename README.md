#include<stdio.h>
int main()
{
	int a[2][2],b[2][2],c[2][2],i,j;
	int p,q,r,s,t,u,v;
	printf("enter the elemennts for first matrix");
	for(i=0;i<2;i++)
	for(j=0;j<2;j++)
	scanf("%d",&a[i][j]);
	printf("enter the elements for second matrix:");
	for(i=0;i<2;i++)
	for(j=0;j<2;j++)
	scanf("%d",&b[i][j]);
	printf("\n the first matrix is\n");
	for(i=0;i<2;i++)
	{
	printf("\n");
	for(j=0;j<2;j++)
	
	printf("%d\t",a[i][j]);
}
printf("\n the second matrix is\n");
	for(i=0;i<2;i++)
	{
	printf("\n");
	for(j=0;j<2;j++)
	printf("%d\t",b[i][j]);
}
p=(a[0][0]+a[1][1])*(b[0][0]+b[1][1]);
q=(a[1][0]+a[1][1])*b[0][0];
r=a[0][0]*(b[0][1]-b[1][1]);
s=a[1][1]*(b[1][0]-b[0][0]);
t=(a[0][0]+a[0][1])*b[1][1];
u=(a[1][0]-a[0][0])*(b[0][0]+b[0][1]);
v=(a[0][1]-a[1][1])*(b[1][0]+b[1][1]);
c[0][0]=p+s-t+v;
c[0][1]=r+t;
c[1][0]=q+s;
c[1][1]=p-q+r+u;
printf("\n after multiplication\n");
	for(i=0;i<2;i++)
	{
	printf("\n");
	for(j=0;j<2;j++)
	printf("%d\t",c[i][j]);
}
	return 0;
}
