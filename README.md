#include <iostream>
using namespace std;
int main(){
	int n;
	cout<<"Zehmet olmasa arrayin olcusunu daxil edin: ";
	cin>>n;
	int arr[n];
	for(int i=0; i<n; i++){
		cin>>arr[i];
	}
	int bolunme;
	cout<<"Zehmet olmasa arrayin bolunme derecesini yazin \n";
	cin>>bolunme;
	int newSize;
	newSize=((n+bolunme-1)/bolunme)*bolunme;
	int newArr[newSize];
	
	for(int i=0; i<newSize; i++){
		if(i<n){
		newArr[i]=arr[i];
	}
	else{
		newArr[i]=0;
	}
	}
	for(int i=0; i<newSize; i++){
		cout<<newArr[i] << " ";
		if((i+1)%bolunme==0){
			cout<<endl;
		}	
	}
	return 0;
}
