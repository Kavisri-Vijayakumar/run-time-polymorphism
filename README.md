package runtimepolymorphism;
class employee{
    void work(){
        System.out.println("employee is working");
    }
}
class manager extends employee{
    @Override
    void work(){
        System.out.println("manager is planning");
    }
}
class developer extends employee{
    @Override
    void work(){
        System.out.println("developer is coding");
    }
}
class tester extends employee{
    @Override
    void work(){
        System.out.println("tester is testing");
    }
}
public class Runtimepolymorphism {

    
    public static void main(String[] args) {
        employee Employee;
        Employee=new manager();
        Employee.work();
        Employee=new developer();
        Employee.work();
        Employee=new tester();
        Employee.work();
    }
    
}
output
manager is planning
developer is coding
tester is testing
