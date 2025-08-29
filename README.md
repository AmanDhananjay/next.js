1. Employee.java (POJO Class)

public class Employee {
    private int employeeNumber;
    private String employeeFirstName;
    private String employeeLastName;
    private double salary;
    private char gender;

    // Default Constructor
    public Employee() {
    }

    // Parameterized Constructor
    public Employee(int employeeNumber, String employeeFirstName, String employeeLastName, double salary, char gender) {
        this.employeeNumber = employeeNumber;
        this.employeeFirstName = employeeFirstName;
        this.employeeLastName = employeeLastName;
        this.salary = salary;
        this.gender = gender;
    }

    // Getters & Setters
    public int getEmployeeNumber() {
        return employeeNumber;
    }

    public void setEmployeeNumber(int employeeNumber) {
        this.employeeNumber = employeeNumber;
    }

    public String getEmployeeFirstName() {
        return employeeFirstName;
    }

    public void setEmployeeFirstName(String employeeFirstName) {
        this.employeeFirstName = employeeFirstName;
    }

    public String getEmployeeLastName() {
        return employeeLastName;
    }

    public void setEmployeeLastName(String employeeLastName) {
        this.employeeLastName = employeeLastName;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    public char getGender() {
        return gender;
    }

    public void setGender(char gender) {
        this.gender = gender;
    }

    // Function to return full name
    public String getFullName() {
        return employeeFirstName + " " + employeeLastName;
    }

    // Display employee details
    public void displayDetails() {
        System.out.println("Employee No: " + employeeNumber);
        System.out.println("Name: " + getFullName());
        System.out.println("Salary: " + salary);
        System.out.println("Gender: " + gender);
    }
}










MainApp.java (As


public class MainApp {
    public static void main(String[] args) {
        // Case 1: Assign values using Setters
        Employee emp1 = new Employee();
        emp1.setEmployeeNumber(101);
        emp1.setEmployeeFirstName("Aman");
        emp1.setEmployeeLastName("Dhananjay");
        emp1.setSalary(45000);
        emp1.setGender('M');
        emp1.displayDetails();

        System.out.println("-------------------------");

        // Case 2: Assign values using Constructor
        Employee emp2 = new Employee(102, "Riya", "Sharma", 55000, 'F');
        emp2.displayDetails();

        System.out.println("-------------------------");

        // Case 3: Accept from Command Line Arguments
        // Example: java MainApp 103 Rahul Verma 60000 M
        if (args.length >= 5) {
            int empNo = Integer.parseInt(args[0]);
            String fName = args[1];
            String lName = args[2];
            double sal = Double.parseDouble(args[3]);
            char gender = args[4].charAt(0);

            Employee emp3 = new Employee(empNo, fName, lName, sal, gender);
            emp3.displayDetails();
        }
    }
}













BusinessLogic.java (Sala





public class BusinessLogic {

    // Compare two employees
    public static String validateSalary(Employee e1, Employee e2) {
        if (e1.getSalary() > e2.getSalary()) {
            return e1.getEmployeeFirstName();
        } else if (e1.getSalary() < e2.getSalary()) {
            return e2.getEmployeeFirstName();
        } else {
            return "Both have equal salary";
        }
    }

    // Compare multiple employees
    public static String validateSalary(Employee[] employees) {
        Employee maxEmp = employees[0];
        for (Employee e : employees) {
            if (e.getSalary() > maxEmp.getSalary()) {
                maxEmp = e;
            }
        }
        return maxEmp.getEmployeeFirstName();
    }
}






TestApp.java





public class TestApp {
    public static void main(String[] args) {
        Employee e1 = new Employee(201, "Rohan", "Verma", 40000, 'M');
        Employee e2 = new Employee(202, "Sneha", "Patel", 60000, 'F');
        Employee e3 = new Employee(203, "Karan", "Singh", 75000, 'M');

        // Exercise 15: Compare two employees
        System.out.println("Highest Salary (between 2): " + BusinessLogic.validateSalary(e1, e2));

        // Exercise 16: Compare more than 2 employees
        Employee[] empArr = {e1, e2, e3};
        System.out.println("Highest Salary (among all): " + BusinessLogic.validateSalary(empArr));

        // Exercise 17: Display Full Name
        System.out.println("Full Name of e2: " + e2.getFullName());
    }
}
