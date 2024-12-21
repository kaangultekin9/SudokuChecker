public class Main 
{
  public static boolean isValid (int[][] arr) {
   for(int i=0; i<arr.length; i++) { 
    for (int j=0; j<arr.length; j++) {
     for (int k=j+1; k< arr[i].length; k++) {
      if (arr[i][j]==arr[i][k]) {
      return false;
      }
     }  
    } 
   }

     for(int i=0; i<arr.length; i++) { 
     for (int j=0; j<arr.length; j++) {
     for (int k=j+1; k< arr[i].length; k++) {
      if (arr[j][i]==arr[k][i]) {
       return false;
        }
         }  
       }
     }
    return true;
  }


  //-------------
   public static void main(String[] args) {
   int[][] grid =
   {{5,3,4,6,7,8,9,1,2},
   {6,7,2,1,9,5,3,4,8},
   {1,9,8,3,4,2,5,6,7},
   {8,5,9,7,6,1,4,2,3},
   {4,2,6,8,5,3,7,9,1},
   {7,1,3,9,2,4,8,5,6},
   {9,6,1,5,3,7,2,8,4},
   {2,8,7,4,1,9,6,3,5},
   {3,4,5,2,8,6,1,7,9}
   };
     
  
  boolean result= isValid(grid);
  if (result ) {
  System.out.print("Tebrikler doğru");
  }
 else {
   System.out.print("Yanlis cozdunuz");
 }

  }
