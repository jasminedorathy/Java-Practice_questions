##Java-Practice_Programs


##1) SUM OF ELEMENTS
````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		
		int sum=0;
		for(int i=0;i<n;i++){
		    sum+=a[i];
		}
		System.out.println("Sum of the element "+sum);
	}
}


output

Enter the size of the array
5
Enter the Elements
8
2
5
1
9
Sum of the element 25

````

##  2) FIND MINIMUM AND MAXIMUM ELEMENT IN ARRAY

````java[]
import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the sizee of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		
		int min=a[0];
		int max=a[0];
		for(int i=0;i<n;i++){
		   if(min>a[i]){
		       min=a[i];
		   }
		   if(max<a[i]){
		       max=a[i];
		   }
		}
		System.out.println("Maximum of the element "+max);
		
		System.out.println("Minimum of the element "+min);
	}
}


output

Enter the sizee of the array
5
Enter the Elements
77
71
51
55
63
Maximum of the element 77
Minimum of the element 51


````

##  3) REVERSE AN ARRAY

````java[]
import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		
		System.out.println("After Reverse Element");
	   for(int i=n-1;i>=0;i--){
	       System.out.print(a[i]+" ");
	   }
	}
}

output:

Enter the size of the array
5
Enter the Elements
8
2
5
1
6
After Reverse Element
6 1 5 2 8

````

##  4) FIND THE DUPLICATE ELEMENT IN AN ARRAY

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		
		System.out.println("Duplicate value");
	 for(int i=0;i<n;i++){
	     for(int j=i+1;j<n;j++){
	     if(a[i]==a[j]){
	         System.out.println(a[j]);
	}
}
}
	     }
	 }

output:

Enter the size of the array
9
Enter the Elements
1
2
3
4
2
7
8
8
1
Duplicate value
1
2
8

````

## 5) FIND THE KTH LARGEST ELEMENT

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
        int k=s.nextInt();
        for(int i=0;i<n;i++){
            for(int j=i+1;j<n;j++){
                if(a[i]<a[j]){
                int temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
            }
        }
        System.out.println("After Swapping");
        for(int i=0;i<n;i++){
            System.out.print(a[i]+" ");
        }
        System.out.println(k+"th Largest Element"+a[k-1]);
	     }
	 }


OUTPUT:

Enter the size of the array
8
Enter the Elements
51
55
71
77

115
35
37
99
3
After Swapping
115 99 77 71 55 51 37 35
3th Largest Element77

````

## 6) CHECK IF A GIVEN NUMBER IS PRESENT IN ARRAY

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
        System.out.println("Enter the number you want to check");
        int k=s.nextInt();
        boolean found=false;
        for(int i=0;i<n;i++){
            if(a[i]==k){
                found=true;
            }
        }
        if(found==true){
            System.out.println("Element is found");
        }
        else{
            System.out.println("Element is not found");
        }
	     }
	 }

OUTPUT:

Enter the size of the array
4
Enter the Elements
7
1
4
9
Enter the number you want to check
2
Element is not found


````


## 7) FIND THE UNIQUE VALUE

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		
		System.out.println("unique value");
	 for(int i=0;i<n;i++){
	     int count=0;
	     for(int j=0;j<n;j++){
	     if(a[i]==a[j]){
	        count++;
	}
}
if(count==1){
    System.out.println(a[i]);
}
}
	     }
	 }

OUTPUT:
Enter the size of the array
6
Enter the Elements
5
2
5
4
1
4
unique value
2
1

````

## 8) MOVE ALL THE ZEROS TO THE END OF AN ARRAY

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	  System.out.println("Enter the array size");
	  int n=s.nextInt();
	  int a[]=new int[n];
	  System.out.println("Enter the array element");
	  for(int j=0;j<n;j++){
	      a[j]=s.nextInt();
	  }
	   int   i=0;
	  for(int num:a){
	   
	      if(num==0){
	          a[i]=num;
	          i++;
	      }
	  }
	  while(i<n){
	      a[i]=0;
	      i++;
	  }
	  System.out.println("After Move all Zero");
	  for(int j=0;j<n;j++){
	      System.out.print(a[j]+" ");
	  }
	}
}


output:

Enter the array size
5
Enter the array element
0
1
0
12
7
After Move all Zero
1 12 7 0 0

