# Binary-Search-
Binary Search is defined as a searching algorithm used in a sorted array by repeatedly dividing the search interval in half. The idea of binary search is to use the information that the array is sorted and reduce the time complexity to O(log N). 

#include <stdio.h>
int binarySearch(int arr[], int l, int r, int x)
{
	while (l <= r) {
		int m = l + (r - l) / 2;

		
		if (arr[m] == x)
			return m;

		
		if (arr[m] < x)
			l = m + 1;


		else
			r = m - 1;
	}


	return -1;
}

                               
int main(void)
{
	int arr[] = { 2, 3, 4, 10, 40 };
	int n = sizeof(arr) / sizeof(arr[0]);
	int x = 10;
	int result = binarySearch(arr, 0, n - 1, x);
	(result == -1) ? printf("Element is not present"
							" in array")
				: printf("Element is present at "
							"index %d",
							result);
	return 0;
}
