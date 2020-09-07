# Ada-Matrix
#include <bits/stdc++.h>
using namespace std;

int main() {

    int t;
    cin>>t;
    while(t--){
            int n;
        cin>>n;
        vector<int> A(n*n+1);
        for(int i=1;i<A.size();i++){
               cin>>A[i];
        }

    int operations=0;
    for(int j=n;j>0;j--){
        if(A[j]!=j){
                operations++;
            vector<int> B=A;
            for(int i=1;i<=j;i++){
                for(int k=1;k<=j;k++){
                    A[(i-1)*n+k]=B[(k-1)*n+i];
                }
            }
        }
    }
    cout<<operations<<endl;
    }

}

