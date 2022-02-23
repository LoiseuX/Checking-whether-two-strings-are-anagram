# Checking-whether-two-strings-are-anagram
    import java.util.Arrays;
    import java.util.Scanner;

    public class CheckingWhetherTwoStringsAreAnagram {
      public static void main(String[] args) {
        
        String a1 = null,a2 = null;
        
        //get input from the user
        //Scanner in = new Scanner(System.in);
        //System.out.print("Input first string: ");
        //String input1 = in.nextLine();
        //System.out.print("Input second string: ");
        //String input2= in.nextLine();
        //System.out.println("Result: " + anagramCheck(input1, input2));
        
        //given input
        String input1 = "Debit card";
        String input2 = "bad Credit";
        
        if(anagramCheck(input1, input2)){
            System.out.println("The strings are anagrams");
        }
        else {
            System.out.println("The strings are not Anagrams");
        }
    }
    static boolean anagramCheck(String input1, String input2){
        input1 = input1.toLowerCase().replace(" ", "");
        input2 =input2.toLowerCase().replace(" ", "");
        
        //checking length
        if (input1.length() != input2.length()){
        return false;
        }
        
        //transforms to arrays
        char charToArray1[] = input1.toCharArray();
        char charToArray2[] = input2.toCharArray();
        
        //sorting
        Arrays.sort(charToArray1);
        Arrays.sort(charToArray2);
        
        for (int x = 0; x < input1.length(); x++){
            if (charToArray1[x] != charToArray1[x]){
                return false;
            }
        }
        return true;
    }
    
}
