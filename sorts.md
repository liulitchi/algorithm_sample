### 插入排序（Insertion sort）

- C 语言代码

```c
#include <stdio.h>

void insertion_sort(int arr[], int len);

int main(void) {
	int list1[] = {243, 205, 165, 849, 907, 128, 78};
	int arr_len = sizeof(list1) / sizeof(list1[0]);
	insertion_sort(list1, arr_len);
	
	printf("result = {");
	for (int i = 0; i < arr_len; i++)
		printf("%d, ", list1[i]);
	printf("}\n");

	return 0;
}

void insertion_sort(int arr[], int len) {
	for (int i = 1; i < len; i++) {
		int key = arr[i];
		while ((i - 1 >= 0) && (arr[i - 1] > key)) {
			arr[i] = arr[i - 1];
			i--;
		}
		arr[i] = key;
	}
}
```
