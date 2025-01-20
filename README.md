# weather-report-usingc-

//Name      :Viraj Jamdhade
//Div       : A
//Roll No.  : 67


#include <iostream>
using namespace std;

class weather

{
 private:

    int day, ht, lt, rain, snow;

 public:

    weather()

    {
        day=0;

        ht=0;

        lt=0;

        rain=0;

        snow=0;

    }

    weather(int a, int b, int c, int d, int e)

    {
        day=a;

        ht=b;

        lt=c;

        rain=d;

        snow=e;
    }

    weather accept(weather&w)

    {
        day=w,day;

        ht=w.ht;

        lt=w.lt;

        rain=w.rain;

        snow=w.snow;

    }


    void accept()

    {

        cout<<"\n Enter the day of month : ";
        cin>>day;

        cout<<"\n Enter High Temperature : ";
        cin>>ht;

        cout<<"\n Enter Low Temperature : ";
        cin>>lt;

        cout<<"\n Enter the rain of the day : ";
        cin>>rain;

        cout<<"\n Enter the snow of the day : ";
        cin>>snow;

       }

};
