Reavnvn
\

import java.util.ArrayList;
import java.util.Iterator;
 
public class ArrayListIterator {
 
    public static void main(String a[]){
        ArrayList<String> arrl = new ArrayList<String>();
        //adding elements to the end
        arrl.add("First");
        arrl.add("Second");
        arrl.add("Third");
        arrl.add("Random");
        Iterator<String> itr = arrl.iterator();
        while(itr.hasNext()){
            System.out.println(itr.next());
        }
    }
}
==================================
public class ArraySum {

	public static void main(String[] args) {
		
		
		int a[]={2,4,5,45,67,89,43,565,564,90};
		int sum=0;
		
		for(int i=0;i<a.length;i++)
		{
			sum=sum+a[i];
		}
		System.out.println(sum);
	}

}

========================

import java.util.Arrays;
import java.util.Scanner;

import com.sun.jna.platform.win32.WinUser.INPUT;


public class BinarySearch {

	public static void main(String[] args) 
	
	{
		int i=0, item=65;
		int a[]={2,5,7,84,7,3,5,54,67,};

		
		Arrays.sort(a);
		
		int first=0, last=a.length-1;
		int middle=(first+last)/2;
		
		while(first<=last)
		{
			if(a[middle]<item)
			{
				first=middle+1;
			}
			else if(a[middle]>item)
			{
				last=middle-1;
			}
			else if(a[middle]==item)
			{
				System.out.println("Number found");
				break;
			}
			middle=(first+last)/2;
		}
		if(first>last)
		{
			System.out.println("Numnber not found");
		}
	}

}
========================

import java.util.Arrays;

public class DeleteRepeatedChar {

	public static void main(String[] args) {
		
		String s="abbbdddee";
		
		char c[]=s.toCharArray();
		
		Arrays.sort(c);
		
		int length=c.length;
		
		int count=0;
		
		String finalValue ="";
		
		
        
		for(int i=0;i<length;i++)
		{
			for(int j=0;j<length;j++)
			{
				if(c[i]==c[j])
				{
				 count=count+1;
				}
			}
			
	
			if (count > 1) {
	            finalValue=finalValue+c[i];
	            i=i+count-1;
	        } else {
	            finalValue = finalValue + c[i];
	        }
			count=0;
		
		}
			
		 System.out.println(finalValue);
	}

}

========================
public class Factorial {
	
	public int Fact(int a)
	{
		
		int fact=1;
		for(int i=a;i>=1;i--)
		{
			fact=fact*i;
			
		}
		
		
		return fact;
	}
	
	

	public static void main(String[] args)
	{
	int n=6;

	Factorial obj=new Factorial();

	System.out.println(obj.Fact(n));
	
	
	
	
	
	//	int fact=1;
	
	/*
	for(int i=n;i>=1;i--)
	{
		fact=fact*i;
		
	}
	System.out.println(fact);
	*/
	
	
	}

}
=============================

public class Fibonacci {

	public static void main(String[] args) 
	
	
	{
		int i=0;
		int j=1;
		int x=20;
		
		System.out.println(i);
		System.out.println(j);
		
		for(int a=0;a<=x;a++)
		{
			int sum=i+j;
			System.out.println(sum);
			i=j;
			j=sum;
		}
		
	
	}

}
===============================

public class FirstHundredPrimeNumber {

	public static void main(String[] args)
	{
		 
	int	primecount=0;
		for(int i=1;primecount<51;i++)
		{
			int count=0;
			for(int num=1;num<=i;num++)
			{
				if(i%num==0)
				{
					count=count+1;
				}
				
			}
			if(count==2)
			{
				System.out.print(i+" ");
				primecount=primecount+1;
			}
		}
		System.out.println(primecount);

	}

}
================================

public class Linear_Search 

{
	public static void main(String args[]){

	int a[]={2,5,7,84,3,54,67,3,5,7};
	
	for(int i=0;i<a.length;i++)
	{
		if(a[i]==84)
		{
			System.out.println("Number is found at position "+ (i+1));
		}
	}
	
	}
	
}
===================================

public class maxrepeatedchar {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

	
		String str="aaaahhhiioooiiokkpppkk";
		char c[]=str.toCharArray();
		
		int len=c.length;
		
		
				int temp=0;
				int count=0; int index=0;
				
		for(int i=0;i<len-1;i++)
		{
			for(int j=0;j<len-1;j++)
			{
				if(c[i]==c[j])
				{
					temp=temp+1;
				}
				
			}
			
		if(temp>count)
		{
		count=temp;
		index=i;
		}
		temp=0;
		}
		
		char ch[]=Character.toChars(c[index]);
		System.out.println(ch);
		System.out.println(count);
	}

}

==================================

import java.util.ArrayList;
import java.util.List;

public class MyArrayListNewCollection {

