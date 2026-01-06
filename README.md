# Unique-number | C++
This program Gives the unique number entered in an integer type array

// Online C++ compiler to run C++ program online
#include <iostream>
using namespace std;

int main() {
    int m = 0, unq, count = 0, n = 5, chalak = 0;
    
    cout << "Enter the number of elements : " ;
    cin >> n;
    
    int arr[n];
    
    cout << "Enter " << n << " elements : ";
    for(int i = 0; i < n; i++){
        cin >> arr[i];
    }
    for(int i = 0; i < n; i++){
        cout << arr[i] << ' ';
    }cout << endl;    
    
    for(int i = 0; i < n; i++){
        count = 0;
        for(int j = 0; j < n; j++){
            if(i != j){
                if(arr[i] == arr[j]){
                    count++;
                }
            }
            
        }
        if(count == 0){
            if(m == 0){
                cout << "Unique vaulue(s) are : ";
            }
            cout << arr[i] << ' ';
            m++;
            chalak++;
        }
    }
    if(chalak < 1){
        cout << "No unique values \n";
    }
    
    return 0;
}
