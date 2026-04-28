[Program-1 Wap for addition, sub ,mul, div using object and classes.](#Assignment-1)

[Program-2 Write a class for addition of two distance where each distance is given in m,cm,mm.](#Assignment-2)

[Program-3 Similarly, test the result by creation of object in main class where each distance is given in m,cm.](#Assignment-3)

[Program-4 Similarly for time given in hours, min and seconds.](#Assignment-4)

[Program-5 Time given in hours and minutes.](#Assignment-5) 

[Program-6 Collect the code from internet for any five programs of c language. (Fact, armstrong, palindrome, Fibonacci, pattern)](#Assignment-6) 

[Program-7 Write a class that is having four method for 1-dimensional array. (Input, output 1,out2, reverse).](#Assignment-7)

[Program-8 write a class with multiple methods to perform matrix operations (transpose, addition, sum of rows, sum of columns, sum of diagonal).](#Assignment-8)

[Program-9 Write a program using three classes to print 1-100 ,1-100,1-100 with and without thread and analyse the output and repeat the same program using runnable interface.](#Assignment-9)

[Program-10 Using the concept of multithreading the output of all three threads must be synchronised (use join method).](#Assignment-10)

[Program-11 Addition of 2 numbers using swing.](#Assignment-11)

[Program-12 Make a registration form with 10 elements and send the data into database (use jdbc connectivity)](#Assignment-12)

[Program-13 Make one calculator in swing.](#Assignment-13)

[Program-14 Matrix Addition using swing class.](#Assignment-14)

[Program-15 Create one jframe apply 10 buttons on that after clicking on each button a new structure is created.(Circle, oval rectangle, etc ....)](#Assignment-15)

[Program-16 Just using mouse Event create a frame like paint brush with selection of colour and width.](#Assignment-16)

[Program-17 Create a package of any 5 classes of your choice and import it.](#Assignment-17)

[Program-18 Create one package and sub package  import and test it .](#Assignment-18)

[Program-19 Create one small array of size 5 apply array out of bounds exception using try catch give a proper message in catch and demonstrate the exception exactly in the same fashion demonstrate arithmetic exception .](#Assignment-19)

[Program-20 To test the range of age of one student.write a program using user defined exception.](#Assignment-20)

[Program-21 File Handling Programs (given in the PPT)](#Assignment-21)

[Program-22 Inheritance Programs, using interface and abstract classes.](#Assignment-22)

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

## Assignment-8
```
import java.util.Scanner;

public class MainClass {
    public static void main(String[] args) {
        Matrix obj = new Matrix();

        obj.input();
        obj.addition();
        obj.transpose();
        obj.sumRows();
        obj.sumCols();
        obj.sumDiagonal();
    }
}

class Matrix {
    int a[][];
    int b[][];
    int r, c;

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter rows and columns: ");
        r = sc.nextInt();
        c = sc.nextInt();

        a = new int[r][c];
        b = new int[r][c];

        System.out.println("Enter first matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                a[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter second matrix:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                b[i][j] = sc.nextInt();
            }
        }
    }

    void addition() {
        System.out.println("Addition:");
        int sum[][] = new int[r][c];

        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                sum[i][j] = a[i][j] + b[i][j];
                System.out.print(sum[i][j] + " ");
            }
            System.out.println();
        }
    }

    void transpose() {
        System.out.println("Transpose of first matrix:");
        int t[][] = new int[c][r];

        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                t[j][i] = a[i][j];
            }
        }

        for (int i = 0; i < c; i++) {
            for (int j = 0; j < r; j++) {
                System.out.print(t[i][j] + " ");
            }
            System.out.println();
        }
    }

    void sumRows() {
        System.out.println("Sum of rows (first matrix):");
        for (int i = 0; i < r; i++) {
            int s = 0;
            for (int j = 0; j < c; j++) {
                s += a[i][j];
            }
            System.out.print(s + " ");
        }
        System.out.println();
    }

    void sumCols() {
        System.out.println("Sum of columns (first matrix):");
        for (int j = 0; j < c; j++) {
            int s = 0;
            for (int i = 0; i < r; i++) {
                s += a[i][j];
            }
            System.out.print(s + " ");
        }
        System.out.println();
    }

    void sumDiagonal() {
        System.out.println("Sum of diagonals (first matrix):");
        int s1 = 0, s2 = 0;

        for (int i = 0; i < r; i++) {
            s1 += a[i][i];
            s2 += a[i][c - i - 1];
        }

        System.out.println("Primary = " + s1 + ", Secondary = " + s2);
    }
}

```

Output:
<img width="392" height="583" alt="image" src="https://github.com/user-attachments/assets/d71cc9ad-f86f-418d-9cda-a38a798439fc" />

## Assignment-9
```
public class MainClass {
    public static void main(String[] args) {
        A a = new A();
        B b = new B();
        C c = new C();

        a.print();
        b.print();
        c.print();
    }
}

class A {
    void print() {
        System.out.print("A: ");
        for (int i = 1; i <= 100; i++)
            System.out.print(i + " ");
    }
}

class B {
    void print() {
        System.out.print("\nB: ");
        for (int i = 1; i <= 100; i++)
            System.out.print(i + " ");
    }
}

class C {
    void print() {
        System.out.print("\nC: ");
        for (int i = 1; i <= 100; i++)
            System.out.print(i + " ");
    }
}
```

Output:
<img width="922" height="430" alt="image" src="https://github.com/user-attachments/assets/63ac606d-1ec0-483d-9fbb-ccb9b7289532" />

```
public class MainClass {
    public static void main(String[] args) {
        A t1 = new A();
        B t2 = new B();
        C t3 = new C();

        t1.start();
        t2.start();
        t3.start();
    }
}

class A extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++)
            System.out.println("A: " + i);
    }
}

class B extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++)
            System.out.println("B: " + i);
    }
}

class C extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++)
            System.out.println("C: " + i);
    }
}

```

Output:
<img width="112" height="704" alt="image" src="https://github.com/user-attachments/assets/d6032066-06c6-4b8e-9e9b-cde1fff523b1" />



## Assignment-10
```
public class MainClass {
    public static void main(String[] args) throws Exception {
        A t1 = new A();
        B t2 = new B();
        C t3 = new C();

        t1.start();
        t1.join();

        t2.start();
        t2.join();

        t3.start();
        t3.join();
    }
}
class A extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++)
            System.out.println("A: " + i);
    }
}

class B extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++)
            System.out.println("B: " + i);
    }
}

class C extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++)
            System.out.println("C: " + i);
    }
}

```

Output:
<img width="102" height="693" alt="image" src="https://github.com/user-attachments/assets/efbdf718-d541-4842-b932-5267df2c0f1e" />



## Assignment-11
```
import javax.swing.*;
import java.awt.event.*;

public class AddSwing extends JFrame implements ActionListener {
    JTextField t1, t2, t3;
    JButton b;

    AddSwing() {
        t1 = new JTextField();
        t2 = new JTextField();
        t3 = new JTextField();
        b = new JButton("Add");

        t1.setBounds(50, 50, 150, 30);
        t2.setBounds(50, 100, 150, 30);
        t3.setBounds(50, 150, 150, 30);
        b.setBounds(50, 200, 150, 30);

        add(t1);
        add(t2);
        add(t3);
        add(b);

        b.addActionListener(this);

        setSize(300, 300);
        setLayout(null);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        int a = Integer.parseInt(t1.getText());
        int b = Integer.parseInt(t2.getText());
        int c = a + b;
        t3.setText(String.valueOf(c));
    }

    public static void main(String[] args) {
        new AddSwing();
    }
}
```

Output:



## Assignment-12
```
import javax.swing.*;
import java.awt.event.*;
import java.sql.*;

public class RegistrationForm extends JFrame implements ActionListener {
    JTextField t1,t2,t3,t4,t5,t6,t7,t8,t9,t10;
    JButton b;

    RegistrationForm() {
        setLayout(null);

        JLabel l1=new JLabel("Name");
        JLabel l2=new JLabel("Email");
        JLabel l3=new JLabel("Phone");
        JLabel l4=new JLabel("Address");
        JLabel l5=new JLabel("Username");
        JLabel l6=new JLabel("Password");
        JLabel l7=new JLabel("Gender");
        JLabel l8=new JLabel("Course");
        JLabel l9=new JLabel("City");
        JLabel l10=new JLabel("Country");

        l1.setBounds(30,20,100,25); t1.setBounds(140,20,150,25);
        l2.setBounds(30,50,100,25); t2.setBounds(140,50,150,25);
        l3.setBounds(30,80,100,25); t3.setBounds(140,80,150,25);
        l4.setBounds(30,110,100,25); t4.setBounds(140,110,150,25);
        l5.setBounds(30,140,100,25); t5.setBounds(140,140,150,25);
        l6.setBounds(30,170,100,25); t6.setBounds(140,170,150,25);
        l7.setBounds(30,200,100,25); t7.setBounds(140,200,150,25);
        l8.setBounds(30,230,100,25); t8.setBounds(140,230,150,25);
        l9.setBounds(30,260,100,25); t9.setBounds(140,260,150,25);
        l10.setBounds(30,290,100,25); t10.setBounds(140,290,150,25);

        b = new JButton("Submit");
        b.setBounds(140,330,100,30);

        add(l1); add(t1);
        add(l2); add(t2);
        add(l3); add(t3);
        add(l4); add(t4);
        add(l5); add(t5);
        add(l6); add(t6);
        add(l7); add(t7);
        add(l8); add(t8);
        add(l9); add(t9);
        add(l10); add(t10);
        add(b);

        b.addActionListener(this);

        setSize(350,420);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        String s1=t1.getText();
        String s2=t2.getText();
        String s3=t3.getText();
        String s4=t4.getText();
        String s5=t5.getText();
        String s6=t6.getText();
        String s7=t7.getText();
        String s8=t8.getText();
        String s9=t9.getText();
        String s10=t10.getText();

        try {
            Class.forName("com.mysql.cj.jdbc.Driver");
            Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/test","root","root");

            PreparedStatement ps = con.prepareStatement(
                "insert into registration values(?,?,?,?,?,?,?,?,?,?)"
            );

            ps.setString(1,s1);
            ps.setString(2,s2);
            ps.setString(3,s3);
            ps.setString(4,s4);
            ps.setString(5,s5);
            ps.setString(6,s6);
            ps.setString(7,s7);
            ps.setString(8,s8);
            ps.setString(9,s9);
            ps.setString(10,s10);

            ps.executeUpdate();

            JOptionPane.showMessageDialog(this,"Data Inserted Successfully");

            con.close();
        } catch(Exception ex) {
            System.out.println(ex);
        }
    }

    public static void main(String[] args) {
        new RegistrationForm();
    }
}





import javax.swing.*;
import java.awt.event.*;
import java.sql.*;

public class RegistrationForm extends JFrame implements ActionListener {
    JTextField t1,t2,t3,t4,t5,t6,t7,t8,t9,t10;
    JButton b;

    RegistrationForm() {
        setLayout(null);

        JLabel l1=new JLabel("Name");
        JLabel l2=new JLabel("Email");
        JLabel l3=new JLabel("Phone");
        JLabel l4=new JLabel("Address");
        JLabel l5=new JLabel("Username");
        JLabel l6=new JLabel("Password");
        JLabel l7=new JLabel("Gender");
        JLabel l8=new JLabel("Course");
        JLabel l9=new JLabel("City");
        JLabel l10=new JLabel("Country");

        l1.setBounds(30,20,100,25); t1.setBounds(140,20,150,25);
        l2.setBounds(30,50,100,25); t2.setBounds(140,50,150,25);
        l3.setBounds(30,80,100,25); t3.setBounds(140,80,150,25);
        l4.setBounds(30,110,100,25); t4.setBounds(140,110,150,25);
        l5.setBounds(30,140,100,25); t5.setBounds(140,140,150,25);
        l6.setBounds(30,170,100,25); t6.setBounds(140,170,150,25);
        l7.setBounds(30,200,100,25); t7.setBounds(140,200,150,25);
        l8.setBounds(30,230,100,25); t8.setBounds(140,230,150,25);
        l9.setBounds(30,260,100,25); t9.setBounds(140,260,150,25);
        l10.setBounds(30,290,100,25); t10.setBounds(140,290,150,25);

        b = new JButton("Submit");
        b.setBounds(140,330,100,30);

        add(l1); add(t1);
        add(l2); add(t2);
        add(l3); add(t3);
        add(l4); add(t4);
        add(l5); add(t5);
        add(l6); add(t6);
        add(l7); add(t7);
        add(l8); add(t8);
        add(l9); add(t9);
        add(l10); add(t10);
        add(b);

        b.addActionListener(this);

        setSize(350,420);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        String s1=t1.getText();
        String s2=t2.getText();
        String s3=t3.getText();
        String s4=t4.getText();
        String s5=t5.getText();
        String s6=t6.getText();
        String s7=t7.getText();
        String s8=t8.getText();
        String s9=t9.getText();
        String s10=t10.getText();

        try {
            Class.forName("com.mysql.cj.jdbc.Driver");
            Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/test","root","root");

            PreparedStatement ps = con.prepareStatement(
                "insert into registration values(?,?,?,?,?,?,?,?,?,?)"
            );

            ps.setString(1,s1);
            ps.setString(2,s2);
            ps.setString(3,s3);
            ps.setString(4,s4);
            ps.setString(5,s5);
            ps.setString(6,s6);
            ps.setString(7,s7);
            ps.setString(8,s8);
            ps.setString(9,s9);
            ps.setString(10,s10);

            ps.executeUpdate();

            JOptionPane.showMessageDialog(this,"Data Inserted Successfully");

            con.close();
        } catch(Exception ex) {
            System.out.println(ex);
        }
    }

    public static void main(String[] args) {
        new RegistrationForm();
    }
}
```

Output:



## Assignment-13
```
import javax.swing.*;
import java.awt.event.*;

public class Calculator extends JFrame implements ActionListener {
    JTextField t;
    JButton b1,b2,b3,b4,b5,b6,b7,b8,b9,b0,bAdd,bSub,bMul,bDiv,bEq,bClr;

    String op="";
    double n1,n2;

    Calculator() {
        t = new JTextField();
        t.setBounds(30,30,240,30);
        add(t);

        b1=new JButton("1"); b2=new JButton("2"); b3=new JButton("3");
        b4=new JButton("4"); b5=new JButton("5"); b6=new JButton("6");
        b7=new JButton("7"); b8=new JButton("8"); b9=new JButton("9");
        b0=new JButton("0");

        bAdd=new JButton("+"); bSub=new JButton("-");
        bMul=new JButton("*"); bDiv=new JButton("/");
        bEq=new JButton("="); bClr=new JButton("C");

        b1.setBounds(30,80,50,40); b2.setBounds(90,80,50,40); b3.setBounds(150,80,50,40);
        b4.setBounds(30,130,50,40); b5.setBounds(90,130,50,40); b6.setBounds(150,130,50,40);
        b7.setBounds(30,180,50,40); b8.setBounds(90,180,50,40); b9.setBounds(150,180,50,40);
        b0.setBounds(30,230,50,40);

        bAdd.setBounds(210,80,60,40); bSub.setBounds(210,130,60,40);
        bMul.setBounds(210,180,60,40); bDiv.setBounds(210,230,60,40);

        bEq.setBounds(90,230,50,40); bClr.setBounds(150,230,50,40);

        add(b1); add(b2); add(b3); add(b4); add(b5); add(b6);
        add(b7); add(b8); add(b9); add(b0);
        add(bAdd); add(bSub); add(bMul); add(bDiv);
        add(bEq); add(bClr);

        b1.addActionListener(this); b2.addActionListener(this); b3.addActionListener(this);
        b4.addActionListener(this); b5.addActionListener(this); b6.addActionListener(this);
        b7.addActionListener(this); b8.addActionListener(this); b9.addActionListener(this);
        b0.addActionListener(this);
        bAdd.addActionListener(this); bSub.addActionListener(this);
        bMul.addActionListener(this); bDiv.addActionListener(this);
        bEq.addActionListener(this); bClr.addActionListener(this);

        setSize(320,350);
        setLayout(null);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        String s=e.getActionCommand();

        if(s.equals("1")||s.equals("2")||s.equals("3")||s.equals("4")||
           s.equals("5")||s.equals("6")||s.equals("7")||s.equals("8")||
           s.equals("9")||s.equals("0")) {
            t.setText(t.getText()+s);
        }
        else if(s.equals("+")||s.equals("-")||s.equals("*")||s.equals("/")) {
            n1=Double.parseDouble(t.getText());
            op=s;
            t.setText("");
        }
        else if(s.equals("=")) {
            n2=Double.parseDouble(t.getText());

            if(op.equals("+")) t.setText(""+(n1+n2));
            else if(op.equals("-")) t.setText(""+(n1-n2));
            else if(op.equals("*")) t.setText(""+(n1*n2));
            else if(op.equals("/")) t.setText(""+(n1/n2));
        }
        else if(s.equals("C")) {
            t.setText("");
        }
    }

    public static void main(String[] args) {
        new Calculator();
    }
}
```

Output:



## Assignment-14
```
import javax.swing.*;
import java.awt.event.*;

public class MatrixAdd extends JFrame implements ActionListener {
    JTextField a[][] = new JTextField[2][2];
    JTextField b[][] = new JTextField[2][2];
    JTextField c[][] = new JTextField[2][2];
    JButton btn;

    MatrixAdd() {
        setLayout(null);

        int x1 = 50, x2 = 200, x3 = 350, y = 50;

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                a[i][j] = new JTextField();
                b[i][j] = new JTextField();
                c[i][j] = new JTextField();

                a[i][j].setBounds(x1 + j*40, y + i*40, 35, 30);
                b[i][j].setBounds(x2 + j*40, y + i*40, 35, 30);
                c[i][j].setBounds(x3 + j*40, y + i*40, 35, 30);

                add(a[i][j]);
                add(b[i][j]);
                add(c[i][j]);
            }
        }

        btn = new JButton("Add");
        btn.setBounds(200, 150, 80, 30);
        add(btn);

        btn.addActionListener(this);

        setSize(500, 300);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                int x = Integer.parseInt(a[i][j].getText());
                int y = Integer.parseInt(b[i][j].getText());
                c[i][j].setText(String.valueOf(x + y));
            }
        }
    }

    public static void main(String[] args) {
        new MatrixAdd();
    }
}
```

Output:



## Assignment-15
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class DrawPanel extends JPanel {
    int shape = 0;

    void setShape(int s) {
        shape = s;
        repaint();
    }

    protected void paintComponent(Graphics g) {
        super.paintComponent(g);

        if (shape == 1) g.drawOval(100, 50, 100, 100);
        else if (shape == 2) g.drawOval(100, 50, 150, 80);
        else if (shape == 3) g.drawRect(100, 50, 150, 100);
        else if (shape == 4) g.drawRoundRect(100, 50, 150, 100, 30, 30);
        else if (shape == 5) g.fillRect(100, 50, 150, 100);
        else if (shape == 6) g.fillOval(100, 50, 100, 100);
        else if (shape == 7) g.drawLine(50, 50, 200, 150);
        else if (shape == 8) g.drawArc(100, 50, 150, 100, 0, 180);
        else if (shape == 9) {
            int x[] = {100,150,200};
            int y[] = {150,50,150};
            g.drawPolygon(x,y,3);
        }
        else if (shape == 10) g.fillArc(100, 50, 150, 100, 0, 180);
    }
}

public class ShapeFrame extends JFrame implements ActionListener {
    JButton b[] = new JButton[10];
    DrawPanel p;

    ShapeFrame() {
        setLayout(null);

        p = new DrawPanel();
        p.setBounds(50, 50, 300, 200);
        add(p);

        String names[] = {"Circle","Oval","Rectangle","RoundRect","FillRect",
                          "FillCircle","Line","Arc","Triangle","FillArc"};

        for (int i = 0; i < 10; i++) {
            b[i] = new JButton(names[i]);
            b[i].setBounds(50 + (i%5)*100, 270 + (i/5)*50, 90, 30);
            add(b[i]);
            b[i].addActionListener(this);
        }

        setSize(600,400);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        for (int i = 0; i < 10; i++) {
            if (e.getSource() == b[i]) {
                p.setShape(i+1);
            }
        }
    }

    public static void main(String[] args) {
        new ShapeFrame();
    }
}
```

Output:



## Assignment-16
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.util.ArrayList;

class DrawPoint {
    int x,y,size;
    Color color;

    DrawPoint(int x,int y,Color c,int s) {
        this.x=x;
        this.y=y;
        this.color=c;
        this.size=s;
    }
}

class PaintPanel extends JPanel implements MouseMotionListener {
    ArrayList<DrawPoint> points = new ArrayList<>();
    Color currentColor = Color.BLACK;
    int size = 5;

    PaintPanel() {
        addMouseMotionListener(this);
    }

    public void mouseDragged(MouseEvent e) {
        points.add(new DrawPoint(e.getX(), e.getY(), currentColor, size));
        repaint();
    }

    public void mouseMoved(MouseEvent e) {}

    protected void paintComponent(Graphics g) {
        super.paintComponent(g);

        for (DrawPoint p : points) {
            g.setColor(p.color);
            g.fillOval(p.x, p.y, p.size, p.size);
        }
    }

    void setColor(Color c) {
        currentColor = c;
    }

    void setSize(int s) {
        size = s;
    }
}

public class PaintApp extends JFrame implements ActionListener {
    PaintPanel panel;
    JComboBox<String> colors;
    JComboBox<String> sizes;

    PaintApp() {
        panel = new PaintPanel();
        panel.setBackground(Color.WHITE);

        String c[] = {"Black","Red","Blue","Green","Yellow"};
        String s[] = {"2","5","10","20"};

        colors = new JComboBox<>(c);
        sizes = new JComboBox<>(s);

        colors.addActionListener(this);
        sizes.addActionListener(this);

        add(colors, BorderLayout.NORTH);
        add(sizes, BorderLayout.SOUTH);
        add(panel, BorderLayout.CENTER);

        setSize(600,500);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        String col = (String)colors.getSelectedItem();
        if(col.equals("Black")) panel.setColor(Color.BLACK);
        if(col.equals("Red")) panel.setColor(Color.RED);
        if(col.equals("Blue")) panel.setColor(Color.BLUE);
        if(col.equals("Green")) panel.setColor(Color.GREEN);
        if(col.equals("Yellow")) panel.setColor(Color.YELLOW);

        int sz = Integer.parseInt((String)sizes.getSelectedItem());
        panel.setSize(sz);
    }

    public static void main(String[] args) {
        new PaintApp();
    }
}
```

Output:



## Assignment-17
```
package mypack;

public class A {
    public void show() {
        System.out.println("Class A");
    }
}

package mypack;

public class B {
    public void show() {
        System.out.println("Class B");
    }
}

package mypack;

public class C {
    public void show() {
        System.out.println("Class C");
    }
}

package mypack;

public class D {
    public void show() {
        System.out.println("Class D");
    }
}

package mypack;

public class E {
    public void show() {
        System.out.println("Class E");
    }
}

import mypack.*;

public class MainClass {
    public static void main(String[] args) {
        A a = new A();
        B b = new B();
        C c = new C();
        D d = new D();
        E e = new E();

        a.show();
        b.show();
        c.show();
        d.show();
        e.show();
    }
}
```

Output:



## Assignment-18
```
package mypack;

public class A {
    public void show() {
        System.out.println("Class A from mypack");
    }
}

package mypack;

public class B {
    public void show() {
        System.out.println("Class B from mypack");
    }
}

package mypack.subpack;

public class C {
    public void show() {
        System.out.println("Class C from subpack");
    }
}

package mypack.subpack;

public class D {
    public void show() {
        System.out.println("Class D from subpack");
    }
}

import mypack.*;
import mypack.subpack.*;

public class MainClass {
    public static void main(String[] args) {
        A a = new A();
        B b = new B();
        C c = new C();
        D d = new D();

        a.show();
        b.show();
        c.show();
        d.show();
    }
}
```

Output:



## Assignment-19
```
public class ExceptionDemo {
    public static void main(String[] args) {

        int arr[] = {10, 20, 30, 40, 50};

        try {
            System.out.println("Accessing 6th element: " + arr[5]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: Array index is out of bounds. Please check the index.");
        }

        try {
            int a = 10;
            int b = 0;
            int c = a / b;
            System.out.println(c);
        } catch (ArithmeticException e) {
            System.out.println("Error: Division by zero is not allowed.");
        }
    }
}
```

Output:



## Assignment-20
```
import java.util.Scanner;

class InvalidAgeException extends Exception {
    InvalidAgeException(String msg) {
        super(msg);
    }
}

class AgeTest {
    void checkAge(int age) throws InvalidAgeException {
        if (age < 18 || age > 60)
            throw new InvalidAgeException("Age must be between 18 and 60");
        else
            System.out.println("Valid age");
    }
}

public class MainClass {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter age: ");
        int age = sc.nextInt();

        AgeTest obj = new AgeTest();

        try {
            obj.checkAge(age);
        } catch (InvalidAgeException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

Output:



## Assignment-21
```
import java.io.*;

public class FileHandling {
    public static void main(String[] args) {
        try {
            FileWriter fw = new FileWriter("data.txt");
            fw.write("Hello, this is file handling in Java.\n");
            fw.write("Second line of text.");
            fw.close();

            FileReader fr = new FileReader("data.txt");
            BufferedReader br = new BufferedReader(fr);

            String line;

            while ((line = br.readLine()) != null) {
                System.out.println(line);
            }

            br.close();
        } catch (Exception e) {
            System.out.println("Error: " + e);
        }
    }
}
```

Output:



## Assignment-22
```
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking...");
    }
}

public class MainClass {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.eat();
        d.bark();
    }
}
```

Output:

```
interface Shape {
    void area();
}

class Circle implements Shape {
    public void area() {
        double r = 5;
        System.out.println("Area of Circle = " + (3.14 * r * r));
    }
}

class Rectangle implements Shape {
    public void area() {
        int l = 4, b = 6;
        System.out.println("Area of Rectangle = " + (l * b));
    }
}

public class MainClass {
    public static void main(String[] args) {
        Shape s1 = new Circle();
        Shape s2 = new Rectangle();

        s1.area();
        s2.area();
    }
}
```

Output:


```
abstract class Shape {
    abstract void draw();

    void display() {
        System.out.println("Drawing Shape");
    }
}

class Circle extends Shape {
    void draw() {
        System.out.println("Circle Drawn");
    }
}

class Rectangle extends Shape {
    void draw() {
        System.out.println("Rectangle Drawn");
    }
}

public class MainClass {
    public static void main(String[] args) {
        Shape s1 = new Circle();
        Shape s2 = new Rectangle();

        s1.draw();
        s1.display();

        s2.draw();
        s2.display();
    }
}
```

Output:



