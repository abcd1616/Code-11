# Code-11
Exp 11

#include <stdio.h>

void bubbleSort(int a[], int n)
{
    for (int i = 0; i < n - 1; i++)
    {
        for (int j = 0; j < n - i - 1; j++)
        {
            if (a[j] > a[j + 1])
            {
                int temp = a[j];
                a[j] = a[j + 1];
                a[j + 1] = temp;
            }
        }
    }
}

void display(int a[], int n)
{
    for (int i = 0; i < n; i++)
        printf("%d ", a[i]);

    printf("\n");
}

int main()
{
    int a[100], n;

    printf("Enter number of elements: ");
    if (scanf("%d", &n) != 1 || n < 1 || n > 100)
        return 0;

    printf("Enter %d elements:\n", n);

    for (int i = 0; i < n; i++)
    {
        scanf("%d", &a[i]);
    }

    bubbleSort(a, n);

    printf("Sorted array using Bubble Sort: ");
    display(a, n);

    return 0;
}
