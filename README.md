# lab-sheet-08
code

// Q1. Generic Box
class Box<T> {
    T value;

    Box(T value) {
        this.value = value;
    }

    void display() {
        System.out.println(value);
    }
}

// Q2. Generic Result
class Result<T> {
    T marks;

    Result(T marks) {
        this.marks = marks;
    }

    void display() {
        System.out.println("Marks: " + marks);
    }
}

// Q3. Generic Student
class Student1<T> {
    T id;

    Student1(T id) {
        this.id = id;
    }

    void display() {
        System.out.println("Student ID: " + id);
    }
}

// Q4. Generic Pair
class Pair<T, U> {
    T id;
    U name;

    Pair(T id, U name) {
        this.id = id;
        this.name = name;
    }

    void display() {
        System.out.println(id + " " + name);
    }
}

// Q5. Product Pair
class Product<T, U> {
    T id;
    U price;

    Product(T id, U price) {
        this.id = id;
        this.price = price;
    }

    void display() {
        System.out.println("ID: " + id + " Price: " + price);
    }
}

// Q6. Generic Employee
class Employee<T, U> {
    T id;
    U name;

    Employee(T id, U name) {
        this.id = id;
        this.name = name;
    }

    void display() {
        System.out.println("ID: " + id + " Name: " + name);
    }
}

// Q7. Generic Method
class Q7 {
    static <T> void display(T value) {
        System.out.println(value);
    }
}

// Q8. Generic Method for Three Values
class Q8 {
    static <T> void display(T a, T b, T c) {
        System.out.println(a + " " + b + " " + c);
    }
}

// Q9. Generic ArrayList
class Q9 {
    static void run() {
        java.util.ArrayList<Integer> list =
            new java.util.ArrayList<>();

        for (int i = 1; i <= 10; i++) {
            list.add(i);
        }

        for (int n : list) {
            System.out.println(n);
        }
    }
}

// Q10. Generic String List
class Q10 {
    static void run() {
        java.util.ArrayList<String> names =
            new java.util.ArrayList<>();

        names.add("Rahul");
        names.add("Aman");
        names.add("Ravi");
        names.add("Neha");
        names.add("Priya");

        System.out.println(names.get(0));

        names.set(1, "Karan");
        names.remove("Ravi");

        System.out.println("Size: " + names.size());
        System.out.println(names);
    }
}

// Q11. Search in Generic List
class Q11 {
    static void run() {
        java.util.Scanner sc = new java.util.Scanner(System.in);

        java.util.ArrayList<Integer> list =
            new java.util.ArrayList<>();

        for (int i = 1; i <= 10; i++) {
            list.add(i);
        }

        System.out.print("Enter number: ");
        int n = sc.nextInt();

        if (list.contains(n)) {
            System.out.println("Number Found");
        } else {
            System.out.println("Number Not Found");
        }
    }
}

// Q12. Generic Container
class Container<T> {
    T value;

    void add(T value) {
        this.value = value;
    }

    T get() {
        return value;
    }
}

// Q13. Generic Class with Three Parameters
class Student2<T, U, V> {
    T id;
    U name;
    V marks;

    Student2(T id, U name, V marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    void display() {
        System.out.println(id + " " + name + " " + marks);
    }
}

// Q14. Generic Method and ArrayList
class Q14 {
    static <T> void displayList(
        java.util.ArrayList<T> list) {

        for (T item : list) {
            System.out.println(item);
        }
    }
}

// Q15. Mini Generic Student Management
class Student3<T, U, V> {
    T id;
    U name;
    V marks;

    Student3(T id, U name, V marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    void display() {
        System.out.println(
            "ID: " + id +
            " Name: " + name +
            " Marks: " + marks
        );
    }
}

// MAIN CLASS
public class Main {
    public static void main(String[] args) {

        // Q1
        Box<Integer> b1 = new Box<>(100);
        Box<String> b2 = new Box<>("Hello");
        Box<Double> b3 = new Box<>(85.5);
        b1.display();
        b2.display();
        b3.display();

        // Q2
        Result<Integer> r1 = new Result<>(90);
        Result<Double> r2 = new Result<>(85.5);
        r1.display();
        r2.display();

        // Q3
        Student1<Integer> s1 = new Student1<>(101);
        s1.display();

        // Q4
        Pair<Integer, String> p =
            new Pair<>(101, "Rahul");
        p.display();

        // Q5
        Product<Integer, Double> p1 =
            new Product<>(1, 500.0);
        Product<Integer, Double> p2 =
            new Product<>(2, 750.0);
        Product<Integer, Double> p3 =
            new Product<>(3, 900.0);
        p1.display();
        p2.display();
        p3.display();

        // Q6
        Employee<Integer, String> e =
            new Employee<>(101, "Aman");
        e.display();

        // Q7
        Q7.display(100);
        Q7.display(85.5);
        Q7.display("Hello");
        Q7.display('A');

        // Q8
        Q8.display(10, 20, 30);
        Q8.display("A", "B", "C");
        Q8.display(1.5, 2.5, 3.5);

        // Q9
        Q9.run();

        // Q10
        Q10.run();

        // Q11
        Q11.run();

        // Q12
        Container<Integer> c1 = new Container<>();
        c1.add(100);
        System.out.println(c1.get());

        Container<String> c2 = new Container<>();
        c2.add("Hello");
        System.out.println(c2.get());

        Container<Double> c3 = new Container<>();
        c3.add(85.5);
        System.out.println(c3.get());

        // Q13
        Student2<Integer, String, Double> st1 =
            new Student2<>(101, "Rahul", 85.5);

        Student2<Integer, String, Double> st2 =
            new Student2<>(102, "Aman", 90.0);

        Student2<Integer, String, Double> st3 =
            new Student2<>(103, "Ravi", 88.5);

        st1.display();
        st2.display();
        st3.display();

        // Q14
        java.util.ArrayList<Integer> numbers =
            new java.util.ArrayList<>();

        numbers.add(10);
        numbers.add(20);
        numbers.add(30);

        Q14.displayList(numbers);

        java.util.ArrayList<String> words =
            new java.util.ArrayList<>();

        words.add("Java");
        words.add("Python");

        Q14.displayList(words);

        // Q15
        java.util.ArrayList<
            Student3<Integer, String, Double>> students =
            new java.util.ArrayList<>();

        students.add(new Student3<>(101, "Rahul", 85.5));
        students.add(new Student3<>(102, "Aman", 90.0));
        students.add(new Student3<>(103, "Ravi", 88.0));
        students.add(new Student3<>(104, "Neha", 92.5));
        students.add(new Student3<>(105, "Priya", 95.0));

        System.out.println("All Students:");

        for (Student3<Integer, String, Double> s : students) {
            s.display();
        }

        System.out.println("First Student:");
        students.get(0).display();

        int searchId = 103;
        boolean found = false;

        for (Student3<Integer, String, Double> s : students) {
            if (s.id.equals(searchId)) {
                System.out.println("Student Found:");
                s.display();
                found = true;
                break;
            }
        }

        if (!found) {
            System.out.println("Student Not Found");
        }

        System.out.println("Total Students: " + students.size());

        // Type Safety Example
        // students.add("Hello"); // Error: Wrong Type
    }
}

