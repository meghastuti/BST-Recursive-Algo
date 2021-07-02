 public class BinarySearch {				
    int binarySearch(int arr[],int left,int right,int search)				
    {				
      		
      if (left <=right)
    
         {				
            int mid = (right +left) / 2;				
 				
           if (arr[mid] == search)				
				return mid;
				
			if (arr[mid] < search)	
				return binarySearch(arr, mid + 1, right, search);
				
			if (arr[mid] > search)	
			return binarySearch(arr, left, mid - 1, search);
        }				
         return -1;				
   }				
  				
    public static void main(String args[])				
    {				
       	BinarySearch tree = new BinarySearch();			
		int arr[] = { 2, 3, 4, 15, 25, 40, 60, 70 };	
		int search = 40;
		int left = 0; 
		int right = arr.length - 1;
		int result = tree.binarySearch(arr,left,right,search);		
		if (result == -1)		
			System.out.println("Element not present");	
		else		
			System.out.println("Element index " + result);	
    }				
}				
				
