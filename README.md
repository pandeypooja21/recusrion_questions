# recursion_questions
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
Q2) FACTORIAL OF A NUMBER 
int  solve(int n){
    if(n==0){
        return 1;
        
    }
  return  n*solve(n-1);
    
}

int main() {
    int n;
    cin>>n;
  
    
 cout<<solve(n);
   

return 0;
}
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Q3) POWER CALCULATION

#include <bits/stdc++.h>
using namespace std;

double solve(double a, int b) {
    if (b == 0) {
        return 1;  // Base case: any number raised to the power 0 is 1
    }
    if(b<0){
        b=abs(b);
        a=1/a;
        
 }
    if(b%2==0){
        return solve(a*a,b/2);
    }
    return a * solve(a, b - 1);  // Multiply a by the result of a^(b-1)
}

int main() {
    double a;
    int b;
    cin >> a;
    cin>> b;
    cout << solve(a, b) << endl;
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Q4) SUM OF AN ARRAY: tc=O(n)
#include <bits/stdc++.h>
using namespace std;
int solve(vector<int>& arr,int index,int n,int sum){
    if(index==n){
        return sum;
    }
    return solve(arr,index+1,n,sum+arr[index]);
}



int main() {
    vector<int> arr={1,2,3,4,5};
   int n = arr.size();
    cout<<solve(arr,0,n,0);
    
return 0;
}


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Q5) FIBONACCI SEQUENCE 
#include <bits/stdc++.h>
using namespace std;
int  solve(int n){
    if(n==0){
        return 0;
        
  }
    if(n==1){
        return 1;
    }
  return  solve(n-1)+solve(n-2);
    
}

int main() {
    int n;
    cin>>n;
  
    
   
   for(int i=0;i<=n;i++){    // print the sequence(0,1,1,2,3,5,.......)
       cout<<solve(i)<<" ";
   }
   

  return 0;
}
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Q6) SUM OF DIGITS 
#include <bits/stdc++.h>
using namespace std;
int  solve(int n){
    if(n==0){
        return 0;
        
 }
   
  return  n%10+solve(n/10);
    
}

int main() {
   int n;
   cin>>n;
    cout<<solve(n);

  return 0;
}
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Q7) 

