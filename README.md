# Arrays
Practice
package Array;
public class ImplementationOfQueue
{
	public static void main(String[] ijhb)
	{
		Fifo fifo=new Fifo();
		fifo.push(5);
		fifo.push(10);
		fifo.push(15);
		fifo.push(20);
		fifo.push(25);
		System.out.println(fifo.pop());
		fifo.print();
		System.out.println(fifo.pop());
		fifo.print();
		System.out.println(fifo.pop());
		fifo.print();
		System.out.println(fifo.pop());
		fifo.print();
		System.out.println(fifo.pop());
		fifo.print();
		System.out.println(fifo.pop());
		fifo.print();
	}
}
class Fifo
{
	int[] a=new int[5];
	int index=0;              
	public int pop()
	{
		if(index>0)
		{
			int temp=a[0];
			for(int i=0; i<index-1; i++)
			{
				a[i]=a[i+1];
			}
			index--;
			return temp;
		}
		else
		{
			System.out.println("Queue is empty");
			return 0;
		}
	}
	public void push(int num)
	{
		if(index<a.length)
		{
			a[index++]=num;
		}
		else
			System.out.println("Queue is FULL");
	}
	public void print()
	{
		for(int i=0; i<index; i++)
		{
			System.out.print(a[i]+" ");
		}
		System.out.println();
	}
}
