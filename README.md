# experiment
The experiment code
The essential use of Visual C++
实验二
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
实验三
#include<iostream>
using namespace std;

class student
{
private:
	int num;
	char name[20];
	char sex;
	int age;
	float grade1,grade2,grade3,aver;
public:
	void input();
	void average();
	void whether();
	void display();
};

void student::input()
{
	cout<<"Please input the number of the student:";
	cin>>num;
	cout<<endl<<"Please input the name of the student:";
	cin>>name;
	do{
		cout<<"Please input the sex:";
		cin>>sex;
		if(sex=='m'||sex=='M'||sex=='w'||sex=='W') break;
		else cout<<endl<<"Please input M/W !"<<endl;
	}while(true);
	do{
		cout<<"Please input the age of the student:";
		cin>>age;
		if(age>0&&age<=120) break;
		else cout<<endl<<"Please input the right age!"<<endl;
	}while(true);
	cout<<"Please input three grades:";
	cin>>grade1>>grade2>>grade3;
	cout<<endl;
}

void student::average()
{
	aver=(grade1+grade2+grade3)/3;
}

void student::whether()
{
	int count=0;
	if(grade1<60) count++;
	if(grade2<60) count++;
	if(grade3<60) count++;
	cout<<"The student :"<<name<<"has "<<count<<"fails"<<endl;
}

void student::display()
{
	cout<<num<<"\t"<<name<<"\t"<<sex<<"\t"<<age<<"\t"<<aver<<"\t"<<endl;
}
void main()
{
	student stu1,stu2,stu3;
	stu1.input();
	stu2.input();
	stu3.input();
	stu1.average();
	stu2.average();
	stu3.average();
	stu1.whether();
	stu2.whether();
	stu3.whether();
	cout<<"No.\t"<<"Name\t"<<"Sex\t"<<"Age\t"<<"Average\t"<<endl;
	stu1.display();
	stu2.display();
	stu3.display();
}
实验四
include<iostream>
#include<string>
using namespace std;
class Student
{
private:
	int number;
	string name;
	char sex;
	float class1;
	float class2;
	float class3;
	float aver;
public:
	 Student();
	void Input();
	void Modify();
	void Average();
	void Display();
	string Name();
	float averout();
	float class1out();
	float class2out();
	float class3out();
};

 Student::Student()
{
	class1=0;
	class2=0;
	class3=0;
	aver=0;
}

