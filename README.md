# ACD_JAVAB_Session4_Assignment1


import java.util.Scanner;
public class ReverseArr{
	int i;
	Scanner input = new Scanner(System.in);
	public void insert(int a[], int num)
	{
		for(i =1; i<=num; i++)
		{
			System.out.println("Enter "+i+" number");
			a[i-1]=input.nextInt();
		}
		for(i =1; i<=num; i++)
		{
			System.out.println(i+" number is "+a[i-1]+"; ");
		}
	}
		
	public void RevArray(int a[], int num)
	{	
		int len, temp;
		len=num;
		for(i=0; i<num/2;i++)
		{
					temp = a[i];
					a[i]=a[len-1];
					a[len-1]=temp;
			len=len-1;
			}
			
		for(i =0; i<num; i++)
		{
			System.out.println(i+" number is "+a[i]+"; ");
		}
		input.close();
	}
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		Scanner input = new Scanner(System.in);
		int num;
		System.out.println("Enter total number you want to enter");
		num = input.nextInt();
		int a[]=new int[num];
		ReverseArr sa = new ReverseArr();
		sa.insert(a,num);
		sa.RevArray(a,num);
		input.close();
	}

}
