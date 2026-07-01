# PALINDROME
ACTIVITY
#include <stdio.h>

int main() {
    int arr[100], size = 0;
    char ch;

    printf("Enter numbers separated by spaces: ");
    
    while (scanf("%d%c", &arr[size], &ch) == 2) {
        size++;
        if (ch == '\n') break; 
    }

    int left = 0, right = size - 1;
    while (left < right) {
        if (arr[left] != arr[right]) {
            printf("NOT PALINDROME\n");
            return 0;
        }
        left++;
        right--;
    }

    printf("PALINDROME\n");
    return 0;
}
