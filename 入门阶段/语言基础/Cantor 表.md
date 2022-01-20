## 来源

[洛谷](https://www.luogu.com.cn/problem/P1014)

## 答案

~~~c++
#include <bits/stdc++.h>
using namespace std;

int main() {
	int m, n, i;
	cin >> n;

	for (i = 1; i < n; i++) {
		if ((1 + i)*i / 2 >= n) {
			m = n - (i - 1) * i / 2;
			break;
		}
	}

	if (i % 2 == 0) {
		cout << m << "/" << i + 1 - m;
	} else {
		cout << i + 1 - m << "/" << m;
	}

	return 0;
}
~~~

## 解析

注意找规律。