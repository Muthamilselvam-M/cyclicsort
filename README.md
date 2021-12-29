# cyclicsort


import java.util.Arrays;
public class Main{
    public static void main(String[] args){
        int[] arr = {1,3,4,2,5};
        cyclic(arr);
        System.out.println(Arrays.toString(arr));
    }
    public static void cyclic(int[] arr){
        int i = 0;
        while(i<arr.length){
            int correct = arr[i] - 1;
            if (arr[i] != arr[correct]){
                swap(arr,i,correct);
                
            } 
            else{
                i++;
            }
        }
    }
    public static void swap(int[] arr,int one,int two){
        int temp = arr[one];
        arr[one] = arr[two];
        arr[two] = temp;
    }
}
