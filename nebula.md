
import java.util.HashMap;
import java.util.Scanner;


class Quicksort{
    
 int partition(HashMap<Integer, String>hm,int l,int h)   //to sort wrt pivot
{ 
     String temp=new String();                                       //created temporary string
        String pivot=new String();                                    //created pivot string
        pivot=hm.get(h);                                                 // pivot is the highest index value
    int i = (l - 1);                                                           // Pointer Index of LeftList   
   
     
  for (int j = l; j <= h- 1; j++)                                        //j is traversal pointer
    { 
        
        if (hm.get(j).compareTo(pivot)<=0) 
        { 
            i++;                                                                 // increment left list index
            temp=hm.get(i);                                             //swap ith and jth element
        hm.put(i, hm.get(j));
        hm.put(j,temp);
        } 
    } 
    temp=hm.get(i+1);                                                //swap pivot and element at i+1 th position
        hm.put(i+1, hm.get(h));                                    //i.e. pivot is after the last element of LeftList
        hm.put(h,temp);
        
    return (i + 1); 
}
    

   
    
void QuickSort1(HashMap<Integer, String> hm, int l,int h) {
        
        int j;
        if(l<h)                                                      //loop until low is < than high value
        {
            j=partition(hm,l,h);                            //pivot value
            
            QuickSort1(hm,l,j-1);                         //sort left of pivot                               
            QuickSort1(hm,j+1,h);                       //sort right of pivot
            
            
        }
        
        
        
    }}
public class Nebula {
    public static void main(String args[])
    {int n; 
        Quicksort q=new Quicksort();                                                   //creating object of class Quicksort

        String s=new String();                                                                //creating String object s
        HashMap<Integer,String> hm;				//creating object hm of Generic class HashMap with Key:Integer Value:String
        hm = new HashMap<>();				//creating instance for object hm
        Scanner sc=new Scanner(System.in);                                       //sc  is instance for getting input
        
        System.out.println("How many value?");
        n=sc.nextInt();  					//n stores number of values
        
        for(int i=0;i<n;i++)
        {
        System.out.println("Enter value for key "+i);
        s=sc.next();                                                                             //s stores ith String value
        hm.put(i,s); 						//hm is updated with String s value for key i
 
        }
        
        q.QuickSort1(hm,0,n-1);                                 		 //function call with hm index 0 and index n-1 parameters
        
        for(int i=0;i<n;i++)
        {System.out.print(i); 					//key value printed in loop
        System.out.println(hm.get(i));				//value corresponding to key i is printed.
        
        }
        }
        
        
    }
    
  

