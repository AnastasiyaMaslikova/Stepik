# Stepik

Задача на программирование повышенной сложности: огромное число Фибоначчи по модулю

Даны целые числа 1 ≤ n ≤ 10^18 и 2 ≤ m ≤ 10^5, необходимо найти остаток от деления n-го числа Фибоначчи на m.

Программа:

#include <iostream>
#include <vector>

using namespace std;

int main() {
    long long n = 0;
    long long m = 0;
    cin >> n;
    cin >> m;
    vector <long long> F(2);
    F[0] = 0;
    F[1] = 1;
    long long t = 0;
    for (long long j = 2; j < m ^ 2 + 1; ++j) {
        F.push_back ((F[j - 1] + F[j - 2]) % m);
        ++t;
        if ((F[j] == 1) && (F[j - 1] == 0)) break;
    }
    cout << F[n % t] << endl;
    return 0;
}
