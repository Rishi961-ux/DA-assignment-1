#include <iostream>
#include <vector>
#include <algorithm>  // for std::max
using namespace std;

int maxSubarraySum(const vector<int>& arr) {
    int maxSoFar = arr[0];
    int maxEndingHere = arr[0];
    for (size_t i = 1; i < arr.size(); ++i) {
        maxEndingHere = max(arr[i], maxEndingHere + arr[i]);
        maxSoFar = max(maxSoFar, maxEndingHere);
    }
    return maxSoFar;
}
int main() {
    vector<int> arr = {-2, -5, 6, -2, -3, 1, 5, -6};
    cout << "Maximum subarray sum: " << maxSubarraySum(arr) << endl;
  
    return 0;
}
