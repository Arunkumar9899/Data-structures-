#include<stdio.h>
int main()
{
	int i,n,a[10],pos,key,option;
	printf("enter the n element");
	scanf("%d",&n);
	printf("enter the elements");
	for(i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
		
}
	printf("enter the pos and  key values");
	scanf("%d%d",&pos,&key);
	printf("1.insert\n2.delete\n");
	scanf("%d",&option);
	switch(option)
	{
		case 1:
			for(i=n;i>=pos;i--)
			{
				a[i]=a[i-1];
			}
			a[pos-1]=key;
			for(i=0;i<=n;i++)
			{
				printf("%d",a[i]);
					
			}
			break;
		case 2:
			for(i=pos;i<n;i++)
			{
				a[i]=a[i+1];
				for(i=0;i<n-1;i++)
				{
					printf("%d",a[i]);
				}
			}
			break;
			
			
	}
	
}
