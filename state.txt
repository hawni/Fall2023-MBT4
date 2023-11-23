#include <iostream>
#include <random>
#include <ctime>
#include <cmath>
#include <string>
#include <fstream>

using namespace std;
class state_machine
{
    public:
    void sm_1();
    void sm_2();
    void sm_3();
    void sm_4();
    // int menu();
    // void bye();
};
// /////////////////

void state_machine::sm_4()
{
    bool b = true;
    char ans;
    string letter;
    ofstream file("example.txt");
    cout << "*****you made a file !*****" << endl;
    while(b){
        if (file.is_open()) {
            cout << "write : " << endl;
            cin >> letter;
            file << letter << endl;
            }
        cin.get();
        cout << "do you wan to add another word to your file ?(y/n) " << endl;
        // system("pause");
        cin >> ans;
        if (ans == 'N' || ans == 'n')
            b = false;
        else
            continue;
    }
    file.close();
}


void state_machine::sm_3()
{
    double d;
    cout << "enter a number: ";
    cin >> d;
    cout << endl;
    cout << "pow 2: " << pow(d, 2) << endl;  // tavan 2 add
    cout << "sqr: " << sqrt(d) << endl;  // rishe add jazr
    cout << "log: " << log(d) << endl;   //logaritm add
    cout << "abs: " << abs(d) << endl;  //gadr motlag
    cout << "round: " << round(d) << endl;  //rond

}











void state_machine::sm_2()
{
       default_random_engine randomGenerator(time(0));
        randomGenerator.seed(time(0));
        uniform_int_distribution<int> diceRo11(1, 6);
        
        cout << "your dice number:" << diceRo11(randomGenerator) << endl;

}
// ///////

void state_machine::sm_1()
{
    cout << " _" << endl;
    cout << "( \\" << endl;
    cout << ") )" << endl;
    cout << "( ( .-------.    A.-.A" << endl;
    cout << "\\ \\/          \\/  , , \\" << endl;
    cout << " \\  \\         =|   t  /=" << endl;
    cout << "  \\  |----.      ----" << endl;
    cout << "  / //     | ||" << endl;
    cout << " /_,))     |_,))" << endl;
    cout << "_" << endl;
    cout << "_" << endl;

}


// void state_machine::bye()
// {
//     cout << " ___  ___" << endl;
//     cout << "/   \\/   \\" << endl;
//     cout << "\\        /" << endl;
//     cout << " \\      /" << endl;
//     cout << "  \\    /" << endl;
//     cout << "   \\  /" << endl;
//     cout << "    \\/" << endl;
// }




int main()
{

    int a=1, b=1;
    state_machine s;

// /////////
    while (1){
    cout << endl;
    cout << "****some point :****" << endl;
    cout << "1)enter a number from 1 to 4" << endl << "2) num '5' -> exit !" << endl;
    cout << "3)now we are in state 1" << endl << "4)try your chence :" << endl;
    cin >> a;
    cout << endl;
        if((b-1 == a || b+1 == a) || b == a){
            b = a;
            switch (a){
            case 1:
                cout << "num1:" << endl;
                s.sm_1();
                break;
            case 2:
                cout << "num2:" << endl << endl;
                s.sm_2();
                break;
            case 3:
                cout << "num3:" << endl;
                s.sm_3();
                break;
            case 4:
                s.sm_4();
                
                break;
            case 5:
                exit(1);
            default:
                cout << "YOUR RUNG!!!" << endl << "try again :" << endl << endl;
                break;
            }
        }
        else
            {cout << "ERROR! -> MOVEMENT IN DIAMETER! " << endl;}
    }
}


//     vector<int> v;
//     v.push_back(a);
// if(c>0){
//         if(v.at(i-1)% 2 == 0 && a == 2 || a == 4){
//             cout << "you can NOT move on the diameter!" << endl;
//             }
//         else
//             return a;
//         }

