#include <stdio.h>
int main()
{
    int n;
    int mark = 1;
    scanf("%d",&n);
    int a[n];
    for(int i = 0; i < n ;i++){
        scanf("%d",&a[i]);
    }
    int b[99] = {0};
    for(int j = 0; j < n; j++){
        b[a[j]+50]++;
    }
    for(int k = 0; k < 99; k++){
        if(b[k] > n/2){
            printf("%d",k-50);
            mark = 0;
            break;
        }
    }
    if(mark == 1)
    printf("no");
    return 0;
}
