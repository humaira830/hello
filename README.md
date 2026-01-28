//QUESTION NO 1::
 #include <iostream>
 using namespace std;

 int main()
 {

 int num=1;
 while (num<=10 )
 {
 cout << num << " ";
 num++;
 }  cout << endl; 
return 0;
 } 
 ..............................................
 QUESTION NO 2::
 #include <iostream>
using namespace std;

int main() {
    int n = 5;

    // 1. Square Star Pattern
    cout << "1. Square Star Pattern\n";
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= n; j++) {
            cout << "* ";
        }
        cout << endl;
    }

    cout << endl;

    // 2. Right Angle Triangle
    cout << "2. Right Angle Triangle\n";
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= i; j++) {
            cout << "* ";
        }
        cout << endl;
    }

    cout << endl;

    // 3. Inverted Right Angle Triangle
    cout << "3. Inverted Right Angle Triangle\n";
    for(int i = n; i >= 1; i--) {
        for(int j = 1; j <= i; j++) {
            cout << "* ";
        }
        cout << endl;
    }

    cout << endl;

    // 4. Number Pattern
    cout << "4. Number Pattern\n";
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= i; j++) {
            cout << j << " ";
        }
        cout << endl;
    }

    cout << endl;

    // 5. Same Number Pattern
    cout << "5. Same Number Pattern\n";
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= i; j++) {
            cout << i << " ";
        }
        cout << endl;
    }

    return 0;
}
............OUTPUT(EXAMPLES)...........
* * * * *
* * * * *
* * * * *
* * * * *
* * * * *

*
* *
* * *
* * * *
* * * * *

* * * * *
* * * *
* * *
* *
*

1
1 2
1 2 3
1 2 3 4
1 2 3 4 5

1
2 2
3 3 3
4 4 4 4
5 5 5 5 5

...............................................................
QUESTION NO 3::
#include <iostream>
using namespace std;

int main() {
    int n = 5;

    // 1. Full Pyramid
    cout << "1. Full Pyramid\n";
    for(int i = 1; i <= n; i++) {
        for(int s = n; s > i; s--)
            cout << " ";
        for(int j = 1; j <= (2*i-1); j++)
            cout << "*";
        cout << endl;
    }

    cout << endl;

    // 2. Inverted Full Pyramid
    cout << "2. Inverted Full Pyramid\n";
    for(int i = n; i >= 1; i--) {
        for(int s = n; s > i; s--)
            cout << " ";
        for(int j = 1; j <= (2*i-1); j++)
            cout << "*";
        cout << endl;
    }

    cout << endl;

    // 3. Diamond Pattern
    cout << "3. Diamond Pattern\n";
    for(int i = 1; i <= n; i++) {
        for(int s = n; s > i; s--)
            cout << " ";
        for(int j = 1; j <= (2*i-1); j++)
            cout << "*";
        cout << endl;
    }
    for(int i = n-1; i >= 1; i--) {
        for(int s = n; s > i; s--)
            cout << " ";
        for(int j = 1; j <= (2*i-1); j++)
            cout << "*";
        cout << endl;
    }

    cout << endl;

    // 4. Hollow Square
    cout << "4. Hollow Square\n";
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= n; j++) {
            if(i == 1 || i == n || j == 1 || j == n)
                cout << "* ";
            else
                cout << "  ";
        }
        cout << endl;
    }

    cout << endl;

    // 5. Pascal's Triangle
    cout << "5. Pascal's Triangle\n";
    for(int i = 0; i < n; i++) {
        int num = 1;
        for(int s = 1; s <= n-i; s++)
            cout << " ";
        for(int j = 0; j <= i; j++) {
            cout << num << " ";
            num = num * (i - j) / (j + 1);
        }
        cout << endl;
    }

    return 0;
}
.........OUTPUT(EXAMPLES)......
    *
   ***
  *****
 *******
*********


*********
 *******
  *****
   ***
    *


    *
   ***
  *****
 *******
*********
 *******
  *****
   ***
    *



* * * * * 
*       * 
*       * 
*       * 
* * * * * 





     1
    1 1
   1 2 1
  1 3 3 1
 1 4 6 4 1
..............................................................
QUESTION NO 3::ARRAYS(1D AND 2D)
1..#include <iostream>
using namespace std;

