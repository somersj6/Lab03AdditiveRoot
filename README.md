# Lab03AdditiveRoot
A lab calculating the additive root and persistence.

#include <iostream>
#include <iomanip>
#include <cmath>
using std::cout;
using std::cin;
using std:: endl;

int addroot(int root)
{
    int digit;
    int addroot;
    addroot = 0;
    while(root>0)
            {
                digit = root%10;
                root = root/10;
                addroot = addroot+digit;
            
            } 
    return addroot;
}
int main()
{
    int num;
    int pers;
    pers = 1;
    int root;
    root = 0;
    int digit;
    digit = 0;

    while (cin>>num && num>0)
    {
       
        root = 0;
        digit = 0;
        pers = 1;
        
            while(num>0)
            {
                digit = num%10;
                num = num/10;
                root = root+digit;
            
            } 
        while (root > 9)
        {
            pers = pers+1;
            root = addroot(root);

        }           
    cout<<"additive root: " << root <<endl;
    cout<<"additive persistence: " << pers << endl;  
    cout<<0100<<endl;
    }
