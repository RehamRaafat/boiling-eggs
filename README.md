#include <bits/stdc++.h>

using namespace std;

int main()
{
    int t;
    cin>>t;
    int test=1;
    while(t)
    {
        int n,p,q,cnt=0,sum=0;
        vector<int>v;
        cin>>n>>p>>q;
        for(int i=0; i<n; i++)
        {
            int y;
            cin>>y;
            v.push_back(y);
        }
        sort(v.begin(),v.end());
        for(int k=0; k<p && k<n; k++)
        {
                if(v[k]<=q)
                {
                    cnt++;
                    sum+=v[k];
                    q-=v[k];
                }
                else
                    break;
        }


        cout<<"Case "<<test<<": "<<cnt<<endl;
        t--;
        test++;
    }
    return 0;
}
