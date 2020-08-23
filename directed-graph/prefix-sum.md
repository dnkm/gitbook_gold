# Prefix Sum

## 2D Grid

```cpp
// range query
// ranged sum -- prefixsum
// ranged minimum
// binary indexed tree (Fenwick)
// segment tree

#include <bits/stdc++.h>

using namespace std;

int ar[4][4] = {
    {1, 2, 4, 1},
    {3, 5, 4, 2},
    {2, 2, 2, 2},
    {2, 2, 2, 2}
};
int ps[4][4];

void buildPS() {
    // row 0
    ps[0][0] = ar[0][0];
    for(int c = 1; c < 4; c++) {
        ps[0][c] = ps[0][c-1] + ar[0][c];
    }
    
    // rows 1 ~ N
    for(int r = 1; r < 4; r++) {
        ps[r][0] = ps[r-1][0] + ar[r][0];
        for(int c = 1; c < 4; c++) {
            ps[r][c] = ps[r-1][c] + ps[r][c-1] - ps[r-1][c-1] + ar[r][c];
        }
    }
    
    // printing
    for(int r = 0; r < 4; r++) {
        for(int c = 0; c < 4; c++) {
            cout << ps[r][c] << " ";
        }
        cout << "\n";
    }
}

int sum(int x, int y, int xx, int yy) {
    return ps[][] - ps[][] - ps[][] + ps[][];
}

int main() {
    buildPS();
    
    cout << sum(1, 1, 2, 2);        // (2,2) ~ (1,1) inclusive
}




















```

