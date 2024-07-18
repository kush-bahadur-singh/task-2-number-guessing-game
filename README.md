# task-2-number-guessing-game
#include <iostream>
#include <cstdlib> 
#include <ctime>
using namespace std;
int main() {
srand(static_cast<unsigned int>(time(0))); 
cout<<"Enter the range of picup a random value ";
int range;
cin>>range;
int ran_no = rand() % range + 1; 
int find;
int count = 0;
cout << "find the number between 1 and "<<range<<" :";

    do {
        cin >> find;
        count++;

        if (find < ran_no) {
            cout << "It is low value! Try again: ";
        } else if (find > ran_no) {
            cout << "It is hihg value! Try again: ";
        } else {
            cout << "good you can find the random number" << ran_no << " in " << count << " attempts." << endl;
        }
    } while (find != ran_no);

    return 0;}
