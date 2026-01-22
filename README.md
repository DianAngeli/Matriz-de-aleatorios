#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main() {
    int m[10][10];
    int i,j,n,x,y,encontrado=0;
    srand(time(NULL));
    for(i=0;i<10;i++){
        for(j=0;j<10;j++){
            m[i][j]=rand()%100+1;
            printf("%d ",m[i][j]);
        }
        printf("\n");
    }
    scanf("%d",&n);
    for(i=0;i<10&&encontrado==0;i++){
        for(j=0;j<10&&encontrado==0;j++){
            if(n==m[i][j]){
                x=i;
                y=j;
                encontrado=1;
            }
        }
    }
    if(encontrado==1){
         printf("Encontrado en [%d] [%d]",x,y);
    }
    return 0;
}
