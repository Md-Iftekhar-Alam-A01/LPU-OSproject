#include<stdio.h>
#include<unistd.h>
int main(){
int n,i,j,a,b,c,x=0;
int temp=0;
printf("Enter number of processes\n");
scanf("%d",&n);
int q1[n],q2[n],q3[n];
int p[n],pro[n],bt[n],at[n],rt[n];
for(i=0;i<n;i++)
{
printf("enter process name for process %d = ",i+1,"\n");
printf("P");
scanf("%d",&pro[i]);
printf("enter priority for this process \n");
scanf("%d",&p[i]);
printf("enter burst time for this process \n");
scanf("%d",&bt[i]);
}
for(i=0;i<n-1;i++)
{
for(j=0;j<(n-i-1);j++)
{
if(p[j]>p[j+1]){
temp=p[j];
p[j]=p[j+1];
p[j+1]=temp;
temp=pro[j];
pro[j]=pro[j+1];
pro[j+1]=temp;
temp=bt[j];
bt[j]=bt[j+1];
bt[j+1]=temp;
}}
}
for(i=0;i<n;i++)
{
printf("Process P%d",pro[i]);
printf(" with priority %d",p[i]);
printf(" has burst time %d",bt[i]);
printf("\n");
}
printf("\nenter the number of processes you want to process in queue 1 \n");
scanf("%d",&a);
printf("enter the number of processes you want to process in queue 2 \n");
scanf("%d",&b);
printf("enter the number of processes you want to process in queue 3 \n");
scanf("%d",&c);
for(i=0;i<a;i++){
q1[x]=p[i];
x=x+1;
}