	public static void main(String a[]){
		ArrayList<String> arrl = new ArrayList<String>();
		//adding elements to the end
		arrl.add("First");
		arrl.add("Second");
		arrl.add("Third");
		arrl.add("Random");
		
		
		System.out.println("Actual ArrayList:"+arrl);
		
		
		List<String> list = new ArrayList<String>();
		list.add("one");
		list.add("two");
		arrl.addAll(list);
		System.out.println("After Copy: "+arrl);
	}
}
=================================

import java.util.ArrayList;

public class MyBasicArrayList {
 
    public static void main(String[] a){
         
        ArrayList<String> al = new ArrayList<String>();
        //add elements to the ArrayList
        
        al.add("JAVA");
        al.add("C++");
        al.add("PERL");
        al.add("PHP");
        System.out.println(al);
        
        
        
        //get elements by index
        System.out.println("Element at index 1: "+al.get(1));
        System.out.println("Does list contains JAVA? "+al.contains("JAVA"));
        //add elements at a specific index
        al.add(2,null);
        System.out.println(al);
        System.out.println("Is arraylist empty? "+al.isEmpty());
        System.out.println("Index of PERL is "+al.indexOf("PERL"));
        System.out.println("Size of the arraylist is: "+al.size());
    }
}

===============================

public class NumberisFibonacci {

	public static void main(String[] args) {
		
		int n=47;
		int a=0,b=1, sum=0;
		for(int i=1;i<=n;i++)
		{
			if(sum==n)
			{
				System.out.println("No. is fibonacci");
				break;
			}
			
			sum=b+a;
			a=b;
			b=sum;
			
				
		}

	}

}

====================================
public class Palindrome {

	public static void main(String[] args) 
	
	{
		String str="madam i madam";
int n=str.length();

int count=0;



for(int i=0; i<(n/2)+1; i++)
		{
			
			if(str.charAt(i) !=str.charAt(n-i-1))
			{
				count=1;
				break;
			}
			
		}
		
		if(count==1)
		{
			System.out.println("Not a plaindrome");
			
		}
		else
		{
			System.out.println("Palindrome");
		}
	}

}

================================
public class PrimeNumbers {

	public static void main(String[] args)
	{
		
		int number=2
			;
		int count=0;
		//number is divided by 2 because a number can be maximum divisible by half of its value
		for(int i=2;i<=number/2;i++)
		{
			if(number%i==0)
			{
				count=1;
			}
			
		}
		if(count==0)
		{
			System.out.println(number+" Number is a prime number");
		}
		else
		{
			System.out.println(number+" Number is not a prime number");
		}

	}

}
==============================

import java.util.Arrays;

public class RepeatedNumber {

	public static void main(String[] args) {
		
		int array[]={2,7,4,7,8,1};
		Arrays.sort(array);
		
		for(int a=0;a<array.length-1;a++)
		{
			if(array[a]==array[a+1])
			{
				System.out.println("Duplicate Number" +array[a]);
			}
		}

}
}
===================================

public class Reverse_number {

	public static void main(String[] args)
	
	{
		int i=6429846;
		
		while(i!=0)
		{
			int rem= i%10;
			System.out.print(rem);
			int div=i/10;
			div=i;
		}

	}
}

==================================

public class Reverse {

	public static void main(String[] args)
	{
		
		String str="Print a string";
		//System.out.println(str.length());
		
		char a[]=str.toCharArray();
		int l=a.length;
		for(int i=l-1;i>=0;i--)
		{
			System.out.print(a[i]);
		}
	}

}

=================================

public class Swap {

	public static void main(String[] args) {
	
		int a=30;
		int b=20;
		
		
		System.out.print(a+","+b+"print before swap");
		
		a=a+b;
		b=a-b;
		a=a-b;
		
		System.out.print(a+","+b+"Print after swap");
	   
		
	}

}
========================================


Hi Abdur,
It was indeed a pleasure working with you. You are a quick learner and have the ability to get to the root of the situation for any issue. This was evident in your prompt responses to development and business partners on defect-fix retest requests.

I also appreciate the fact that you are taking charge of your career moves and moving over to a newer venture. This shows that you really live the motto “Change is the only Constant”

Good Luck in the new projects and as you say, I hope our paths cross again !!




-==================

As you’re already aware ‘today is my last working day at Accenture and Bank of America’. After  1.5 years of this wonderful experience, it is very difficult to say goodbye to my leads, colleagues and all my well-wishers. I feel that it is time for me to move on to new opportunities. I can only wish that my new phase in life will give me such rewarding experiences and supportive friends. Thank you so much for making my time at Bank of America Project a truly enjoyable one.

During these last 1.5 years at IVV,  you all have provided me support and through your encouragement and guidance I have been able to excel at the projects offered to me. With many of you, I have shared a unique camaraderie which I hope will continue in the years to come even though I shall not be here with the company. I would like to extend my best wishes to entire group.

Thank you again !!!

I am sure our path will cross again and we will meet again. J J


\\
Hello All,

