# Diff-helman
#include <iostream>
#include<math.h>

using namespace std;

void Exchange(int p,int g,int xa,int xb )
{
     int k1,k2,ya,yb;

     ya=pow(g,xa);
     ya%=p;

     yb=pow(g,xb);
     yb%=p;

     k1=pow(yb,xa);
     k1%=p;

     k2=pow(ya,xb);
     k2%=p;

     if(k1==k2)
       {
         cout<<"Prime number is= "<<p<<endl;
         cout<<"Primitive root number is= "<<g<<endl;
         cout<<"Private keys are Xa= "<< xa <<" Xb= " <<xb<<endl;
         cout<<"Public keys are Ya= "<< ya <<" Yb= " <<yb<<endl;
         cout<<"New key is "<<k1<<endl;
       }
}



int main()
{
    int p,g,xa,xb;
    cout << "Enter a prime number " ;
    cin>> p;
    cout << "Enter a primitive roots " ;
    cin>> g;
    cout << "Enter two private keys " ;
    cin>> xa>>xb;

    Exchange(p,g,xa,xb);

    return 0;
}
