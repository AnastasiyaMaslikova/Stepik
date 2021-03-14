# Stepik

Задача на программирование: небольшое число Фибоначчи

Дано целое число 1 ≤ n ≤ 40, необходимо вычислить nn-е число Фибоначчи (напомним, что F0 = 0, F1 = 1 и Fn = F(n−1) + F(n−2) при n ≥ 2).

Программа:

#include <cassert>
#include <iostream>

class Fibonacci {
public:
static int get(int n) {
assert(n >= 0);
if (n == 0 || n == 1) {
return n;
}
return get(n - 2) + get(n - 1); 
}
};

int main(void) {
int n;
std::cin >> n;
std::cout << Fibonacci::get(n) << std::endl;
return 0;
}
