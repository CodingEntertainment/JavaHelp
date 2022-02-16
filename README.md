# JavaHelp
# Collection.sort() Funciton Help
import java.util.*;
import java.lang.*;
import java.io.*;

class Student{
    int rollNo;
    String name;
    
    public Student (int rollNo,String StudentName){
        this.rollNo = rollNo;
        this.name = StudentName;
    }
    
    public String toString()
    {
        return this.rollNo + " " + this.name + " ";   
    }
}

class Sortbyroll implements Comparator<Student>
{
    public int compare(Student student1, Student student2)
    {
        return student1.rollNo - student2.rollNo;
    }
}
public class Main {
    public static void main (String[] args) {
        ArrayList<Student> students = new ArrayList<Student>();
        students.add(new Student(41,"abc"));
        students.add(new Student(11,"abc"));
        students.add(new Student(31,"abc"));
        Collections.sort(students,new Sortbyroll());
        for(int i=0;i<students.size();i++)
        {
            System.out.println(students.get(i));
        }
    }
}