int main() {
    int n, a[100];
    cout << "Enter size: ";
    cin >> n;

    cout << "Enter elements:\n";
    for(int i = 0; i < n; i++)
        cin >> a[i];

    cout << "Array elements:\n";
    for(int i = 0; i < n; i++)
        cout << a[i] << " ";

    return 0;
}
OUTPOUT::5
10 20 30 40 50
       ..................
2..  #include <iostream>
using namespace std;

int main() {
    int n, a[100], sum = 0;
    cin >> n;

    for(int i = 0; i < n; i++) {
        cin >> a[i];
        sum += a[i];
    }

    cout << "Sum = " << sum;
    return 0;
}
INPUT::5
1 2 3 4 5
OUTPUT::Sum = 15
       .....................
3..#include <iostream>
using namespace std;

int main() {
    int n, a[100];
    cin >> n;

    for(int i = 0; i < n; i++)
        cin >> a[i];

    int max = a[0];
    for(int i = 1; i < n; i++)
        if(a[i] > max)
            max = a[i];

    cout << "Largest = " << max;
    return 0;
}
INPUT::5
12 45 7 89 23
OUTPUT::Largest = 89
              .......................
4..#include <iostream>
using namespace std;

int main() {
    int n, a[100];
    cin >> n;

    for(int i = 0; i < n; i++)
        cin >> a[i];

    cout << "Reversed array:\n";
    for(int i = n-1; i >= 0; i--)
        cout << a[i] << " ";

    return 0;
}
INPUT::5
1 2 3 4 5
OUTPUT::Reversed array:
5 4 3 2 1
      ................................
5..#include <iostream>
using namespace std;

int main() {
    int r, c, a[10][10];
    cin >> r >> c;

    for(int i = 0; i < r; i++)
        for(int j = 0; j < c; j++)
            cin >> a[i][j];

    cout << "Matrix:\n";
    for(int i = 0; i < r; i++) {
        for(int j = 0; j < c; j++)
            cout << a[i][j] << " ";
        cout << endl;
    }
    return 0;
}
INPUT::2 3
1 2 3
4 5 6
OUTPUT::Matrix:
1 2 3
4 5 6
   ...................................
6..#include <iostream>
using namespace std;

int main() {
    int r, c, a[10][10], sum = 0;
    cin >> r >> c;

    for(int i = 0; i < r; i++)
        for(int j = 0; j < c; j++) {
            cin >> a[i][j];
            sum += a[i][j];
        }

    cout << "Sum = " << sum;
    return 0;
}
INPUT::2 2
1 2
3 4
OUTPUT::Sum = 10
   ..........................................
7..#include <iostream>
using namespace std;

int main() {
    int r, c;
    int a[10][10], b[10][10], sum[10][10];

    cin >> r >> c;

    for(int i = 0; i < r; i++)
        for(int j = 0; j < c; j++)
            cin >> a[i][j];

    for(int i = 0; i < r; i++)
        for(int j = 0; j < c; j++)
            cin >> b[i][j];

    for(int i = 0; i < r; i++)
        for(int j = 0; j < c; j++)
            sum[i][j] = a[i][j] + b[i][j];

    cout << "Sum Matrix:\n";
    for(int i = 0; i < r; i++) {
        for(int j = 0; j < c; j++)
            cout << sum[i][j] << " ";
        cout << endl;
    }

    return 0;
}
INPUT::2 2
1 2
3 4
5 6
7 8
OUPUT::Sum Matrix:
6 8
10 12
  ...............................
8..#include <iostream>
using namespace std;

int main() {
    int r, c, a[10][10];
    cin >> r >> c;

    for(int i = 0; i < r; i++)
        for(int j = 0; j < c; j++)
            cin >> a[i][j];

    cout << "Transpose:\n";
    for(int j = 0; j < c; j++) {
        for(int i = 0; i < r; i++)
            cout << a[i][j] << " ";
        cout << endl;
    }

    return 0;
}
INPUT::2 3
1 2 3
4 5 6
OUTPUT::Transpose:
1 4
2 5
3 6
  ....................
9..#include <iostream>

using namespace std;

int main() {
    int scores[] = {85, 92, 78, 96, 88}; 
    int size = sizeof(scores) / sizeof(scores[0]); 
    int sum = 0;
    double average;
    for (int i = 0; i < size; i++) {
        sum += scores[i]; // sum = sum + scores[i];
    
    average = static_cast<double>(sum) / size; 

    cout << "Total sum: " << sum << endl;
    cout << "Average score: " << average << endl;

    return 0;
} 
OUTPUT::Total sum: 439
Average score: 87.8
      ....................................