````
## 9) ROTATE AN ARRAY K POSITION(RIGHT AND LEFT SIDE)

````java[]

import java.util.*;
class Solution{
    public void leftrotate(int a[],int k,int n){
        k%=n;
        reverse(a,0,k-1);
        reverse(a,k,n-1);
        reverse(a,0,n-1);
       
    }
     public void rightrotate(int a[],int k,int n){
        k%=n;
        reverse(a,0,n-1);
        reverse(a,0,k-1);
        reverse(a,k,n-1);
        
       
    }
    public void reverse(int a[],int start,int end){
        while(start<end){
            int temp=a[start];
            a[start]=a[end];
            a[end]=temp;
            start++;
            end--;
        }
    }
}
public class Main
{    
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	  System.out.println("Enter the array size");
	  int n=s.nextInt();
	  int a[]=new int[n];
	  System.out.println("Enter the array element");
	  for(int j=0;j<n;j++){
	      a[j]=s.nextInt();
	  }
	  System.out.println("Enter the k value");
	  int k=s.nextInt();
	   int[] b = Arrays.copyOf(a, n);
	  System.out.println("After rotate");
	  Solution s1=new Solution();
	  s1.leftrotate(a,k,n);
         System.out.println("left Rotated Array: " + Arrays.toString(a));
        s1.rightrotate(b,k,n);
        System.out.println("Right Rotated Array: " + Arrays.toString(b));
	  }
	}


OUTPUT:

Enter the array size
5
Enter the array element
1
2
3
4
5
Enter the k value
2
After rotate
left Rotated Array: [3, 4, 5, 1, 2]
Right Rotated Array: [4, 5, 1, 2, 3]

````

## 10) FIND THE FACTORIAL OF LARGEST NUMBER

````java[]

import java.util.*;
import java.math.BigInteger;
public class Main
{
    public static BigInteger fact(long n){
        if(n==0 || n==1){
            return BigInteger.ONE;
        }
        return BigInteger.valueOf(n).multiply(fact(n-1));
    }
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		int n=s.nextInt();
		BigInteger result=fact(n);
		System.out.println(result);
	}
}


OUTPUT:

100
93326215443944152681699238856266700490715968264381621468592963895217599993229915608941463976156518286253697920827223758251185210916864000000000000000000000000

````


 ## 11) FIND THE MISSING NUMBER

````java[]

  import java.util.*;
public class Main
{
	public static void main(String[] args) {
	  Scanner s=new Scanner(System.in);
	  System.out.println("Enter the size of array");
	  int size=s.nextInt();
	  int a[]=new int[size];
	  System.out.println("Enter the array element");
	  for(int i=0;i<size;i++){
	      a[i]=s.nextInt();
	  }
	  System.out.println("Enter the n value");
	  int n=s.nextInt();
	  int result=(n*(n+1))/2;
	  int sum=0;
	  for(int i=0;i<size;i++){
	      sum+=a[i];
	  }
	  int missingnumber=result-sum;
	  System.out.println("Missing number "+missingnumber);
	}
}

output:

Enter the size of array
6
Enter the array element
4
2
7
1
5
6
Enter the n value
7
Missing number 3

````

## 12) MERGE TWO SORTED ARRAY	

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	  Scanner s=new Scanner(System.in);
	  System.out.println("Enter the size of the first array");
	  int n1=s.nextInt();
	  int a[]=new int[n1];
	  System.out.println("Enter the array element");
	  for(int i=0;i<n1;i++){
	      a[i]=s.nextInt();
	  }
	  System.out.println("Enter the size of the second array");
	  int n2=s.nextInt();
	  int b[]=new int[n2];
	  System.out.println("Enter the array element");
	  for(int i=0;i<n2;i++){
	      b[i]=s.nextInt();
	  }
	  int c[]=new int[n1+n2];
	  for(int i=0;i<n1;i++){
	      c[i]=a[i];
	  }
	  for(int i=0;i<n2;i++){
	      c[i+n1]=b[i];
	      
	  }
	  Arrays.sort(c);
	  System.out.println("After Merged");
	  System.out.println(Arrays.toString(c));
	  
	}
}


