
```c
#include <stdio.h>

int maxSub(int a[], int n){
	int i,j,k,ret=a[0]; // assume n>0
	for(i=0;i<n;i++){
		for(j=i+1;j<n;j++){
			int sum=0;
			for(k=i;k<=j;k++) sum += a[k];
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
