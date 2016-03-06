#include<iostream>
#include<fstream>
#include<cmath>
#include<iomanip>
using namespace std;
int main()
{
   ifstream file; // file is a variable of ifstream
   string FileName; // string to get input from the user
        double x, y;
        string a;
cout << "Enter the input filename "; // reading file name from user
cin >> FileName;
file.open(FileName.c_str()); //open the input file given as input
// reading from file data to array a;
   cout<<endl;
while(!file.eof()) //until the file is empty
{
file>>a;
cout<<a<<" ";
file>>x>>y;
cout<<fixed;
double percent=(x/y)*100;
cout<<setprecision(0)<<round(percent)<<"% "<<setprecision(5)<<" "<<percent/100;
if(percent>=(double)90)
cout<<" Excellent\n\n";
if(percent>=(double)80&&percent<(double)90)
    cout<<" Well Done\n\n";
if(percent>=(double)70&&percent<(double)80)
cout<<" Good\n\n";
if(percent>=(double)60&&percent<(double)70)
cout<<" Need Improvement\n\n";
if(percent<(double)60)
cout<<" Fail\n\n";

}
  
       return 0;
}
