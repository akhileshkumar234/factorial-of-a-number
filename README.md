# factorial-of-a-number
a repository
#include <bits/stdc++.h>

using namespace std;
// Complete the extraLongFactorials function below.
void extraLongFactorials(int n) {
int res[200]={0};
res[0]=1;
int size=1;
for(int i=2;i<=n;i++)
{
    int c=0,p;
   for(int j=0;j<size;j++)
   {
     p=res[j]*i+c;
        res[j]=(p)%10;
        c=(p)/10;
   }
    while(c)
    {
        res[size]=c%10;
        c=c/10;
        size++;
    }
}
for(int j=size-1;j>=0;j--)
{
    cout<<res[j];
}

}

int main()
{
    int n;
    cin >> n;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    extraLongFactorials(n);

    return 0;
}
