public class PeakElement {
    public static int arrayInput(int n,int[] intArray) {


        int index = 0;
        if(n==1){
            return 0;
        }
        if (intArray[0] >= intArray[1])
            return 0;
        if (intArray[n - 1] >= intArray[n - 2])
            return n - 1;

        if (1 <= n && n <= 100000 && intArray.length >= 1 && intArray.length <= 1000000) {
            for (int i = 0; i < intArray.length-1; i++) {
                if (intArray[i] >= intArray[i + 1] && intArray[i] >= intArray[i - 1]) {
                    index = intArray[i];

                    return index;

                }


            }


        }
        for (int i = 0; i < intArray.length; i++)
            if (i == index) {
                System.out.println('1');
            }

        else System.out.println('2');


        return index;
    }


}
public class Main {
    public static void main(String[] args) {
         int[] intArray={3,2,5};

         int n=intArray.length;
         PeakElement peak=new PeakElement();
        System.out.println("The index is "+peak.arrayInput(n,intArray) );







    }






}

