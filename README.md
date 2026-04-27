[Program-1 Wap for addition, sub ,mul, div using object and classes.](#Assignment-1)
[Program-2 Write a class for addition of two distance where each distance is given in m,cm,mm.](#Assignment-2)

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
