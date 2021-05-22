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
    
double eh(int x,int n){
    static double s=1,m=1,a=1;
    double q=1;
    
    if(n==0){
        return s;
    }
    else{
        
        s=(1+(x*s/n));
        
        return eh(x,n-1);
        
    }
}
    
int main()
{
    cout<<e(2,5)<<endl;
    cout<<eh(2,5);

    return 0;
}

