# Arrays-two-dimensional-
Use program language  C++ to create array
/* write a program that creates a 5 by 5, two-dimensional array that store  25 integers*/

#include <stdio.h>
const int M = 3;
const int N = 3;
void print (int arr[M] [N])
{
    int i, j;
    for (i = 0; i < M; i++)
        for (j = 0; j < N; j++)
        printf("%d ", arr[i][j]);
}

void print_RowSum (int arr[M][N])
{
    int sum = 0;
    int i, j;

    for (i = 0; i< M; ++i)
    {
        for (j =0; j < N; ++j)
        {
            sum = sum + arr[i][j];
        }
        printf ("sum of the %d row is = %d\n", i, sum);
        sum = 0;
    }
}

void print_ColSum(int arr[M][N])
{
    int i, j;
    int sum = 0;
    for (j =0; j < M; ++j)
    {
        for (i = 0; i< N; ++i)
        {
           sum = sum + arr[i][j]; 
        }
        printf ("sum of the %d column is = %d\n", j, sum);
        sum = 0;
    }
}

void calculateTotal(int arr[M] [N])
{
    int i, j;
    int sum = 0;
    for (j =0; j < M; ++j)
    {
         for (i = 0; i< N; ++i)
           {
           sum = sum + arr[i][j]; 
        }
         printf ("Sum of all the values is = %d\n", sum);
    }

    void findMaxn(int arr[M][N])
    {
        int max = arr[0][0];
        int i, j;

        for (i = 0; i < M; i++)
         for (j = 0; j < N; j++)
         {
            if (arr[i][j]> max)
            max = arr[i][j];
         }
         printf("Maximum value is %d\n", max);
    }
    int main()
    {
        int arr[M][N];
        int p, q;
        printf( "Enter the number for the array");
        for (p = 0; p < M; p++)
            for (q =0; q <N; q++)
            scanf("%d", &arr[p][q]);
        print(arr);
        print_RowSum(arr);
        print_ColSum(arr);
        findMaxn(arr);
        calculateTotal(arr);
        return 0;

    }
}
