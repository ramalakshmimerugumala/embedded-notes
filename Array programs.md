## .WRITE A C PROGRAM TO FIND THE SUM OF ELEMENTS IN AN ARRAY USING A WHILE LOOP?
program
## 1️⃣ Program to Find the Sum of Elements in an Array Using `while` Loop
```
#include <stdio.h>
int main() {
    int arr[4];
    int sum = 0;

    printf("Enter the elements:\n");
    for(int i = 0; i < 4; i++) {
        scanf("%d", &arr[i]);
    }

    int i = 0;
    while(i < 4) {
        sum = sum + arr[i];
        i++;
    }

    printf("Sum of the elements: %d\n", sum);
    return 0;
} 

# Output
Enter the elements
1
2
3
4
Sum of the elements10
```

# 2 Reverse of an array
Program
```
#include <stdio.h>
int main() {
   int arr[]={34,56,54,32,67,89,90,32,21};
   int size=sizeof(arr)/sizeof(arr[0]);
   printf("Original array:\n");
   for(int i=0;i<size;i++){
       printf("%d\t",arr[i]);
   }
   printf("\n");
   printf("reverse of the array:\n");
   for(int i=8;i>=0;i--){
       printf("%d\t",arr[i]);
   }
    return 0;
}
# Output
Original array:
34	56	54	32	67	89	90	32	21	
reverse of the array:
21	32	90	89	67	32	54	56	34
```

# 3.Remove duplicate elements in the array
program
```
#include <stdio.h>
int main(){
    int arr[6];
    int size = 6;

    printf("Enter elements in the array:\n");
    for(int i = 0; i < size; i++){
        scanf("%d", &arr[i]);
    }

    for(int i = 0; i < size; i++){
        for(int j = i + 1; j < size;j++){
            if(arr[j] == arr[i]){
                for(int k = j; k < size; k++){
                    arr[k] = arr[k + 1];
                }
                size--;
                j--;
            }
        }
    }

    printf("After removing duplicates:\n");
    for(int i = 0; i < size; i++){
        printf("%d ", arr[i]);
    }

    return 0;
}
## Output
Enter elements in the array:
1 2 2 3 4 4
After removing duplicates:
1 2 3 4
```
## Insertion of Element in the arry
```
// Online C compiler to run C program online
#include <stdio.h>
int main(){
int arr[6];
int position;
int number;
printf("Enter elements in the array:");
for(int i=0;i<5;i++){
        scanf("%d",&arr[i]);
}
printf("Original elements in the array:");
for(int i=0;i<5;i++){
        printf("%d",arr[i]);
}
printf("\nEnter the position");
scanf("%d",&position);
printf("\nEnter the number");
scanf("%d",&number);
for(int i=4;i>=position-1;i--){
        arr[i+1]=arr[i];
}
        arr[position-1]=number;
for(int i=0;i<=5;i++){
        printf("%d\n",arr[i]);
}
}
Output:
Enter elements in the array:1
2
4
7
6
Original elements in the array:12476
Enter the position2

Enter the number3
1
3
2
4
7
6
