# CppMaxFinderInClass
This C++ program defines a class called Number that encapsulates the logic for inputting data and finding the maximum number within the class itself. The program creates three instances of the Number class to find the maximum numbers for each set of elements and finally compares the maximums to find the overall maximum.



#include <iostream>

using namespace std;

class Number {
public:
    int num[5];

    void getdata() {
        cout << "Enter 5 elements: ";
        for (int i = 0; i < 5; i++) {
            cin >> num[i];
        }
    }

    int findmax() {
        int max = num[0];
        for (int i = 1; i < 5; i++) {
            if (num[i] > max) {
                max = num[i];
            }
        }
        return max;
    }
};

int main() {
    Number T1, T2, T3;
    int max1, max2, max3;

    cout << "Enter data for Set 1:" << endl;
    T1.getdata();
    cout << "Enter data for Set 2:" << endl;
    T2.getdata();
    cout << "Enter data for Set 3:" << endl;
    T3.getdata();

    max1 = T1.findmax();
    max2 = T2.findmax();
    max3 = T3.findmax();

    int final_max = max1 > max2 ? max1 : max2;

    if (final_max > max3) {
        cout << "Maximum number among the sets: " << final_max << endl;
    } else {
        cout << "Maximum number among the sets: " << max3 << endl;
    }

    return 0;
}
