# longest-arithematic-sub-arrray
#include <iostream>

using namespace std;

int main()
{
    int n;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    int cd=arr[1]-arr[0];
    int curr=2,final=0;
    
    for(int i=2;i<n;i++){
        if(arr[i]-arr[i-1]==cd){
            curr++;
        }
        if(arr[i]-arr[i-1]!=cd){
            cd=arr[i]-arr[i-1];
            curr=2;
        }
        final=max(final,curr);
    }
    cout<<final;

    return 0;
}
