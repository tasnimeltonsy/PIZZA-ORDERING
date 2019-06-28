#include <iostream>
using namespace std;

int main()
{
int itemnum,quantity,optionnum;
float bill,total,price;
string itemsize,option,yon,order;
bill=0, optionnum=0, quantity=0 , total=0 ;
cout<<"Welcome to our Pizza restaurant!" <<endl;
do{
cout<<"Please select one of items"<<endl;
cout<<"1- SUPER SUPREME - S=50 /M=75.5/ L=100"<<endl;
cout<<"2- CHICKEN SUPREME - S=45/ M=73.88/ L=97.99"<<endl;
cout<<"3- MARGHERITA - S=35/ M=70/ L=95"<<endl;
cout<<"4- CHEESE LOVERS - S=60.96/ M=87.75/ L=113.16"<<endl;
cout<<"5- SEA FOOD LOVERS - S= 64.47/ M=94.30/ L=123.25"<<endl;
cin>>itemnum;
switch (itemnum==1)
{
 case 1:
        cout <<"you select SUPER SUPREME "<<endl;
        break;

case 2:

    cout <<"you select CHICKEN SUPREME "<<endl;
    break;

case 3:

    cout <<"you select MARGHERITA "<<endl;
    break;

case 4:

    cout <<"you select CHEESE LOVERS "<<endl;
    break;

case 5:

    cout <<"you select SEA FOOD LOVERS "<<endl;
    break;
}
cout<<"enter the quantity of your pizza !" <<endl;
cin>>quantity;
cout<<"enter the size of your pizza !" <<endl;
cin>>itemsize;

if(itemnum==1)
{
    if(itemsize=="s")
        price=50;
    else if(itemsize=="m")
        price=75.50;
    else if(itemsize=="l")
        price=100;
}
if (itemnum==2)
{
    if (itemsize=="s")
        price=45;
    else if(itemsize=="m")
        price=73.88;
    else  if(itemsize=="l")
        price=97.99;
}
if (itemnum==3)
{
    if (itemsize=="s")
        price=35;
    else if (itemsize=="m")
        price=70;
    else if (itemsize=="l")
        price=95;
}
if(itemnum==4)
{
    if (itemsize=="s")
        price=60.96;
    else if (itemsize=="m")
        price=87.75;
    else if (itemsize=="l")
        price=113.16;

}

if (itemnum==5)
{
    if (itemsize=="s")
        price=64.47;
    else if (itemsize=="m")
        price=94.30;
    else if (itemsize=="l")
        price=123.25;
}

cout<<"Do you want extra topping ?"<<endl;
cin>>yon;
if (yon=="yes")
{
    cout<<"Please select one ( mushroom = 10, onion =5 , sausage =10)"<<endl;
    cin>>option;
    if (option=="mushroom"||option=="sausage")
        optionnum=10;
    else
        optionnum=5;
    //if(option=="sausage")
        //optionnum=10;
}
else
optionnum=0;
total=quantity*(price+optionnum);
bill+=total;
cout<<"do you want another item ?"<<endl;
cin>>order;
}
while(order=="yes");
cout<<"Thank you for using our application your bill = "<<bill<<endl;
return 0;
}
