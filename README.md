//Name      :Viraj Jamdhade
//Div       : A
//Roll No.  : 67


//create a class of weather using a different constructor


#include<iostream>
using namespace std;

class Weather
{
private:
    int day,ht,lt,rain,snow;
public:
Weather()
{

    day=0;
    ht=0;
    lt=0;
    rain=0;
    snow=0;
}
Weather(int a, int b, int c, int d, int e)
{
    day=a;
    ht=b;
    lt=c;
    rain=d;
    snow=e;
}
Weather(Weather &w)
{

    day=w.day;
    ht=w.ht;
    lt=w.lt;
    rain=w.rain;
    snow=w.snow;
}
void accept()
{
    cout<<"\nEnter the day of month   : ";
    cin>>day;
    cout<<"Enter high temperature     : ";
    cin>>ht;
    cout<<"Enter low temperature      : ";
    cin>>lt;
    cout<<"Enter the rain of the day  : ";
    cin>>rain;
    cout<<"Enter the snow of the day  : ";
    cin>>snow;
 }
void display()
{

    cout<<"\n"<<day<<"\t"<<ht<<"\t"<<lt<<"\t"<<rain<<"\t"<<snow;

}
void average(Weather w4[31],int n)
{
    int sumht=0,sumlt=0, sumrain=0,sumsnow=0;
    int alt,aht,arain,asnow;
    for(int i=0;i<n;i++)
    {
        sumht=sumht+w4[i].ht;
        sumlt=sumlt+w4[i].lt;
        sumrain=sumrain+w4[i].rain;
        sumsnow=sumsnow+w4[i].snow;
    }
    alt=sumlt/n;
    aht=sumht/n;
    arain=sumrain/n;
    asnow=sumsnow/n;
    cout<<"\nAverage of rain        : "<<arain;
    cout<<"\nAverage of snow        : "<<asnow;
    cout<<"\nAverage of high temp   : "<<aht;
    cout<<"\nAverage of low temp    : "<<alt;
}

};
int main()
{
    int ch, n=0, i;
    Weather wl;
    wl.display();
    Weather w2(1,2,3,4,5);
    w2.display();
    Weather w3(w2);
    w3.display();
    Weather w4[31];
    Weather w5;
    do
    {
        cout<<"\n\n ****** Programmed by Viraj Jamdhade ****** \n\n";
        cout<<"\nEnter choice : ";
        cout<<"\n1.Accept"<<"\n2.Display"<<"\n3.Average"<<"\n4.EXIT \n\n";
        cin>>ch;
        switch(ch)
        {

        case 1:
            cout<<"\nEnter the number of the day : ";
            cin>>n;
            cout<<"\n\n====== Enter the data ===== \n";
            for(int i=0;i<n;i++)
            {

                w4[i].accept();
            }
            break;
        case 2:
            cout<<"\nday"<<"\t"<<"ht"<<"\t"<<"lt"<<"\t"<<"rain"<<"\t"<<"snow";
            for(int i=0;i<n;i++)
            {
                w4[i].display();
            }
            break;
        case 3:
            w5.average(w4,n);
            break;
        }
    }
    while(ch!=3);
return 0;

}
