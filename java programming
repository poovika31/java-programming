import java.util.*;

class Employee {
    int id;
    String name;
    int totalDays = 0;
    int presentDays = 0;
    int leaveDays = 0;

    Employee(int id, String name) {
        this.id = id;
        this.name = name;
    }

    void markAttendance(boolean isPresent) {
        totalDays++;
        if (isPresent) {
            presentDays++;
        } else {
            leaveDays++;
        }
    }

    void applyLeave(int days) {
        leaveDays += days;
        totalDays += days;
    }

    void display() {
        System.out.println("\nEmployee ID: " + id);
        System.out.println("Name: " + name);
        System.out.println("Total Days: " + totalDays);
        System.out.println("Present Days: " + presentDays);
        System.out.println("Leave Days: " + leaveDays);
    }
}

public class AttendanceSystem {

    static Scanner sc = new Scanner(System.in);
    static ArrayList<Employee> empList = new ArrayList<>();

    // Add Employee
    static void addEmployee() {
        System.out.print("Enter Employee ID: ");
        int id = sc.nextInt();
        sc.nextLine();

        System.out.print("Enter Employee Name: ");
        String name = sc.nextLine();

        empList.add(new Employee(id, name));
        System.out.println("Employee Added Successfully!");
    }

    // Find Employee
    static Employee findEmployee(int id) {
        for (Employee e : empList) {
            if (e.id == id) {
                return e;
            }
        }
        return null;
    }

    // Mark Attendance
    static void markAttendance() {
        System.out.print("Enter Employee ID: ");
        int id = sc.nextInt();

        Employee e = findEmployee(id);
        if (e != null) {
            System.out.print("Is Present (true/false): ");
            boolean present = sc.nextBoolean();
            e.markAttendance(present);
            System.out.println("Attendance Updated!");
        } else {
            System.out.println("Employee Not Found!");
        }
    }

    // Apply Leave
    static void applyLeave() {
        System.out.print("Enter Employee ID: ");
        int id = sc.nextInt();

        Employee e = findEmployee(id);
        if (e != null) {
            System.out.print("Enter number of leave days: ");
            int days = sc.nextInt();
            e.applyLeave(days);
            System.out.println("Leave Applied!");
        } else {
            System.out.println("Employee Not Found!");
        }
    }

    // Display Employee Details
    static void displayEmployee() {
        System.out.print("Enter Employee ID: ");
        int id = sc.nextInt();

        Employee e = findEmployee(id);
        if (e != null) {
            e.display();
        } else {
            System.out.println("Employee Not Found!");
        }
    }

    // Display All Employees
    static void displayAll() {
        for (Employee e : empList) {
            e.display();
        }
    }

    public static void main(String[] args) {

        int choice;

        do {
            System.out.println("\n===== Employee Attendance System =====");
            System.out.println("1. Add Employee");
            System.out.println("2. Mark Attendance");
            System.out.println("3. Apply Leave");
            System.out.println("4. Display Employee");
            System.out.println("5. Display All Employees");
            System.out.println("6. Exit");

            System.out.print("Enter your choice: ");
            choice = sc.nextInt();

            switch (choice) {
                case 1:
                    addEmployee();
                    break;
                case 2:
                    markAttendance();
                    break;
                case 3:
                    applyLeave();
                    break;
                case 4:
                    displayEmployee();
                    break;
                case 5:
                    displayAll();
                    break;
                case 6:
                    System.out.println("Thank You!");
                    break;
                default:
                    System.out.println("Invalid Choice!");
            }

        } while (choice != 6);
    }
}
