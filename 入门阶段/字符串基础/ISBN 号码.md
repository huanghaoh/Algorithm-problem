## 来源

[洛谷](https://www.luogu.com.cn/problem/P1055)

## 答案

~~~c++
#include <bits/stdc++.h>
using namespace std;

int main() {
	char a[13], b;
	int i, j = 1, s = 0;
	cin.getline(a, 14);

	for (i = 0; i < 11; i++) {

		if (a[i] >= '0' && a[i] <= '9') {
			s += (a[i] - 48) * j++;
		}
	}

	s %= 11;

	if (s == 10) {
		b = 'X';
	} else {
		b = char(s + 48);
	}

	if ( b == a[12])
		cout << "Right";
	else {
		a[12] = b;

		for (i = 0; i < 13; i++)
			cout << a[i];
	}

	return 0;
}
~~~

## 解析

注意不要忘记 “X” ，int 和 char 类型的转化。