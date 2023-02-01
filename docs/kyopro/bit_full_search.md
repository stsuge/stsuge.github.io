# bit全探索
1つの桁が2値で表されるようなシーケンスの全パターン列挙する際に使用できる。
言い換えると、{0, 1, ... n - 1}の部分集合 ({}, {0}, {1}, ... , {0, 1}, {0, 2}, ... {0, 1, ... , n - 1})について全探索を行うことができる。
※単純なn重ループで書くことも可能だが、再起などを使用する必要があるため多少手間がかかる。

```
#include "bits/stdc++.h"
using namespace std;
typedef long long ll;

int main() {
    // 桁数
    ll n = 4;

    // {0, 1, ... n - 1}の部分集合について全探索
    for (ll i = 0; i < (1 << n); i++) {
        // LSB（最下位ビット）からの探索
        for (ll j = 0; j < n; j++) {
            if (j & (1 << j)) {
                // 1が立っている桁に対しての処理
            }
        }

        // MSB（最上位ビット）からの探索
        for (ll j = n - 1; j >= 0; j--) {
            if (j & (1 << j)) {
                // 1が立っている桁に対しての処理
            }
        }
    }
}
```

参考：
[競プロ典型 90 問 002 - Encyclopedia of Parentheses（★3）](https://atcoder.jp/contests/typical90/tasks/typical90_b)
[ビット全探索（ 2^n 通りの全探索）](https://algo-logic.info/rec-bit-search/)
