# OOap-Lab-Task-2

class Person {

    String name;
    int age;

    static String universityName = "NUML University";

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    static void showUniversityInfo() {
        System.out.println("University: " + universityName);
    }

    void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

class Teacher extends Person {

    String subject;
    double salary;

    Teacher(String name, int age) {
        super(name, age);
        subject = "Computer Science";
        salary = 60000;
    }

    Teacher(String name, int age, String subject, double salary) {
        super(name, age);
        this.subject = subject;
        this.salary = salary;
    }

    @Override
    void displayInfo() {
        System.out.println("Teacher Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Subject: " + subject);
        System.out.println("Salary: " + salary);
    }
}

class Student extends Person {

    int rollNo;
    double marks;

    Student(String name, int age) {
        super(name, age);
        rollNo = 1;
        marks = 0;
    }

    Student(String name, int age, int rollNo, double marks) {
        super(name, age);
        this.rollNo = rollNo;
        this.marks = marks;
    }

    @Override
    void displayInfo() {
        System.out.println("Student Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Roll Number: " + rollNo);
        System.out.println("Marks: " + marks);
    }
}

public class Main {
    public static void main(String[] args) {

        Teacher t = new Teacher(
            "Ahmed", 35, "Java", 80000
        );

        Student s = new Student(
            "Abdullah", 20, 101, 85
        );

        Person.showUniversityInfo();

        System.out.println("\nTeacher Information:");
        t.displayInfo();

        System.out.println("\nStudent Information:");
        s.displayInfo();
    }
}
