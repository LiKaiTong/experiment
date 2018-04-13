# experiment
The experiment code
The essential use of Visual C++
#include<iostream>
using namespace std;
void main()
{
	int f(int n,int m);
    cout<<"Please input two number:";
    int a,b;
    cin>>a>>b;
    if(a>b) cout<<f(a,b)<<endl;
	else cout<<f(b,a)<<endl;
}

int f(int n,int m)
{
	return (n%m==0)?m:f(m,n%m);
}
#include<iostream>
using namespace std;
void main()
{
	int a,b=3,c,d,m;
	int power(int n);
	cout<<"a=";
	cin>>a;
	cout<<endl<<"m=";
	cin>>m;
	c=a*b;
	d=power(a);
cout<<endl<<c<<endl<<d<<endl;
}

int power(int n)
{
return n*n*n;
}
