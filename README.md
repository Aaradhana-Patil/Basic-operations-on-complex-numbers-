# Basic-operations-on-complex-numbers-
#Basic Mathematical operations like addition, multiplication, subtraction and division on complex numbers using java 
#Author - aaradhana p.
package assignment1;
import java.util.Scanner;
public class complex_91 {
	public static void main(String[] args) {
		float n1,n2;
		float ans;
		complex_op cal= new complex_op();
		Scanner sc=new Scanner(System.in);
		System.out.print("\nEnter the first Complex number:");
		n1=sc.nextFloat();
		n2=sc.nextFloat();
		complex_op object1=new complex_op(n1,n2);
		System.out.print("\nEnter the second Complex number:");
		n1=sc.nextFloat();
		n2=sc.nextFloat();
		complex_op object2=new complex_op(n1,n2);
		int ch;
		do {//int ch;
			System.out.print("\n1.Addition \n2.Substraction \n3.Multiplication \n4.division \n5.Exit");
			System.out.print("\nEnter your choice:");
			 ch= sc.nextInt();
			switch(ch)
			{
			case 1:
				   cal.AddComplex(object1,object2);
				   break;
				   
			case 2:
				   cal.SubComplex(object1,object2);
				   break;
				   
			case 3:
				   cal.MulComplex(object1,object2);
				   break;
				   
			case 4:
				  cal.DivComplex(object1,object2);
				  break;
			default:
				System.out.print("\nEnter valid choice!!!");
			}
			}while(ch<5);
		//sc.close();
		}
	
}
class complex_op{
	float real,imag;
	
	complex_op(){
		real=0;
		imag=0;
	}
	complex_op(float comp1,float comp2){
		real=comp1;
		imag=comp2;
	}
	public void AddComplex(complex_op c1,complex_op c2) {
		float real,imag;
		real=(c1.real+c2.real);
		imag=(c1.imag+c2.imag);
		System.out.print("The addition is:("+real+")+("+imag+")i");
		
	}
	public void SubComplex(complex_op c1,complex_op c2) {
		float real,imag;
		real=(c1.real-c2.real);
		imag=(c1.imag-c2.imag);
		System.out.print("The addition is:("+real+")+("+imag+")i");
		
	}
	public void MulComplex(complex_op c1,complex_op c2) {
		float real,imag;
		real=(c1.real*c2.real)-(c1.imag*c2.imag);
		imag=(c1.real*c2.imag)+(c1.imag*c2.real);
		System.out.print("The multiplication is:("+real+")+("+imag+")i");
		
	}
	public void DivComplex(complex_op c1,complex_op c2) {
		float real,imag;
		real=((c1.real*c2.real)+(c1.imag*c2.imag))/(c2.real*c2.real+c2.imag*c2.imag);
		imag=((c1.imag*c2.real)-(c1.real*c2.imag))/(c2.real*c2.real+c2.imag*c2.imag);
		System.out.print("The division is:("+real+")+("+imag+")i");
		
	}

}
