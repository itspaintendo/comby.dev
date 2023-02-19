import java.util.Scanner;

class Section {
    String name;
    
    public Section(String name) {
        this.name = name;
    }
}

class Student {
    String name;
    
    public Student(String name) {
        this.name = name;
    }
}

class Enrollment {
    Section section;
    Student student;
    
    public Enrollment() {
        section = null;
        student = null;
        System.out.println("Empty enrollment");
    }
    
    public Enrollment(Section section, Student student) {
        this.section = section;
        this.student = student;
    }
}

public class Main {
    public static void main(String[] args) {
        Enrollment enrollment1 = new Enrollment();
        
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter section name: ");
        String sectionName = scanner.nextLine();
        System.out.print("Enter student name: ");
        String studentName = scanner.nextLine();
        scanner.close();
        
        Section section = new Section(sectionName);
        Student student = new Student(studentName);
        
        Enrollment enrollment2 = new Enrollment(section, student);
    }
}