void Student::Input()
{
	cout<<"No.";
	cin>>number;
	cout<<"Name:";
	cin>>name;
	do{
		cout<<"Sex:";
		cin>>sex;
		if(sex=='m'||sex=='M'||sex=='w'||sex=='W') break;
		else cout<<endl<<"Please input M/W !"<<endl;
	}while(true);
	do{cout<<"If the student take the class1?(Y/N)";
		char choice;
	cin>>choice;
	if(choice=='y'||choice=='Y')  
	{
		cout<<"Class1:";
		cin>>class1; break;
	}
	else if(choice=='n'||choice=='N') {class1=-1; break;}
	else cout<<"Please input a right character!"<<endl;
		}while(true);

	{if(class1==-1) 
	{
		cout<<"Class2:";
		cin>>class2;
	}
	else {
		do{cout<<"If the student take the class2?(Y/N)";
		char choice;
	cin>>choice;
	if(choice=='y'||choice=='Y')  
	{
		cout<<"Class2:";
		cin>>class2; break;
	}
	else if(choice=='n'||choice=='N') {class2=-1; break;}
	else cout<<"Please input a right character!"<<endl;
		}while(true);
	}
	}
	if(class1==-1||class2==-1)
	{
		cout<<"Class3:";
		cin>>class3;
	}
	else {
	do{cout<<"If the student take the class3?(Y/N)";
		char choice;
	cin>>choice;
	if(choice=='y'||choice=='Y')  
	{
		cout<<"Class3:";
		cin>>class3; break;
	}
	else if(choice=='n'||choice=='N') {class3=-1; break;}
	else cout<<"Please input a right character!"<<endl;
		}while(true);
	}
}
void Student::Modify()
{do{
  cout<<"1 No."<<number<<endl<<"2 Name:"<<name<<endl<<"3 Sex:"<<sex<<endl;
  if(class1>=0) cout<<"4 Class1:"<<class1;
  else cout<<"4 Class1: No";
  cout<<endl;
  if(class2>=0) cout<<"5 Class2:"<<class2;
  else cout<<"5 Class2: No";
  cout<<endl;
  if(class3>=0) cout<<"6 Class3:"<<class3<<endl;
  else cout<<"6 Class3: No"<<endl;
  	cout<<"Please choose the number to modify:";
	int a;
	cin>>a;
	switch (a){
	case 1:	{cout<<"No.";cin>>number;break;}
	case 2:{cout<<"Name:";cin>>name;break;}
	case 3:	{do{
		cout<<"Sex:";
		cin>>sex;
		if(sex=='m'||sex=='M'||sex=='w'||sex=='W') break;
		else cout<<endl<<"Please input M/W !"<<endl;
			}while(true);break;}
	case 4:	do{cout<<"If the student take the class1?(Y/N)";
		      char choice;
	         cin>>choice;
	         if(choice=='y'||choice=='Y')  
			 {
    		cout<<"Class1:";
	     	cin>>class1; break;
			 }
	        else if(choice=='n'||choice=='N') {class1=-1; break;}
         	else cout<<"Please input a right character!"<<endl;
		   }while(true); break;
	case 5:
			do{cout<<"If the student take the class2?(Y/N)";
		      char choice;
	         cin>>choice;
	         if(choice=='y'||choice=='Y')  
			 {
    		cout<<"Class2:";
	     	cin>>class2; break;
			 }
	        else if(choice=='n'||choice=='N') {class2=-1; break;}
         	else cout<<"Please input a right character!"<<endl;
		   }while(true); break;
	case 6:	do{cout<<"If the student take the class3?(Y/N)";
		      char choice;
	         cin>>choice;
	         if(choice=='y'||choice=='Y')  
			 {
    		cout<<"Class3:";
	     	cin>>class3; break;
			 }
	        else if(choice=='n'||choice=='N') {class3=-1; break;}
         	else cout<<"Please input a right character!"<<endl;
		   }while(true); break;
	}
	cout<<"If you want to continue modify this student?(input 0 to exit,any other number to continue)";
	int i;
	cin>>i;
	if(i==0) break;
}while(true);
}

void Student::Average()
{
	float average(float a,float b);
    float average(float a,float b,float c);
	float a,b;
	if(class1>=0&&class2>=0&&class3>=0) aver=average(class1,class2,class3);
	else {
		if(class1>=0)  {a=class1;if(class2>=0) b=class2;else b=class3;}
		else {a=class2;b=class3;}
		aver=average(a,b);
	}
}
		            
string Student::Name()
{
	return name;
}

float Student::averout()
{
	return aver;
}

float Student::class1out()
{
	return class1;
}

float Student::class2out()
{
	return class2;
}

float Student::class3out()
{
	return class3;
}