SECOND METHOD:

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	  Scanner s=new Scanner(System.in);
	  System.out.println("Enter the size of the first array");
	  int n1=s.nextInt();
	  int a[]=new int[n1];
	  System.out.println("Enter the array element");
	  for(int i=0;i<n1;i++){
	      a[i]=s.nextInt();
	  }
	  System.out.println("Enter the size of the second array");
	  int n2=s.nextInt();
	  int b[]=new int[n2];
	  System.out.println("Enter the array element");
	  for(int i=0;i<n2;i++){
	      b[i]=s.nextInt();
	  }
      int i=0,j=0;
      System.out.println("After union operation");
      while(i<n1 && j<n2){
          if(a[i]<b[j]){
              System.out.println(a[i++]+" ");
          }
          else if(a[i]>b[j]){
              System.out.println(b[j++]+" ");
          }
          else{
                System.out.println(a[i++]+" ");
                j++;
          }
      }
      
      while(i<n1){
           System.out.println(a[i++]+" ");
      }
      while(j<n2){
               System.out.println(b[j++]+" ");
      }
	  
	  
	}
}


output:

Enter the size of the first array
3
Enter the array element
10
20
30
Enter the size of the second array
4
Enter the array element
5
10
15
20
After Merged
[5, 10, 10, 15, 20, 20, 30]

````

## 13) FIND THE OCCURENCE OF AN INTEGER AN ARRAY

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	  Scanner s=new Scanner(System.in);
	  System.out.println("Enter the size of the  array");
	  int n1=s.nextInt();
	  int a[]=new int[n1];
	  System.out.println("Enter the array element");
	  for(int i=0;i<n1;i++){
	      a[i]=s.nextInt();
	  }
       System.out.println("Enter the target value");
       int target=s.nextInt();
       
       int count=0;
       for(int i=0;i<n1;i++){
           if(a[i]==target){
               count++;
           }
       }
       System.out.println("occurence of "+target+": "+ count);
	  
	}
}


OUTPUT:

Enter the size of the  array
7
Enter the array element
1
2
3
2
4
2
5
Enter the target value
2
occurence of 2: 3

````

## 14) INTERSECTION OF TWO ARRAY

````java[]


import java.util.*;
public class Main
{
	public static void main(String[] args) {
	  Scanner s=new Scanner(System.in);
	  ArrayList<Integer>  result=new ArrayList<>();
	  System.out.println("Enter the size of the first array");
	  int n1=s.nextInt();
	  int a[]=new int[n1];
	  System.out.println("Enter the array element");
	  for(int i=0;i<n1;i++){
	      a[i]=s.nextInt();
	  }
	  System.out.println("Enter the size of the second array");
	  int n2=s.nextInt();
	  int b[]=new int[n2];
	  System.out.println("Enter the array element");
	  for(int i=0;i<n2;i++){
	      b[i]=s.nextInt();
	  }
      int i=0,j=0;
      System.out.println("After Intersection operation");
      while(i<n1 && j<n2){
          if(a[i]==b[j]){
              result.add(a[i]);
              i++;
              j++;
          }
          else if(a[i]<b[j]){
             i++;
          }
          else{
                j++;
          }
      }
      
     
	  System.out.println(result);
	  
	}
}


output:

Enter the size of the first array
5
Enter the array element
1
2
3
4
5
Enter the size of the second array
5
Enter the array element
3
4
5
6
7
After Intersection operation
[3, 4, 5]


````

## 15) UNION OF TWO ARRAY

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	  Scanner s=new Scanner(System.in);
	  HashSet <Integer>  result=new HashSet<>();
	  System.out.println("Enter the size of the first array");
	  int n1=s.nextInt();
	  int a[]=new int[n1];
	  System.out.println("Enter the array element");
	  for(int i=0;i<n1;i++){
	      a[i]=s.nextInt();
	  }
	  System.out.println("Enter the size of the second array");
	  int n2=s.nextInt();
	  int b[]=new int[n2];
	  System.out.println("Enter the array element");
	  for(int i=0;i<n2;i++){
	      b[i]=s.nextInt();
	  }
	  
	  
	  for(int num:a){
	      result.add(num);
	  }
	  for( int num:b){
	      result.add(num);
	  }
	  System.out.println("UNION OF TWO ARRAY " +result);
	  
	}
}


output:

