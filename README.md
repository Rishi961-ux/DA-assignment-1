#include <iostream>
using namespace std;

int main() {
    int arr[] = {2, 5, 8, 12, 16, 23, 38, 56, 71, 91};
    int n = 10;
    int key = 23;

int low = 0, high = n - 1, mid;

   while (low <= high) {
        mid = (low + high) / 2;
  if (arr[mid] == key) {
            cout << "Element found at index: " << mid << endl;
            cout << "Position (1-based): " << mid + 1 << endl;
            return 0;
        }
        else if (arr[mid] < key) {
            low = mid + 1;
        }
        else {
            high = mid - 1;
        }
    }

    cout << "Element not found" << endl;
    return 0;
}