void Student::Display()
{
   cout<<number<<"\t"<<name<<"\t"<<sex<<"\t";
  if(class1>=0) cout<<class1<<"\t";
  else cout<<"No\t";
  if(class2>=0) cout<<class2<<"\t";
  else cout<<"No"<<"\t";
  if(class3>=0) cout<<class3<<"\t";
   else cout<<"No"<<"\t";
  cout<<aver<<endl; 
}


 void main()
{
	 cout<<"Please input the number of the student:";
	int num;
	cin>>num;
	Student *stu=new Student[num];
	for(int i=0;i<num;i++)
	{
		stu[i].Input();
	}
	do{
		string b;
		cout<<"Please input the name of the student:";
		cin>>b;
		for(int i=0;i<num;i++)
		{
			if(b==stu[i].Name()) stu[i].Modify();
		}
         cout<<"If you want to continue modify?(input 0 to exit,any other number to continue)";
    	int j;
	    cin>>j;
    	if(j==0) break;
	}while(true);
    int j;
	Student temp;
	for(i =0;i<num;i++)
	{
		stu[i].Average();
	}

	
	cout<<"No.\t"<<"Name\t"<<"Sex\t"<<"Class1\t"<<"Class2\t"<<"Class3\t"<<"Average"<<endl;
	for(i=0;i<num;i++)
	{
		stu[i].Display();
	}
	float sum1=0,aver1,max1=0,min1=0,num1=0;
	
	for(i=0;i<num;i++)
	{
		float x;
		x=stu[i].class1out();
		if(x>=0)
		{sum1=sum1+x;
		if(x>max1) max1=x;
		min1=x;
		if(x<min1) min1=x;
		num1++;
		}
	}
	aver1=max1/num1;

    float sum2=0,aver2,max2=0,min2=0,num2=0;

	for(i=0;i<num;i++)
	{
		float y;
		y=stu[i].class2out();
		if(y>=0)
		{sum2=sum2+y;
		if(y>max2) max2=y;
		min2=y;
		if(y<min2) min2=y;
		num2++;
		}
	}
	aver2=max2/num2;

    float sum3=0,aver3,max3=0,min3=0,num3=0;
	
	for(i=0;i<num;i++)
	{
		float z;
		z=stu[i].class3out();
		if(z>=0)
		{sum3=sum3+z;
		if(z>max3) max3=z;
		min3=z;
		if(z<min3) min3=z;
		num3++;
		}
	}
	aver3=max3/num3;
	cout<<endl;
	cout<<"Class\t"<<"Max\t"<<"Min\t"<<"Average"<<endl;
	cout<<"Class1\t"<<max1<<"\t"<<min1<<"\t"<<aver1<<endl;
	cout<<"Class2\t"<<max2<<"\t"<<min2<<"\t"<<aver2<<endl;
	cout<<"Class3\t"<<max3<<"\t"<<min3<<"\t"<<aver3<<endl;

	
		cout<<"Please input the name of the student to search:";
		string b;
		cin>>b;
		for( i=0;i<num;i++)
		{

			if(b==stu[i].Name()) 
			{cout<<"No.\t"<<"Name\t"<<"Sex\t"<<"Class1\t"<<"Class2\t"<<"Class3\t"<<"Average"<<endl;
			stu[i].Display();}
		}





 

	
}



float average(float a,float b)
{
	float c;
	c=(a+b)/2;
	return c;
}

float average(float a,float b,float c)
{
	float d;
	d=(a+b+c)/3;
	return d;
}
实验五
#include<iostream>
using namespace std;
class Date
{
public:
	int year,month,day;
	int leap(int);
	long dton();
	Date ntod(long);
public:
	Date(){};
	Date(int y,int m,int d){year=y;month=m;day=d;}
	Date operator+(long);
	Date operator-(long);
	long operator-(Date &);
	void disp();
};

int Date::leap(int year)
{
	if(year%4==0&&year%100!=0||year%400==0)
		return 1;
	else return 0;
}

long Date::dton()
{
int day_tab[2][12]={31,28,31,30,31,30,31,31,30,31,30,31,31,29,31,30,31,30,31,31,30,31,30,31};
	long days=0;
	int y,m,lp_year=leap(year);
	for(y=1;y<year;y++)
	{
		if(leap(y)) days+=366;
		else days+=365;
	}
	for(m=1;m<month;m++)
	{
		days+=day_tab[lp_year][m-1];
	}
	days+=day;
	return days;
}

