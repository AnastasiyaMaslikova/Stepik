# Stepik

Задача на программирование: последняя цифра большого числа Фибоначчи


Дано число 1 ≤ n ≤ 10^7, необходимо найти последнюю цифру n-го числа Фибоначчи.

Программа:

#include <iostream>
#include <stdio.h>

using namespace std;

int main() {
    int a = 0, b = 1, c, n;
    cin >> n;
    for (int i = 2; i <= n; i++) {
            c = (a + b) % 10;
            a = b;
            b = c;
        }
    cout << b;
    return 0;
}
