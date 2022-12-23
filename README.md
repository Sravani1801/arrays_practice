# arrays_practice
1) finding index of largest element of an array
// naive approach

#include <bits/stdc++.h>
using namespace std;

int getlargest(int arr[],int n)
{
    for(int i=0;i<n;++i)
    {
        bool flag=true;
        for(int j=i;j<n;++j)
        {
            if(arr[j]>arr[i])
            {
                flag=false;
                break;
            }
        }
        if(flag==true)
    {
        return i;
    }
    }
    
    return -1;
}
int main()
{
    int arr[]={1,7,5};
    cout<<getlargest(arr,3);
    return 0;
}