Date Date::ntod(long n)
{int day_tab[2][12]={31,28,31,30,31,30,31,31,30,31,30,31,31,29,31,30,31,30,31,31,30,31,30,31};
	int y=1,m=1,d;
	for(;;)
	{
		if(leap(y)) {if(n<=366) break;
		            else n-=366;}
		else {if(n<=365) break;
		            else n-=365;}
		y++;
	}
	int lp_year=leap(y);
	for(;;)
	{
		if(n<=day_tab[lp_year][m-1]) break;
		else n-=day_tab[lp_year][m-1];
		m++;
	}
	d=n;  return Date(y,m,d);
}

Date Date::operator+(long days)
{
	long n;
	n=dton();
	return(ntod(n+days));
}

Date Date::operator-(long days)
{
	
	return(ntod(dton()-days));
}

long Date::operator-(Date &b)
{
	if(dton()>b.dton())
	return(dton()-b.dton());
	else return(b.dton()-dton());
}

void Date::disp()
{
	cout<<year<<"--"<<month<<"--"<<day<<endl;
}



void main()
{
	do{
	cout<<"*****************"<<endl;
	cout<<"* 1.Date + days *"<<endl;
	cout<<"* 2.Date - days *"<<endl;
	cout<<"* 3.Date - Date *"<<endl;
	cout<<"*Input 0 to exit*"<<endl;
	cout<<"*****************"<<endl;
	int choice_num;
	cin>>choice_num;
	if(choice_num==1) 
	{
		int year1,month1,day1,days1;
		cout<<"Year=";
		cin>>year1;
		cout<<"Month=";
		cin>>month1;
		cout<<"Day=";
		cin>>day1;
		cout<<"days=";
		cin>>days1;
		Date *p1=new Date(year1,month1,day1);
		Date *p2=new Date();
		*p2=(*p1)+days1;
		cout<<p2->year<<"--"<<p2->month<<"--"<<p2->day<<endl;
		delete p1,p2;
	}
	else
	if(choice_num==2)
	{
      int year2,month2,day2,days2;
		cout<<"Year=";
		cin>>year2;
		cout<<"Month=";
		cin>>month2;
		cout<<"Day=";
		cin>>day2;
		cout<<"days=";
		cin>>days2;
		Date *p1=new Date(year2,month2,day2);
		Date *p2=new Date();
		*p2=(*p1)-days2;
		cout<<p2->year<<"--"<<p2->month<<"--"<<p2->day<<endl;
		delete p1,p2;
	}
	else
	if(choice_num==3)
	{
		int year3,month3,day3,year4,month4,day4;
		cout<<"Year1=";
		cin>>year3;
		cout<<"Month1=";
		cin>>month3;
		cout<<"Day1=";
		cin>>day3;
		cout<<"Year2=";
		cin>>year4;
		cout<<"Month2=";
		cin>>month4;
		cout<<"Day2=";
		cin>>day4;
		Date *p1=new Date(year3,month3,day3);
		Date *p2=new Date(year4,month4,day4);
		int between_days=*p1-*p2;
		cout<<"The discrepant days is:"<<between_days<<endl;
	}
	else
	if(choice_num==0) break;
	else
		cout<<"Please input a right number!"<<endl;
}while(true);

}
实验六
#include<iostream>
#include<string>
using namespace std;

class Basis
{
protected:
	string name;
	char sex;
	int age;
public:
	Basis(string name_input,char sex_input,int age_input)
	{name=name_input;
	sex=sex_input;
	age=age_input;}
	void display()
	{
		cout<<"1 Name:"<<name<<endl<<"2 Sex:"<<sex<<endl<<"3 Age:"<<age<<endl;
	}
    void modify(){
	display();
    cout<<"Please choose the number to modify:";
	int a;
	cin>>a;
	switch (a){
	case 1:cout<<"Name:";
	       cin>>name;break;
	case 2: do{
		cout<<"Sex:";
		cin>>sex;
		if(sex=='m'||sex=='M'||sex=='w'||sex=='W') break;
		else cout<<endl<<"Please input M/W !"<<endl;
			}while(true);break;
	case 3:cout<<"Age:";
	        cin>>age;break;
	}
	}

};

