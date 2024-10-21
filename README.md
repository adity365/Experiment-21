# Experiment-21
AIM : To study searching algorithm and its types(binary and linear search) in C++.

# Searching Algorithm :
In C++, searching algorithms are used to find a specific element or group of elements within a data structure like an array, list, or tree. There are two main types of searching algorithms: linear search and binary search. 

1. Linear Search
Description: This is the simplest searching algorithm. It works by checking each element in the array or list until the desired element is found or the end of the array is reached.
Time Complexity: O(n)
When to use: When the list is unsorted or very small.

2. Binary Search
Description: This algorithm is more efficient than linear search but requires the array to be sorted. It works by repeatedly dividing the search interval in half. If the key is less than the middle element, it searches the left half, otherwise, it searches the right half.
Time Complexity: O(log n)
When to use: When the list is sorted.

# Code Performed in Lab :
Experiment 21(a)
```
// linear search

// Name --> Aditya Agarwal
// PRN --> 23070123162

#include <bits/stdc++.h>
using namespace std;

int search(int arr[], int N, int x)
{
    for (int i = 0; i < N; i++)
        if (arr[i] == x)
            return i;
    return -1;
}

// Driver code
int main(void)
{
    int arr[] = { 2, 3, 4, 10, 40 };
    int x = 10;
    int N = sizeof(arr) / sizeof(arr[0]);

    // Function call
    int result = search(arr, N, x);
    (result == -1)
        ? cout << "Element is not present in array"
        : cout << "Element is present at index " << result;
    return 0;
}
```
output :
![image](https://github.com/user-attachments/assets/151a2f36-eabd-40da-9e56-37d5a1eeb14c)

Experiment 21(b):
```
// binary Search

// Name --> Aditya Agarwal
// PRN --> 23070123162

# include <iostream>
using namespace std;

// An iterative binary search function.
int binarySearch(int arr[], int low, int high, int x)
{
    while (low <= high) {
        int mid = low + (high - low) / 2;

        // Check if x is present at mid
        if (arr[mid] == x)
            return mid;

        // If x greater, ignore left half
        if (arr[mid] < x)
            low = mid + 1;

        // If x is smaller, ignore right half
        else
            high = mid - 1;
    }

    // If we reach here, then element was not present
    return -1;
}

// Driver code
int main(void)
{
    int arr[] = { 2, 3, 4, 10, 40 };
    int x = 10;
    int n = sizeof(arr) / sizeof(arr[0]);
    int result = binarySearch(arr, 0, n - 1, x);
    if(result == -1){
        cout << "This Element is not present in array";
    } 
    else {
        cout << "Element is present at index " << result;
    }
    return 0;
}
```
Output :
![image](https://github.com/user-attachments/assets/cd3fa674-94cd-4c13-9287-b57be310d321)

# CONCLUSION :
We have learned and implemented sorting and its types which is mainly linear and binary sort in C++.
