#include <iostream>
using namespace std;

int main() {

    int a;

    int b;
    int c;

    int d;
    int e;

    int arr[10][6] = {0};

    int row, col;
    col = sizeof(arr[0]) / sizeof(arr[0][0]);
    row = (sizeof(arr)/col) / sizeof(arr[0][0]);

    int y;

    int q;
    int w;
    int s;
    int f;


    
    
    cout << "**영화 예약 시스템**" << endl;

    cout << "1. 좌석 예약" << endl;
    cout << "2. 예약 변경" << endl;
    cout << "3. 프로그램 종료" << endl;

    cout << "번호를 입력하세요  : ";
    cin >> a;

    if (a == 1) {
    
    cout << "1 2 3 4 5 6 " << endl;
    cout << "------------" << endl;
    cout << '\n';


    for (int i = 0; i < row; i++) {
        for (int j = 0; j < col; j++) {
            cout << arr[i][j] << ' ';

        }
        cout << endl;
    }
    arr[d-1][e-1] = 1;


    cout << '\n';

    cout << "성인(14000원) : ";
    cin >> b;

    cout << '\n';

    cout << "청소년(11000원) : ";
    cin >> c;
    cout << endl;

    for (int r = 0; r < b+c; ++r)
    {
        cout << "몇 열, 몇번째 좌석을 예약하시겠습니다?" << endl;

        cin >> d;
        cin >> e;

        if (d < 10 && e < 6) { 
    
            if (arr[d-1][e-1] == 0) {
                cout << endl << "예약되었습니다." << endl << endl;
                arr[d-1][e-1] = 1;
            }

            else { 
                cout << "이미 예약되었습니다. 다른 자리를 선택하세요." << endl << endl;
                --r;
            }

        }
         else {
            cout << "예약 가능한 좌석이 아닙니다." << endl << endl;
            --r;
        } 
    
    }

    cout << "1 2 3 4 5 6" << endl;
    cout << "-----------" << endl;
    cout << '\n';

    arr[10][6] = {0};
    
    for (int i = 0; i < row; i++) {
        for (int j = 0; j < col; j++) {
            cout << arr[i][j] << ' ';
    
        }
        cout << endl;
    }
    arr[d-1][e-1] = 1;
    cout << endl << endl;

    cout << "**영화 예약 시스템**" << endl;

    cout << "1. 좌석 예약" << endl;
    cout << "2. 예약 변경" << endl;
    cout << "3. 프로그램 종료" << endl;

    cout << "번호를 입력하세요  : ";
    cin >> a;
 
    }

    else if (a == 2) {

    cout << "1 2 3 4 5 6" << endl;
    cout << "-----------" << endl;
    cout << '\n';


    for (int i = 0; i < row; i++) {
        for (int j = 0; j < col; j++) {
            cout << arr[i][j] << ' ';
    
        }
        cout << endl;
    }
    arr[d-1][e-1] = 1;

    cout << "바꿀 좌석의 갯수를 입력하세요 : ";
    cin >> y;

    for(int z = 0; z < y; ++z) {

         cout << "현재 좌석과 바꿀 좌석을 입력하세요." << endl;
         cout << "현재 좌석(N열, M번째) : ";

         cin >> q;
         cin >> w;

         cout << "변경 좌석(n열, m번째) : ";

         cin >> s;
         cin >> f;

        if (s < 10 && f < 6) {
            
            if (arr[d-1][e-1] == 0) {
                cout << "변경되었습니다." << endl;
            }
            else {
                cout << "이미 예약되었습니다. 다른 자리를 선택하세요." << endl;
                --z;
            }
    
        }

        else { 
            cout << "예약 불가 좌석입니다. 다른 자리를 선택하세요." << endl;
            --z;
        }

        }


    cout << "1 2 3 4 5 6" << endl;
    cout << "-----------" << endl;
    cout << '\n';


    for (int i = 0; i < row; i++) {
        for (int j = 0; j < col; j++) {
            cout << arr[i][j] << ' ';
    
        }
        cout << endl;
    }
    arr[d-1][e-1] = 1;
    cout << endl << endl;


    }
    
    else if(a == 3) { 
        cout << "총 " << b*14000 + c*11000 << "원 입니다." << endl;
    }

else {
    cout << "올바른 숫자를 입력해주세요" << endl << endl;
}

}
