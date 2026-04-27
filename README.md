[Program-1 Wap for addition, sub ,mul, div using object and classes.](#Assignment-1)

[Program-2 Write a class for addition of two distance where each distance is given in m,cm,mm.](#Assignment-2)

[Program-3 Similarly, test the result by creation of object in main class where each distance is given in m,cm.](#Assignment-3)

[Program-4 Similarly for time given in hours, min and seconds.](#Assignment-4)

[Program-5 Time given in hours and minutes.](#Assignment-5) 

[Program-6 Collect the code from internet for any five programs of c language. (Fact, armstrong, palindrome, Fibonacci, pattern)](#Assignment-6) 

[Program-7 Write a class that is having four method for 1-dimensional array. (Input, output 1,out2, reverse).](#Assignment-7)

[Program-8 write a class with multiple methods to perform matrix operations (transpose, addition, sum of rows, sum of columns, sum of diagonal).](#Assignment-8)

## Assignment-1
```
public class Arithmetic {
    public static void main(String args[]) {

        Calculate obj = new Calculate();

        obj.input(20,10);

        obj.add();
        obj.sub();
        obj.mul();
        obj.div();
    }
}
class Calculate {
    int a, b;

    void input(int x, int y) {
        a = x;
        b = y;
    }

    void add() {
        System.out.println("Addition = " + (a + b));
    }

    void sub() {
        System.out.println("Subtraction = " + (a - b));
    }

    void mul() {
        System.out.println("Multiplication = " + (a * b));
    }

    void div() {
        System.out.println("Division = " + (a / b));
    }
}
```


Output:
<img width="357" height="146" alt="Screenshot 2026-04-28 002737" src="https://github.com/user-attachments/assets/993534ec-4d89-4c2d-89d0-86e9437e2506" />

## Assignment-2
```
class Distance {
    int meter;
    int centimeter;
    int millimeter;

    Distance(int m, int cm, int mm) {
        meter = m;
        centimeter = cm;
        millimeter = mm;
    }

    Distance add(Distance d) {
        int m = this.meter + d.meter;
        int cm = this.centimeter + d.centimeter;
        int mm = this.millimeter + d.millimeter;

        cm += mm / 10;
        mm = mm % 10;

        m += cm / 100;
        cm = cm % 100;

        return new Distance(m, cm, mm);
    }

    void display() {
        System.out.println(meter + " m " + centimeter + " cm " + millimeter + " mm");
    }

    public static void main(String[] args) {
        Distance d1 = new Distance(2, 50, 8);
        Distance d2 = new Distance(3, 75, 7);

        Distance result = d1.add(d2);

        System.out.print("Result: ");
        result.display();
    }
}
```

Output:
<img width="286" height="52" alt="Screenshot 2026-04-28 003637" src="https://github.com/user-attachments/assets/2a91dd37-8029-4367-b49a-87b38773cfdf" />

## Assignment-3
```
public class MainClass {
    public static void main(String[] args) {

        Distance d1 = new Distance(3, 80);
        Distance d2 = new Distance(2, 50);

        Distance result = d1.add(d2);

        System.out.print("Result: ");
        result.display();
    }
}
class Distance {
    int meter;
    int centimeter;

    Distance(int m, int cm) {
        meter = m;
        centimeter = cm;
    }

    Distance add(Distance d) {
        int m = this.meter + d.meter;
        int cm = this.centimeter + d.centimeter;

        m += cm / 100;
        cm = cm % 100;

        return new Distance(m, cm);
    }

    void display() {
        System.out.println(meter + " m " + centimeter + " cm");
    }
}
```

Output:
<img width="232" height="54" alt="Screenshot 2026-04-28 004423" src="https://github.com/user-attachments/assets/dbd05878-0d2b-479a-b729-9dd3e207b346" />

## Assignment-4
```

public class MainClass {
    public static void main(String[] args) {

        Time t1 = new Time(2, 45, 50);
        Time t2 = new Time(3, 30, 20);

        Time result = t1.add(t2);

        System.out.print("Result: ");
        result.display();
    }
}
class Time {
    int hour;
    int minute;
    int second;

    Time(int h, int m, int s) {
        hour = h;
        minute = m;
        second = s;
    }

    Time add(Time t) {
        int h = this.hour + t.hour;
        int m = this.minute + t.minute;
        int s = this.second + t.second;

        m += s / 60;
        s = s % 60;

        h += m / 60;
        m = m % 60;

        return new Time(h, m, s);
    }

    void display() {
        System.out.println(hour + " hr " + minute + " min " + second + " sec");
    }
}
```

Output:
<img width="337" height="49" alt="Screenshot 2026-04-28 004801" src="https://github.com/user-attachments/assets/ab12146c-356d-4857-a526-dc58946d87f4" />


## Assignment-5
```
public class MainClass {
    public static void main(String[] args) {
        Time t1 = new Time(5, 40);
        Time t2 = new Time(3, 35);

        Time result = t1.add(t2);

        System.out.print("Result: ");
        result.display();
    }
}

class Time {
    int hour;
    int minute;

    Time(int h, int m) {
        hour = h;
        minute = m;
    }

    Time add(Time t) {
        int h = this.hour + t.hour;
        int m = this.minute + t.minute;

        h += m / 60;
        m = m % 60;

        return new Time(h, m);
    }

    void display() {
        System.out.println(hour + " hr " + minute + " min");
    }
}
```

Output:
<img width="302" height="60" alt="Screenshot 2026-04-28 005057" src="https://github.com/user-attachments/assets/ef2e84b8-a737-4e0e-a36b-b8311d7f3da0" />

## Assignment-6
```
class Factorial {
    public static void main(String[] args) {
        int n = 5;
        int fact = 1;

        for (int i = 1; i <= n; i++) {
            fact *= i;
        }

        System.out.println("Factorial = " + fact);
    }
}
```

Output:
<img width="223" height="51" alt="Screenshot 2026-04-28 005349" src="https://github.com/user-attachments/assets/9eea3ae0-fcfb-406f-a7b5-523eb3e692d1" />

```
class Armstrong {
    public static void main(String[] args) {
        int n = 153, temp, sum = 0, r;

        temp = n;

        while (n > 0) {
            r = n % 10;
            sum += r * r * r;
            n = n / 10;
        }

        if (temp == sum)
            System.out.println("Armstrong Number");
        else
            System.out.println("Not Armstrong");
    }
}
```

Output:
<img width="240" height="49" alt="image" src="https://github.com/user-attachments/assets/709344c7-c47d-4605-8e8e-728e1c49d359" />

```
class Palindrome {
    public static void main(String[] args) {
        int n = 121, rev = 0, r, temp;

        temp = n;

        while (n > 0) {
            r = n % 10;
            rev = rev * 10 + r;
            n = n / 10;
        }

        if (temp == rev)
            System.out.println("Palindrome");
        else
            System.out.println("Not Palindrome");
    }
}
```

Output:
<img width="165" height="38" alt="image" src="https://github.com/user-attachments/assets/b83448f7-e13c-4b01-a89f-8a2ad2003468" />

```
class Fibonacci {
    public static void main(String[] args) {
        int n = 10;
        int a = 0, b = 1, c;

        System.out.print(a + " " + b + " ");

        for (int i = 2; i < n; i++) {
            c = a + b;
            System.out.print(c + " ");
            a = b;
            b = c;
        }
    }
}
```

Output:
<img width="400" height="52" alt="image" src="https://github.com/user-attachments/assets/4888c85b-019e-4796-b1ee-2f705d73c6bb" />

```
class Pattern {
    public static void main(String[] args) {
        int n = 5;

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

Output:
<img width="139" height="165" alt="image" src="https://github.com/user-attachments/assets/eebe8ddc-2352-4cec-98a6-5dcf156de3bc" />

## Assignment-7
```
import java.util.Scanner;

public class MainClass {
    public static void main(String[] args) {
        Array1D obj = new Array1D();

        obj.input();

        obj.output1();
        obj.output2();
        obj.reverse();
    }
}

class Array1D {
    int arr[];
    int n;

    void input() {
        Scanner sc = new Scanner(System.in);
        n = sc.nextInt();
        arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
    }

    void output1() {
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    void output2() {
        for (int i = 0; i < n; i++) {
            if (arr[i] % 2 == 0)
                System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    void reverse() {
        for (int i = n - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }
}
```

Output:
<img width="143" height="161" alt="image" src="https://github.com/user-attachments/assets/3fdc4667-336b-44c3-b7f2-73df4d900eda" />
