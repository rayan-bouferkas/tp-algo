#include <stdio.h>
int add(int a, int b){
    return a + b ;
}

int max(int a, int b){
    if (a > b) 
      return a;
    else 
      return b;
   
}

float average(int arr[], int n){
    int sum = 0;
    for (int i = 0; i < n; i++){
        sum = add(sum, arr[i]);
    }
}
int main () {
    int n;
    printf("donner num n :");
    scanf("%d", &n);
    int arr[n];
    for (int i = 0; i < n; i++){
        printf("donner numbre de tab %d :", i + 1);
        scanf("%d", &arr[i]);
    }
    int largest = arr[0];
    for (int i = 0; i < n; i++){
        largest = max(largest, arr[i]);
    }
    float avg = average(arr, n);
    printf("max est : %d\n", largest);
    printf("averrage est : %2.f\n", avg);
    return 0;
}
