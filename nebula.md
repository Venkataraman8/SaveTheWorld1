
import java.util.HashMap;
import java.util.Scanner;


class Quicksort{
    
 int partition(HashMap<Integer, String>hm,int l,int h)   
{ 
     String temp=new String();                                       
        String pivot=new String();                                    
        pivot=hm.get(h);                                                
    int i = (l - 1);                                                            
   
     
  for (int j = l; j <= h- 1; j++)                                        
    { 
        
        if (hm.get(j).compareTo(pivot)<=0) 
        { 
            i++;                                                                 
            temp=hm.get(i);                                             
        hm.put(i, hm.get(j));
        hm.put(j,temp);
        } 
    } 
    temp=hm.get(i+1);                                               
        hm.put(i+1, hm.get(h));                                   
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
        Quicksort q=new Quicksort();                                                   

        String s=new String();                                                               
        HashMap<Integer,String> hm;				
        hm = new HashMap<>();				
        Scanner sc=new Scanner(System.in);                                       
        
        System.out.println("How many value?");
        n=sc.nextInt();  					
        
        for(int i=0;i<n;i++)
        {
        System.out.println("Enter value for key "+i);
        s=sc.next();                                                                             
        hm.put(i,s); 						
 
        }
        
        q.QuickSort1(hm,0,n-1);                                 		         
        for(int i=0;i<n;i++)
        {System.out.print(i); 					
        System.out.println(hm.get(i));				
        
        }
        }
        
        
    }
    
  

