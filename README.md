#include<iostream>
using namespace std;
template<class T>
class bubble
{
 public:
 T a[5],temp;
int index,min,n,i,j,t,count,p,count1,count2,t1;
 bubble()
 {
  count=0;
 // count1=0;
 }
 void get()
 {
  cout<<"\nEnter the array elements\n";
  for(i=0;i<5;i++)
  {
   cin>>a[i];
  }
 }
 void put()
 {
  for(i=0;i<5;i++)
  {
   cout<<"\n"<<a[i];
 }


 }
 void bubblesort()
 {
   for(i=0;i<5;i++)
   {
    for(j=0;j<4-i;j++)
    {
      count++;
       if(a[j]>a[j+1])
      {
        t=a[j];
        a[j]=a[j+1];
        a[j+1]=t;
      }
    }
  }
cout<<"Count="<<count;
}
void insertionsort()
{
        count1=0;
  for(p=1;p<5;p++)
  {
   temp=a[p];
   for(j=p;j>0&&a[j-1]>temp;j--)
   {
    count1++;
    a[j]=a[j-1];
   }
  a[j]=temp;
   put();
 }
cout<<"Count1="<<count1;
}
        void selectionsort()
         {
            count2=0;
           for(j=0;j<5;j++)
            {
              min=a[j],index=j;
              for(i=j+1;i<5;i++)
               {
                 count2++;
                 if(a[i]<min)
                 {
                  min=a[i];
                   index=i;
                 }
               }
               t1=a[j];
               a[j]=a[index];
               a[index]=t1;
}
cout<<"Count2="<<count2;
}
 };
main()
{

 bubble<int>b;
 b.get();
 b.bubblesort();
 b.put();
 b.get();
 b.insertionsort();
 b.put();
 b.get();
 b.selectionsort();
 b.put();
}




