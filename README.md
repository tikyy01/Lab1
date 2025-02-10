#include <iostream>
#include <Windows.h>
using namespace std;

bool Palindrome(int y) {
    int x = 0, original = y;
    while (y > 0) {
        x = (x << 1) | (y & 1);
        y >>= 1; 
    }
    return original == x;
}

int main() {
    SetConsoleCP(1251);
    SetConsoleOutputCP(1251);
    int number;
    cout << "Введите число: ";
    cin >> number;
    if (Palindrome(number)) {
        cout << number << " является палиндромом в двоичной системе.\n";
    }
    else {
        cout << number << " не является палиндромом в двоичной системе.\n";
    }
    return 0;
}
