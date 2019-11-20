# HW3

HW3
//1

 public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        System.out.println("Введите высоту фигуры");
        int height = sc.nextInt();
        sc.close();
        int b = 1;
        for (int i = 1; i <= height; ++i) {
            System.out.print("*");
            if (b <=i&&b<height) {
                System.out.println();
                b++;
                i = 0;
            }
            if (height==i){
                System.out.println();
                height--;
                i=0;
            }

        }
    }
}


//2

import java.util.Scanner;

public class Hello {


    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Введите количество полос: ");
        int x = sc.nextInt();
        int i, j;

        for ( j = 0 ; j <= x ; j++) {
            for (i = 0; i < 4; i++) {
                System.out.print("***");
                System.out.print("+++");
            }
            System.out.println(" ");
        }
        }

}

//3
import java.util.Scanner;

public class Hello {


    public static void main(String[] args) {
    	int[] array = new int[10];
    	for (int i = 0; i < array.length; i++) {
    	    array[i] = (int) Math.round((Math.random() * 30) - 15);
    	    System.out.println(array[i]);
    	}
        }

}

//4

public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		
		System.out.println("Введите размерность квадратной матрицы (от 2 до 5):");
		String dimension = scanner.nextLine();
		scanner.close();
		
		if(dimension.equals("2")) 
		{
			int[][] kubik =
				{
						{1, 1},
						{2, 2}
				};
			turnArray(kubik);
		}
		else if(dimension.equals("3"))
		{
			int[][] kubik =
				{
						{1, 1, 1},
						{2, 2, 2}, 
						{3, 3, 3}
				};
			turnArray(kubik);
		}
		else if(dimension.equals("4"))
		{
			int[][] kubik =
				{
						{1, 1, 1, 1},
						{2, 2, 2, 2}, 
						{3, 3, 3, 3},
						{4, 4, 4, 4},
				};
			turnArray(kubik);
		}
		else if(dimension.equals("5"))
		{
			int[][] kubik =
				{
						{1, 1, 1, 1, 1},
						{2, 2, 2, 2, 2}, 
						{3, 3, 3, 3, 3},
						{4, 4, 4, 4, 4},
						{5, 5, 5, 5, 5},
				};
			turnArray(kubik);
		}
		else System.out.println("Для наглядности работы кода введите число от 2 до 5!");
		}
		
		static void turnArray(int[][] arr){
			System.out.println("Ваша первоначальная матрица:");
		for(int i = 0; i < arr.length; i++)
		{
			for(int j = 0; j < arr[i].length; j++)
			{
				System.out.print(arr[i][j] + " " );
			}
			System.out.println();
		}
		
		System.out.println();
		System.out.println("Поворот матрицы на 90 градусов:");
		for(int j = 0; j < arr.length; j++)
		{
			for(int i = arr.length-1; i >= 0; i--)
			{
				System.out.print(arr[i][j] + " " );
			}
			System.out.println();
		}
		
		System.out.println();
		System.out.println("Поворот матрицы на 180 градусов:");
		for(int i = arr.length-1; i > -1; i--) 
		{
			for(int j = 0; j < arr[i].length; j++)
			{
				System.out.print(arr[i][j] + " " );
			}
			System.out.println();
		}
		
		System.out.println();
		System.out.println("Поворот матрицы на 270 градусов:");
		for(int j = arr.length-1; j >=0; j--)
		{
			for(int i = 0; i < arr.length; i++)
			{
				System.out.print(arr[i][j] + " " );
			}
			System.out.println();
		}
	}
}