As most of you know ‘today is my last working day at Accenture and Bank of America’. After  1.5 years of this wonderful experience, it is very difficult to say goodbye to my leads, colleagues and all my well-wishers. I feel that it is time for me to move on to new opportunities. I can only wish that my new phase in life will give me such rewarding experiences and supportive friends. Thank you so much for making my time at Accenture a truly enjoyable one.

Thank you Sri, Basvaraj, Mukund, Praveen and everyone else at Accenture for giving me the opportunity to bring my best to work here.


=======
Four years ago today, I walked into Facebook for the first time as an employee. Every day since has been a great honor. Facebook is truly a mission based culture. Our objective is to help make the world more open and connected. Despite the fact that we have over 1.3B people who use the product, in our minds, we have so much more work ahead of us than behind us. Work that I believe helps make the world a better place.
Facebook challenges all that I have to offer both as a business and technical leader. It is comprised of some of the most passionate, intelligent people I've had the opportunity to meet. And it is my belief, that as we grow, we are just getting better as a company. We learn from our mistakes, we learn from working together, and we encourage each other to reach beyond what we believe is possible.
I'm grateful for the opportunity to work at a company that touches so many people. I'm grateful that I have an opportunity to work with others who have so much to offer the world. I'm grateful that I have such an awesome team - a team that makes my best ideas better, and is unafraid to tell me of my worst ones. Most of all I'm excited about what lies ahead.
Thank you Mark Zuckerberg, Sheryl Sandberg, David Ebersman, Dave Wehner and everyone else at Facebook for giving me the opportunity to bring my best to work here.





Team –

Since i will be on vacation next week please take care of the below items

•	We need to start our execution from Monday 08/18 (As per test Plan) – Attaching here the Test plan for your reference
•	Make sure of the test cases preparation and complete them in next week whatever the confirmed scope items received
•	Work with Tech team on completing the installations (Please check with Ashok or me before asking any query to tech team as i told in the meeting).
•	Take care of your Time in and Out to the office, maintain 9 hours properly
•	Individual Lab machines please login in to the clones of VM ware and make sure all are working fine or not- make a note and let me know about that once my return.
•	Avoid taking Unplanned leaves on next week and also till this release
•	I will approve MYTE on Tuesday or Wednesday, please check periodically and one can all me and update regarding same if i forgot.

Any urgent call me any time.

==================================


http://beginnersbook.com/2013/04/oops-concepts/

=======================
http://beginnersbook.com/2014/01/java-program-to-display-prime-numbers/

==============================
http://www.share-pdf.com/092b70af6e4046df964193f8b4f00c0b/ICSEProgramsAnswers.pdf

http://www.icsejava.com/programs

http://www.scribd.com/doc/93761560/ICSE-MARCH-2014-JAVA-PROGRAMS-USING-BLUEJ



--------------------------------------------------------
--------------------------------------------------------
---------- Forwarded message ----------
From: "shashank shekhar" <shashank.dba@gmail.com>
Date: Jul 18, 2014 12:28 AM
Subject: Fwd: CV Shortlisted for Test Engineer@Akosha.com|Online Test- First Round
To: "abdur rehman" <rehman.ab.av@gmail.com>
Cc:



---------- Forwarded message ----------
From: priyanka bisht | Akosha <careers+f30h9eus@myakosha.recruiterbox.com>
Date: Thu, Jul 17, 2014 at 7:24 PM
Subject: CV Shortlisted for Test Engineer@Akosha.com|Online Test- First Round
To: shashank.dba@gmail.com


Dear Shashank Shekhar,

Thank you for applying to Akosha. To take your candidature further, kindly reply to this email with an answer to the following question:

Q1.Write a selenium script to automatically fill and submit the following form:
http://goo.gl/Gu1Zol

Please reply to the above question before 4 pm tomorrow. If we don't receive a reply from you, you may consider your application will be rejected.

Thank you.
Akosha Team


-----------------------------------------------
-----------------------------------------------

1st technical
From Java 
=============
1.What is the Difference between final,finally,finalize
2.what is the difference between Call by value and call by referance
3.How to find out the length of the string without using length function
4.How to find out the part of the string from a string
5.difference between throw & throws
6.What is binding(Early and Late binding)

He give Programes 
-----------------------------------
1.Reverse a number
2.1,2,3,4,5,65,76,5,,4,33,4,34,232,3,2323,
find the biggest number among these
simple string programe002E
what is exception, types of exception

From manual
----------------------------------
what is the testcase technique
why we write test case.
bug life cycle
what are the different status of bug
what is the different between functional and smoke testing 
what is STLC.

from Selenium
=======================================
what is testng and its advantage
how to handle SSl/
how to handle alert
how to take screenshot 
give the diagram write a scrpt..
tell me about Project .What are the challenge face during project
what is the difference between RC and webdriver
what is freamwork explain it.
why we use wait statement.

2nd technical
he gives a application & tell to write the scenario
some manual testing concepts.
