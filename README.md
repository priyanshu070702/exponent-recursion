# exponent-recursion

#include <iostream>
using namespace std;

double e(int x,int n){
    static double m=1,a=1;
    double r;
    
    if (n==0){
        return 1;
    }
    else{
        r=e(x,n-1);
        m=m*x;
        a=a*n;
        
        return r+(m/a);
    }
}
int main()
{
    
    cout<<e(2,5);

    return 0;
}
