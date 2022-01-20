## 来源

[洛谷](https://www.luogu.com.cn/problem/P5594)

## 答案

~~~c++
#include <bits/stdc++.h>
using namespace std;

int main() {
	int n, m, k, i, j, p, c;
	cin >> n >> m >> k;
	int a[m][k], b[k] = {0};

	for (i = 0; i < m; i++)
		for (j = 0; j < k; j++)
			a[i][j] = 0;

	while (n--) {
		p = 0;

		for (i = 0; i < m; i++) {
			cin >> c;
			a[p++][c - 1] = 1;
		}
	}

	for (i = 0; i < m; i++) {
		for (j = 0; j < k; j++) {
			if (a[i][j] == 1)
				b[j]++;
		}
	}

	for (i = 0; i < k; i++)
		cout << b[i] << " ";

	return 0;
}
~~~

## 解析

模拟过程。