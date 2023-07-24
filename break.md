```
#define _CRT_SECURE_NO_WARNINGS
/*
	1부터 N까지 연속한 자연수의 합이 M을 초과하지 않는 경우
	최대 N은? 1+2+3+...+N<=M
	모든 과정은 int형으로 가능한 범위
*/
#include <stdio.h>

int main(void)
{
	int N = 50;		// 구구단에서 N을 초과하면 중단....
	for (int i = 1; i <= 9; i++)
	{
		int flag = 0;
		for (int j = 1; j <= 9; j++)
		{
			if (i * j > N)
			{
				flag = 1;
				break; // for j
			}
			else
			{
				printf("%4d", i * j);
			}
		}
		if (flag)
		{
			break; // for i
		}
		printf("\n");
	}

	return 0;
}
```
