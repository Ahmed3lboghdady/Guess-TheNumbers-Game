# Guess-TheNumbers-Game
This C++ program is a simple sequence quiz game. The user is prompted to complete three different number sequences by entering the missing number in each. Points are awarded for each correct answer out of a total of three. If the user scores zero points, a "Good luck next time!" message is displayed. The user can choose to retry the quiz or exit.
   
     #include <iostream>
      using namespace std;
  
      int main()
      {
          char choice = 'Y';
          
          do {
              int points = 0;
              int answers[3];
      //Ask the user to enter the missing number
            cout << "Type the missing number " << "\n";
            cout << "Sequence 1" << "\n";
            cout << "1,5,10,16,??" << "\n";
            cin >> answers[0];
    
            cout << "Type the missing number " << "\n";
            cout << "Sequence 2" << "\n";
            cout << "2,4,8,16,??" << "\n";
            cin >> answers[1];
    
            cout << "Type the missing number " << "\n";
            cout << "Sequence 3" << "\n";
            cout << "1,1,2,3,??" << "\n";
            cin >> answers[2];
      //Declare sequences
            int sequance[3][5] = {
                {1, 5, 10, 16, 23},
                {2, 4, 8, 16, 32},
                {1, 1, 2, 3, 5}
            };
      //Check the user's answers
            if (answers[0] == sequance[0][4]) {
                points++;
            }
            if (answers[1] == sequance[1][4]) {
                points++;
            }
            if (answers[2] == sequance[2][4]) {
                points++;
            }
            //total points
            cout << "Your points are: " << points << " from 3\n";
    
            // If points are 0, print "Good luck next time
            if (points == 0) {
                cout << "Good luck next time!\n";
            }
    
            // Ask the user if they want to try again
            cout << "Do you want to try again? (Y for yes / N for no): ";
            cin >> choice;
            cout << "\n";
    
        } while (choice == 'Y' || choice == 'y');
    
        return 0;
      }
