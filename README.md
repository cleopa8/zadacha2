#include <stdio.h>
#include <stdlib.h>


void convert(int p, int q, int arr[]){
    int s = (q -p)/2;
    int np = p + s;
    int nq = q - 1 - s;
    int t;
   int i = p;
   int j = q-1;

   while(i < np && j >p + s){
             t = arr[i];
              arr[i] = arr[j];
              arr[j] = t;
              i++;
              j--;
   }
}

void convert2(int p, int q, int r, int arr[]){

    int t;
   int i = p;
   int j = q;
   int h = r;

   while(i < q || j <r){
             t = arr[i];
              arr[i] = arr[j];
              arr[j] = t;
              i++;
              j++;
   }
}
int main()
{
    int br;
    printf("Enter count of integer array elements:\n");
    scanf("%d", &br);
    int arr[br];
    printf("Enter integer array elements:\n");
    for(int i = 0; i < br; i++){
       scanf("%d", &arr[i]);

     // printf("%d", arr[i]);
    }
    int p, q, r;
    printf("Enter p:\n");
     scanf("%d", &p);
    printf("Enter q>p && q < count of array:\n");
     scanf("%d", &q);

      printf("Enter r>q>p && r < count of array:\n");
     scanf("%d", &r);
        convert(p,q,arr);
        for(int i = 0; i < br; i++){


         printf("%d\n", arr[i]);
       }
     convert2(p,q,r, arr);
     //convert(p,q,arr);

        for(int i = 0; i < br; i++){


      printf("%d\n", arr[i]);
    }

    return 0;
}
