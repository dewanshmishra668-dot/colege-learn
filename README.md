# colege-learn
This is my first repository
<br>
Author-Dewansh Mishra
#include<iostream>
#include<vector>
#include<unordered_map>
using namespace std;
vector<int> twosum(vector<int>&arr, int n, int tar){
    unordered_map<int, int> m;
    vector<int> ans;
    for(int i = 0; i < n; i++){
        int first = arr[i];
        int second = tar-first;
        if(m.find(second) != m.end()){
            ans.push_back(m[second]);
            ans.push_back(i);
            return ans;
        }
        m[first] = i;
    }
    return ans;
}
int main(){
    vector<int> arr = {1, 3, 4, 5, 6};
    int n = arr.size();
    int tar = 10;
    vector<int> result = twosum(arr, n, tar);
    for(int i : result){
        cout << i << " ";
    }
    return 0;
}

