j
```c
#include <stdio.h>
int main(int argc, char *argv[]) {
	if (argc<3){
		printf("not enough arguments!");
		return 0;
	}
	FILE *in, *out;
	int n;
	in = fopen(argv[1],"r");
	out = fopen(argv[2],"w");
	fscanf(in,"%d",&n);
	fprintf(out,"%d",n);
	fclose(in);
	fclose(out);
	return 0;
}




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
