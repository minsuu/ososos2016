
```c
#include <stdio.h>

int maxSub(int a[], int n){
	int i,j,ret=a[0]; // assume n>0
	for(i=0;i<n;i++){
		int sum=0;
		for(j=i;j<n;j++){
			sum += a[j];
			if(ret<sum) ret = sum;
		}
	}
	return ret;
}

int main(void) {
	int a[1010], n, i;
	scanf("%d",&n);
	for(i=0;i<n;i++) scanf("%d",&a[i]);
	printf("%d",maxSub(a,n));
	return 0;
}

```
