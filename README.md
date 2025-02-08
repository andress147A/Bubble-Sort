# Bubble-Sort
O Bubble Sort é um algoritmo de ordenação simples que compara e troca elementos adjacentes repetidamente até que a lista esteja ordenada. Seu nome vem do efeito de "bolhas" subindo ao topo. Apesar de fácil implementação, é ineficiente para grandes volumes de dados, pois tem complexidade O(n²) no pior caso.

public class BubbleSort {

    public static void bubbleSort(int[] arr) {
        int n = arr.length;
        boolean swapped;
        for (int i = 0; i < n - 1; i++) {
            swapped = false;
            System.out.println("Iteração " + (i + 1) + ":");
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {                  
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                    swapped = true;
                }
                printArray(arr);
            }
              if (!swapped) {
                break;
            }
            System.out.println();
        }
    }
    public static void main(String[] args) {
        int[] arr = {64, 34, 25, 12, 22, 11, 90};

        System.out.println("Array antes da ordenação:");
        printArray(arr);
        System.out.println();

        bubbleSort(arr);

        System.out.println("\nArray após a ordenação:");
        printArray(arr);
    }
    public static void printArray(int[] arr) {
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
    }
}

