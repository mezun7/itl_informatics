# C++ vs Python

### [Вывод текста в консоль](#stdout)
####C++:
```
#include <iostream>

using namespace std;

int main() {
    cout << "Hello world" << endl;
}
```
`out: Hello world`

####Python:
```
print("Hello world")
```
`out: Hello world`

---
### [Переменные и арифметические операции с ними. 1](#vars-1)
####C++:
```
#include <iostream>

using namespace std;

int main() {
    int a, b;
    a = 7;
    int c = 5;
    int d = a + c;
    b = a - d;
    b++;
    cout << "a = " << a << "| b = " << b << "| c = " << c << "| d = " << d << endl;
}
```
`out: a = 7 | b = -4 | c = 5 | d = 12`  

####Python:
```
a = 7
c = 5
d = a + c
b = a - d
b += 1
print("a = {} | b = {} | c = {} | d = {}\n".format(a, b, c, d))
```
`out: a = 7 | b = -4 | c = 5 | d = 12`

---
### [Переменные и арифметические операции с ними. 2](#vars-2)
####C++:
```
#include <iostream>
#include <cmath>

using namespace std;

int main() {
    double pi = 3.14, r = 2, s, a;
    s = pi * r * r;
    cout << "s = " << s << endl;
    cout << "sqrt(2) = " << sqrt(2) << endl;
}
```
```
s = 12.56
sqrt(2) = 1.41421
```

####Python:
```
import math
pi = 3.14
r = 2
s = pi * r * r 
print("s = {}".format(s))
print("sqrt(2) = {}".format(math.sqrt(2)))
```
```
s = 12.56
sqrt(2) = 1.4142135623730951
```
---
### [Вывод дробных чисел](#precision)
####C++:
```
#include <iostream>
#include <iomanip>

using namespace std;

int main() {
    cout << fixed << setprecision(9); 
    cout << "1/3 = " << 1.0/3.0 << endl;
}
```
```
1/3 = 0.333333333
```

####Python:
```
print("1/3 = %.9f" % (1/3))
```
```
1/3 = 0.333333333
```
---

### [Ввод из консоли](#stdin)
####C++:
```
#include <iostream>

using namespace std;

int main() {
    int a, b;
    cin >> a >> b;
    cout << "sum = " << a + b << endl;
    cout << "diff = " << a - b << endl;
    cout << "mul = " << a * b << endl;
    cout << "div = " << a / b << endl;
    cout << "mod = " << a % b << endl;
}
```
```
15 6
---
sum = 21
diff = 9
mul = 90
div = 2
mod = 3
```

####Python:
```
a, b = map(int, input().split(' '))
print("sum = %d" % (a + b))
print("diff = %d" % (a - b))
print("mul = %d" % (a * b))
print("div = %d" % (a // b))
print("mod = %d" % (a % b))

```
```
15 6
---
sum = 21
diff = 9
mul = 90
div = 2
mod = 3
```
---
### [Условия](#if)
####C++:
```
#include <iostream>

using namespace std;

int main() {
    int a, b;
    cin >> a >> b;
    
    if (a < b) {
        cout << "b is greater than a" << endl;
    } else if (a > b) {
        cout << "a is greater than b" << endl;
    } else {
        cout << "a is equal to b" << endl;
    }
    
    if (a % 2 == 0 && b % 2 == 0) {
        cout << "a and b are even" << endl;
    } else if (a % 2 != 0 || b % 2 != 0) {
        cout << "a or b is odd" << endl;
    }
}
```
```
15 6
---
a is greater than b
a or b is odd
```

####Python:
```
a, b = map(int, input().split(' '))

if a < b:
    print("b is greater than a")
elif a > b:
    print("a is greater than b")
else:
    print("a is equal to b")

if a % 2 == 0 and b % 2 == 0:
    print("a and b are even")
elif a % 2 != 0 or b % 2 != 0:
    print("a or b is odd")
```
```
15 6
---
a is greater than b
a or b is odd
```
---