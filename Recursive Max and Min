//******Divide and conquer method to recursively implement and to find the maximum and minimum in a given list of n elements********

#include <iostream>
#include <stdlib.h>

using namespace std;

void RecMaxMin(int[],int,int,int*,int*);

int main(int argc, char** argv){
	int Arr[500000], Num, i;
	int Max=0, Min=0;
	
	cout<<"Enter the size of the array: \n";
	cin>>Num;
	cout<<"Enter the elements of the array: \n";
	
	for(i=0; i<Num; i++)
	cin>>Arr[i];
	RecMaxMin(Arr, 0, Num-1, &Max, &Min);
	
	cout<<"\n Max Element = " <<Max<< "\n Min Element = " <<Min<<endl; 
	return 0;
}
	
	//Function for implementing the min and max element using divide and conquer
	
	void RecMaxMin(int a[], int low, int high, int *max, int *min){
		int mid, max1, max2, min1, min2;
			if(high-low==1){
				if(a[low] > a[high]){
					*max = a[low];
					*min = a[high];
				}else{
					*max = a[high];
					*min = a[low];
				}
			}
			else if(low==high){
				*min = *min = a[low];
			}
			else if(low<high){
				mid=(low+high)/2;
					RecMaxMin(a,low,mid,&max1,&min1);
					RecMaxMin(a,mid+1,high,&max2,&min2);
					if(max1 > max2)
						*max = max1;
						else
						*max = max2;
						
					if(min1 < min2)
					*min = min1;
					else
					*min = min2;
			}
}
	