Enter the size of the first array
3
Enter the array element
2
3
4
Enter the size of the second array
3
Enter the array element
4
5
6
UNION OF TWO ARRAY [2, 3, 4, 5, 6]

````

## 16) FIND THE KTH SMALLEST ELEMENT IN AN ARRAY

````java[]


import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
        int k=s.nextInt();
        for(int i=0;i<n;i++){
            for(int j=i+1;j<n;j++){
                if(a[i]<a[j]){
                int temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
            }
        }
        System.out.println("After Sorting");
        for(int i=0;i<n;i++){
            System.out.print(a[i]+" ");
        }
        System.out.println(k+"th Smallest Element"+a[n-k]);

 }
	 }


OUTPUT:


Enter the size of the array
5
Enter the Elements
9
2
6
8
1
3
After Sorting
9 8 6 2 1
3th Smallest Element6

````

## 17) FIND THE ALL PAIR IN AN ARRAY THAT SUM UP TO A SPECIFIC VALUE

````JAVA[]



import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		System.out.println("Enter the target number");
		int target=s.nextInt();
       int left=0;
       int right=n-1;
       boolean found=false;
       while(left<=right){
           int sum=a[left]+a[right];
           if(sum==target){
               System.out.println("pair of element"+"("+a[left]+","+a[right]+")");
               found=true;
               left++;
               right--;
           }
           else if(sum<target){
               left++;
           }
           else{
               right--;
           }
           
       }
       if(!found){
           System.out.println("Not found");
       }
	     }
	 }

OUTPUT:

Enter the size of the array
6
Enter the Elements
1
4
6
8
10
12
Enter the target number
14
pair of element(4,10)
pair of element(6,8)



````

## 18) FIND THE PAIR WITH THE GIVEN SUM

````JAVA[]



import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the Elements");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		System.out.println("Enter the target number");
		int target=s.nextInt();
       int left=0;
       int right=n-1;
       boolean found=false;
       while(left<=right){
           int sum=a[left]+a[right];
           if(sum==target){
               System.out.println("pair of element"+"("+a[left]+","+a[right]+")");
               return;
           }
           else if(sum<target){
               left++;
           }
           else{
               right--;
           }
           
       }
           System.out.println("Not found");
	     }
	 }

output:

Enter the size of the array
6
Enter the Elements
1
4
6
8
10
12
Enter the target number
14
pair of element(4,10)

````

## 19) SUBARRAY WITH GIVEN SUM

````java[]

import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
		System.out.println("Enter the size of the array");
		int n=s.nextInt();
		int a[]=new int[n];
		System.out.println("Enter the array element");
		for(int i=0;i<n;i++){
		    a[i]=s.nextInt();
		}
		System.out.println("Enter the target value");
		int target=s.nextInt();
		
		int start=0;
		int sum=0;
		for(int end=0;end<n;end++){
		    sum+=a[end];
		
		while(sum>target && start<=end){
		    sum-=a[start];
		    start++;
		}
		if(sum==target){
		    System.out.println("subarray from index "+start+" to "+end);
		    System.out.println("Subarray Element");
		    for(int i=start;i<=end;i++){
		        System.out.print(a[i]+" ");
		    }
		    return;
		}
		}
		System.out.println("No subarray found");
	}
}


OUTPUT:

Enter the size of the array
6
Enter the array element
1
4
20
3
10
5
Enter the target value
33
subarray from index 2 to 4
Subarray Element
20 3 10

````
## MOVE ALL NAGATIVE NUMBERS TO ONE SIDE OF THE ARRAY

````java[]

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        
        System.out.println("Enter the array size:");
        int n = s.nextInt();
        
        int a[] = new int[n];
        System.out.println("Enter the array elements:");
        for (int j = 0; j < n; j++) {
            a[j] = s.nextInt();
        }
        
        int i=0;
        for(int j=0;j<n;j++){
            if(a[j]>0){
           int temp=a[j];
           a[j]=a[i];
           a[i]=temp;
           i++;
        }
        }

        System.out.println("After moving all negative numbers to the end:");
        for (int j = 0; j < n; j++) {
            System.out.print(a[j] + " ");
        }
    }
}

OUTPUT:

Enter the array size:
5
Enter the array elements:
7
-1
5
-2
-3
After moving all negative numbers to the end:
7 5 -1 -2 -3

````

## 




    







    



