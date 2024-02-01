# Task1
    using System;

    class Queen
    {
     static void main()
     {
        int rows = 8;
        int cols = 8;
        
        int[,] matrix = new int[rows, cols];
        
        int startRow = 0;
        int startCol = 4;
        
        matrix[startRow, startCol] = 1;
        
        int[] rowMoves = {2,2,1,1 };
        int[] colMoves = {-1, 1,2,-2 };
        
        for (int i = 0; i < 4; i++)
        {
            int newRow = startRow + rowMoves[i];
            int newCol = startCol + colMoves[i];

           
            if (newRow >= 0 && newRow < rows && newCol >= 0 && newCol < cols)
            {
                matrix[newRow, newCol] = 1;
            }
        }
        
        for (int i = 0; i < rows; i++)
        {
            for (int j = 0; j < cols; j++)
            {
                Console.Write(matrix[i, j] + " ");
            }
            Console.WriteLine();
        }
    }
}