class Teacher : virtual public Basis
{
protected:
	int work_num;
private:
	string title;
	int salary;
public:
	Teacher(string name_input,char sex_input,int age_input,int work_num_input,string title_input,int salary_input):Basis(name_input,sex_input,age_input)
	{work_num=work_num_input;
	title=title_input;
	salary=salary_input;}
	string getTitle(){
		return title;}
	int getSalary(){return salary;}
	void setTitle()
	{cin>>title;}
	void setSalary(){
	cin>>salary;}
	void display(){
       cout<<"1 Name:"<<name<<endl<<"2 Sex:"<<sex<<endl<<"3 Age:"<<age<<endl<<"4 Work_num:"<<work_num<<endl<<"5 Title:"<<title<<endl<<"6 Salary:"<<salary<<endl;
	}
	void modify()
	{
		display();
    cout<<"Please choose the number to modify:";
	int a;
	cin>>a;
	switch (a){
	case 1:cout<<"Name:";
	       cin>>name;break;
	case 2: do{
		cout<<"Sex:";
		cin>>sex;
		if(sex=='m'||sex=='M'||sex=='w'||sex=='W') break;
		else cout<<endl<<"Please input M/W !"<<endl;
			}while(true);break;
	case 3:cout<<"Age:";
	        cin>>age;break;
	case 4:
	        cout<<"Work_num:";
	      cin>>work_num;break;
	case 5: cout<<"Title:";
        	cin>>title;break;
	case 6:
	     cout<<"Salary:";
	       cin>>salary;break;
	}
	}

};


class Student:virtual public Basis
{
protected:
	int num;
	int classes;
	string major;
	float grade;
public:
	Student(string name_input,char sex_input,int age_input,	int num_input,int classes_input,string major_input,float grade_input):Basis(name_input,sex_input,age_input)
	{num=num_input;
	classes=classes_input;
	major=major_input;
	grade=grade_input;}
	void display(){
    cout<<"1 Name:"<<name<<endl<<"2 Sex:"<<sex<<endl<<"3 Age:"<<age<<endl<<"4 No:"<<num<<endl<<"5 Class:"<<classes<<endl<<"6 Major:"<<major<<endl<<"7 Grade:"<<grade<<endl;
	}
	
     void modify()
	{
		display();
    cout<<"Please choose the number to modify:";
	int a;
	cin>>a;
	switch (a){
	case 1:cout<<"Name:";
	       cin>>name;break;
	case 2: do{
		cout<<"Sex:";
		cin>>sex;
		if(sex=='m'||sex=='M'||sex=='w'||sex=='W') break;
		else cout<<endl<<"Please input M/W !"<<endl;
			}while(true);break;
	case 3:cout<<"Age:";
	        cin>>age;break;
	case 4:cout<<"No:";
	       cin>>num;break;
	case 5:cout<<"Class:";
	       cin>>classes;break;
	case 6:cout<<"Major:";
	       cin>>major;break;
	case 7:cout<<"Grade:";
	       cin>>grade;break;
	}
	 }

};

