#include<stdio.h>
int main(){
int n,m,i,j,k,y,max[20][20],alloc[20][20],avail[50],ind=0;
printf("\nEnter the number of Processes:");
scanf("%d",&n);
printf("\nEnter the number of Resources:");
scanf("%d",&m);
printf("\nEnter the Allocation memory:\n");
for(i=0;i<n;i++){
for(j=0;j<m;j++){
scanf("%d",&alloc[i][j]); }}
printf("\nEnter the Max Matrix:\n");
for(i=0;i<n;i++){
for(j=0;j<m;j++){
scanf("%d",&max[i][j]); }}
printf("\nenter the available matrix:\n");
for(i=0;i<m;i++)
scanf("%d",&avail[i]);
int finish[n],safe_sequence[n],work[m],need[n][m];
for(i=0;i<n;i++){
for(j=0;j<m;j++){
need[i][j]=max[i][j]-alloc[i][j]; }}
printf("\n Need Matrix is:");
for(i=0;i<n;i++){
printf("\n");
for(j=0;j<m;j++)
printf("%d",need[i][j]); }
for(i=0;i<m;i++){
work[i]=avail[i]; }
for(i=0;i<n;i++){
finish[i]=0; }
for(k=0;k<n;k++){
for(i=0;i<n;i++){
if(finish[i]==0){
int flag=0;
for(j=0;j<m;j++){
if(need[i][j]>work[j]){
flag=1;
break; }}
if(flag==0){
safe_sequence[ind++]=i;
for(y=0;y<m;y++)
work[y]+=alloc[i][y];
finish[i]=1; }}}}
printf("\n The System is in safe state\n Following is the safe sequence:\n");
for(i=0;i<=n-1;i++)
printf("P%d ", safe_sequence[i]);
printf("\n");
}
