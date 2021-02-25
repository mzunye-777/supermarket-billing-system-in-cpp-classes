# supermarket-billing-system-in-cpp-classes
#include <iostream>
#include<string.h>
using namespace std;

class product{
	public:
	int pno,quan,g;
	string pname,sname,sdate;
	float pprice,total,change,money;
	void teller();
	void pino();
	void create_product();
	void show_product();
	void owner_ship();
};
void product::owner_ship(){
	cout<<"THIS PROGRAM WAS MADE BY GEOFFREY MULI";
    cout<<"\nUMMA UNIVERSITY,SCHOOL OF BUSINESS AND TECHNOLOGY\n";
}
void product::pino(){
	int pin,x=8;
	while(x!=0){
		cout<<"\nPLEASE ENTER YOUR PIN: ";
		cin>>pin;
		if(pin==1111){
			cout<<"\nCORRECT PIN\n";
			x=0;
		}
		else 
		cout<<"WLONG PIN";
	}
}
void product::teller(){
	cout<<"\nEnter the server's name: ";
	cin>>sname;
	cout<<"\nEnter today's date: ";
	cin>>sdate;
}
void product::create_product(){
	cout<<"\nEnter number of items being bought:";
	cin>>g;
	for(int i=1;i<=g;i++){
	cout<<"\nEnter name of the product: ";
	cin>>pname;
	cout<<"\nenter the product bar code: ";
	cin>>pno;
	cout<<"\nenter the product price: ";
	cin>>pprice;
	total+=pprice;
	}
	cout<<"\nEnter the amount given: ";
	cin>>money;
	change=money-total;
};
void product::show_product(){
	cout<<"\nTHE TOTAL PRICE FOR YOUR ITEMS IS "<<total;
	cout<<"\nTHE BALANCE REMAINING IS "<<change;
	cout<<"\nYOU HAVE BEEN SERVERD BY "<<sname;
	cout<<"\nTHANK YOU FOR CHOOSING MACHO MACHO WE LOVE YOU";
}
int main(){
	cout <<"WELCOME TO MACHO MACHO SUPERMARKET"<<endl;
	product p;
	p.owner_ship();
	system("pause");
	system("cls");
	p.teller();
	p.pino();
	system("pause");
	system("cls");
	p.create_product();
	system("cls");
	p.show_product();
	return 0;
	}