class Graduate: public Student,public Teacher
{
protected:
	string workplace;
public:
	Graduate(string name_input,char sex_input,int age_input,int work_num_input,string title_input,int salary_input,int num_input,int classes_input,string major_input,float grade_input,string workplace_input):Student(name_input,sex_input,age_input,num_input,classes_input,major_input,grade_input),Teacher(name_input,sex_input,age_input,work_num_input,title_input,salary_input),Basis(name_input,sex_input,age_input)
	{workplace=workplace_input;
	}
	void display(){
    cout<<"1 Name:"<<name<<endl<<"2 Sex:"<<sex<<endl<<"3 Age:"<<age<<endl<<"4 Work_num:"<<work_num<<endl<<"5 Title:"<<getTitle()<<endl<<"6 Salary:"<<getSalary()<<endl<<"7 No:"<<num<<endl<<"8 Class:"<<classes<<endl<<"9 Major:"<<major<<endl<<"10 Grade:"<<grade<<endl<<"11 Workplace:"<<workplace<<endl;
	}
    void modify()
	{
		display();
    cout<<"Please choose the number to modify:";
	int a;
	cin>>a;
	switch (a){
	case 1:cout<<"Name:";
	       cin>>name;break;
	case 2: do{
		cout<<"Sex:";
		cin>>sex;
		if(sex=='m'||sex=='M'||sex=='w'||sex=='W') break;
		else cout<<endl<<"Please input M/W !"<<endl;
			}while(true);break;
	case 3:cout<<"Age:";
	        cin>>age;break;
	case 4:
	        cout<<"Work_num:";
	      cin>>work_num;break;
	case 5: cout<<"Title:";
		setTitle();break;
	case 6:
	     cout<<"Salary:";
		 
		   setSalary();break;
    case 7:cout<<"No:";
	       cin>>num;break;
	case 8:cout<<"Class:";
	       cin>>classes;break;
	case 9:cout<<"Major:";
	       cin>>major;break;
	case 10:cout<<"Grade:";
	       cin>>grade;break;
	case 11:cout<<"Workplace:";
		   cin>>workplace;break;
	}
	 }


	

};

class Teacher_studying:public Student,public Teacher
{
public:
	Teacher_studying(string name_input,char sex_input,int age_input,int work_num_input,string title_input,int salary_input,int num_input,int classes_input,string major_input,float grade_input):Student(name_input,sex_input,age_input,num_input,classes_input,major_input,grade_input),Teacher(name_input,sex_input,age_input,work_num_input,title_input,salary_input),Basis(name_input,sex_input,age_input)
	{}
	void display(){
     cout<<"1 Name:"<<name<<endl<<"2 Sex:"<<sex<<endl<<"3 Age:"<<age<<endl<<"4 Work_num:"<<work_num<<endl<<"5 Title:"<<getTitle()<<endl<<"6 Salary:"<<getSalary()<<endl<<"7 No:"<<num<<endl<<"8 Class:"<<classes<<endl<<"9 Major:"<<major<<endl<<"10 Grade:"<<grade<<endl;
	}
  void modify()
	{
		display();
    cout<<"Please choose the number to modify:";
	int a;
	cin>>a;
	switch (a){
	case 1:cout<<"Name:";
	       cin>>name;break;
	case 2: do{
		cout<<"Sex:";
		cin>>sex;
		if(sex=='m'||sex=='M'||sex=='w'||sex=='W') break;
		else cout<<endl<<"Please input M/W !"<<endl;
			}while(true);break;
	case 3:cout<<"Age:";
	        cin>>age;break;
	case 4:
	        cout<<"Work_num:";
	      cin>>work_num;break;
	case 5: cout<<"Title:";
        	setTitle();break;
	case 6:
	     cout<<"Salary:";
	       setSalary();break;
    case 7:cout<<"No:";
	       cin>>num;break;
	case 8:cout<<"Class:";
	       cin>>classes;break;
	case 9:cout<<"Major:";
	       cin>>major;break;
	case 10:cout<<"Grade:";
	       cin>>grade;break;
	}
  }
};
实验七
#include<iostream>
#include<cmath>
using namespace std;
class Plane
{
public:
	virtual float area() const=0;
	virtual float girth() const=0;
};

class Body
{
private:
	Plane *pbasic;
	float high;
public:
	float volume(){return high*pbasic->area();}
	float surfaceArea(){return (2*pbasic->area()+pbasic->girth()*high);}
	void setPbasic(Plane& plane){pbasic=&plane;}
	void setHigh(){cin>>high;}
};

class Rectangle:public Plane
{
private:
	float a;
	float b;
public:
	virtual float area() const {return a*b;}
	virtual float girth() const { return 2*(a+b);}
	void setA(){cin>>a;}
	void setB(){cin>>b;}
};

