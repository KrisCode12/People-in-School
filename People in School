import java.util.Scanner;
public class CollegeList{

    public static void main(String[] args) {
      Scanner scan = new Scanner (System.in);

      System.out.println ("Press S for Students, Press F for Faculty, Press E for Employee: ");
      String choice = scan.nextLine();

        scan.nextLine();

        if (choice.equalsIgnoreCase("S")){
            System.out.println("Type student's name, contact number, program, and year level." +
                    " Press Enter after every input.");

            String name = scan.nextLine();
            String contactNumber = scan.nextLine();
            String program = scan.nextLine();
            int yearLevel = scan.nextInt();

            Student  student = new Student();
            student.setName(name);
            student.setContactNumber(contactNumber);
            student.setProgram(program);
            student.setYearLevel(yearLevel);

            System.out.println("Name: " + student.getName());
            System.out.println("Contact Number: " + student.getContactNumber());
            System.out.println("Program: " + student.getProgram());
            System.out.println("Year level: " + student.getYearLevel());
        }else if (choice.equalsIgnoreCase("E")){
            System.out.println("Type employee's name, contact number, salary, " +
                    "and department. Enter input every lines.");
            String name = scan.nextLine();
            String contactNumber = scan.nextLine();
            double salary = scan.nextDouble();

            // prevents Scanner skipping input
            scan.nextLine();

            // take department input (last input)
            String department = scan.nextLine();
            Employee employee = new Employee();
            employee.setName(name);
            employee.setContactNumber(contactNumber);
            employee.setSalary(salary);
            employee.setDepartment(department);

            // display employee information
            System.out.println("-------------------------------");
            System.out.println("Name: " + employee.getName());
            System.out.println("Contact Number: " + employee.getContactNumber());
            System.out.println("Salary: " + employee.getSalary());
            System.out.println("Department: " + employee.getDepartment());

        }else if(choice.equalsIgnoreCase("F")){
            System.out.print("Are you regular or tenured faculty member? Y/N: ");
           String response = scan.nextLine();

            System.out.println("Type employee's name, contact number, salary, " +
                    "and department. Press Enter once you entered an input.");


            scan.nextLine();
            String name = scan.nextLine();
            String contactNum = scan.nextLine();
            double salary = scan.nextDouble();


            scan.nextLine();

            String department = scan.nextLine();

            Faculty faculty = new Faculty();
            faculty.setName(name);
            faculty.setContactNumber(contactNum);
            faculty.setSalary(salary);
            faculty.setDepartment(department);

            if (response.equalsIgnoreCase("Y")) {
                faculty.isRegular(true);
            } else {
                faculty.isRegular(false);
            }


            System.out.println("-------------------------------");
            System.out.println("Name: " + faculty.getName());
            System.out.println("Contact Number: " + faculty.getContactNumber());
            System.out.println("Salary: " + faculty.getSalary());
            System.out.println("Department: " + faculty.getDepartment());

            System.out.println("Status: " + (faculty.isStatus() ? "Regular" : "Irregular"));

        }



    }
}
public class Person {
    private String name;
    private String contactNumber;

    public void setName(String name) {
        this.name = name;
    }
    public String getName(){
        return name;
    }
    public void setContactNumber(String contactNumber){
        this.contactNumber = contactNumber;
    }
    public String getContactNumber(){
        return contactNumber;
    }


}
public class Student extends  Person {
    private String program;
    private int yearLevel;

    public void setProgram(String program ){
        this.program = program;
    }
    public String getProgram(){
        return program;
    }
    public void setYearLevel(int yearLevel){
        this.yearLevel = yearLevel;
    }
    public int getYearLevel(){
        return yearLevel;
    }
}
public class Employee extends Person {
    private double salary;
    private String department;

    public void setSalary(double salary){
        this.salary = salary;
    }
    public double getSalary(){
        return salary;
    }
    public void setDepartment(String department){
        this.department = department;
    }
    public String getDepartment(){
        return department;
    }
}
public class Faculty extends  Employee {
    private boolean status;


    public void isRegular(boolean Status){
        this.status = status;
    }
    public boolean isStatus(){
        return status;
    }


}
