[Program-1 Wap for addition, sub ,mul, div using object and classes.](#Assignment-1)

## Assignment-1
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



Output:
<img width="357" height="146" alt="Screenshot 2026-04-28 002737" src="https://github.com/user-attachments/assets/993534ec-4d89-4c2d-89d0-86e9437e2506" />