class Circle:public Plane
{
private:
	float a;
public:
	virtual float area() const {return a*a*3.1415926;}
	virtual float girth() const { return 2*a*3.1415926;}
	void setRad(){cin>>a;}
};

class Point
{
private:
    float x;
	float y;
public:
	void setXy(){cin>>x>>y;}
	float getX()const{return x;}
	float getY()const{return y;}
	Point(float input_x,float input_y){x=input_x;y=input_y;}

};

class Triangle:public Plane
{
private:
	Point A;
	Point B;
	Point C;
    
	
public:
	Triangle(float Xa1,float Ya1,float Xb1,float Yb1,float Xc1,float Yc1):A(Xa1,Ya1),B(Xb1,Yb1),C(Xc1,Yc1){}
	Point getA(){return A;}
	Point getB(){return B;}
	Point getC(){return C;}

	 virtual float area()  const { 
		 float Xa;
	float Ya;
    float Xb;
	float Yb;
    float Xc;
	float Yc;
		 Xa=A.getX();
 Ya=A.getY();
     Xb=B.getX();
	 Yb=B.getY();
     Xc=C.getX();
	Yc=C.getY();
	 
    
		return fabs((Xa*Yb+Ya*Xc+Xb*Yc-Xa*Yc-Ya*Xb-Yb*Xc)/2);}
	 virtual float girth() const
	{  float Xa;
	float Ya;
    float Xb;
	float Yb;
    float Xc;
	float Yc;

		 Xa=A.getX();
	 Ya=A.getY();
     Xb=B.getX();
	 Yb=B.getY();
     Xc=C.getX();
	 Yc=C.getY();
		return sqrt((Xa-Xb)*(Xa-Xb)+(Ya-Yb)*(Ya-Yb))+sqrt((Xc-Xb)*(Xc-Xb)+(Yc-Yb)*(Yc-Yb))+sqrt((Xa-Xc)*(Xa-Xc)+(Ya-Yc)*(Ya-Yc));
	 }
};

int main()
{
	Body Cylinder;
	Body RectangularPyramid;
	Body TrianglePrism;
	Circle circle;
    Rectangle rectangle;
	
	cout<<"输入圆柱的半径:";
	circle.setRad();
	cout<<"输入圆柱的高:";
    Cylinder.setHigh();
    Cylinder.setPbasic(circle);
	cout<<"圆柱的体积为:";
    cout<<Cylinder.volume();
	cout<<endl<<"圆柱的表面积为:";
	cout<<Cylinder.surfaceArea();
	cout<<endl<<endl;
	cout<<"输入四棱柱底面的长:";
	rectangle.setA();
    cout<<"输入四棱柱底面的宽:";
	rectangle.setB();
    cout<<"输入四棱柱底面的高:";
    RectangularPyramid.setHigh();
    RectangularPyramid.setPbasic(rectangle);
	cout<<"四棱柱的体积为:";
    cout<<RectangularPyramid.volume();
	cout<<endl<<"四棱柱的表面积为:";
    cout<<RectangularPyramid.surfaceArea();
	cout<<endl<<endl;
	float Xa;
	float Ya;
    float Xb;
	float Yb;
    float Xc;
	float Yc;
	cout<<"输入三棱柱底面顶点A的<x,y>坐标:";
	cin>>Xa>>Ya;
	cout<<"输入三棱柱底面顶点B的<x,y>坐标:";
    cin>>Xb>>Yb;
	cout<<"输入三棱柱底面顶点C的<x,y>坐标:";
	cin>>Xc>>Yc;
    Triangle triangle(Xa,Ya,Xb,Yb,Xc,Yc);
	cout<<"输入三棱柱的高:";
	TrianglePrism.setHigh();
    TrianglePrism.setPbasic(triangle);
	cout<<"三棱柱的体积为:";
	cout<<TrianglePrism.volume();
	cout<<endl<<"三棱柱的表面积为:";
	cout<<TrianglePrism.surfaceArea();
	return 0;






}
