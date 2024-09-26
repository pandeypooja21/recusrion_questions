# recusrion_questions
contain all the resursion questions and their implementation
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Q1) IMPLEMENTING BINARY SERACH BY RECURSION   : tc=O(logn)
#include <bits/stdc++.h>
using namespace std;

int solve(vector<int>& arr, int start, int end, int x) {
    if (start <= end) {
        int mid = start + (end - start) / 2;
  if (arr[mid] == x)
            return mid;
   if (arr[mid] < x)
            return solve(arr, mid + 1, end, x);
        else
            return solve(arr, start, mid - 1, x);
    }
    return -1;
}

int main() {
    vector<int> arr = {1, 4, 6, 7, 9, 10};
    int x;
    cin >> x;
    int ans = solve(arr, 0, arr.size() - 1, x);
    cout << ans;
 return 0;
}
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

