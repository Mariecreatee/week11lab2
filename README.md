#include <iostream>
#include <vector>
#include <numeric>
#include <algorithm>


using namespace std;


//problem5
// vector<int> columnWiseSum(const vector<vector<int>>& matrix) {
//     if (matrix.empty() || matrix[0].empty()) {
//         return {};
//     }
//
//     int numRows = matrix.size();
//     int numCols = matrix[0].size();
//     vector<int> columnSums(numCols, 0);
//
//     for (int j = 0; j < numCols; ++j) {
//         for (int i = 0; i < numRows; ++i) {
//             columnSums[j] += matrix[i][j];
//         }
//     }
//     return columnSums;
// }
//
//
// int main() {
//     vector<vector<int>> matrix = {
//         {2, 3, 0},
//         {1, 2, 3},
//         {4, 5, 6}
//     };
//
//     vector<int> sums = columnWiseSum(matrix);
//
//     cout << "Column-wise sums: ";
//     for (size_t i = 0; i < sums.size(); ++i) {
//         cout << sums[i] << (i == sums.size() - 1 ? "" : " ");
//     }
//     cout << endl;
//
//     return 0;
// }


//problem6


// int diagonals(const vector<vector<int>>& matrix, int n) {
//     int sum = 0;
//     for (int i = 0; i < n; ++i) {
//         sum += matrix[i][i];
//     }
//     return sum;
// }
//
// int main() {
//     vector<vector<int>> matrix = {
//         {1, 2, 3},
//         {4, 5, 6},
//         {7, 8, 9}
//     };
//     int n = matrix.size();
//     int result = diagonals(matrix, n);
//     cout << "The sum of the main diagonal elements is: " << result<<endl;
//     return 0;
// }


//problem7


void printMatrix(const vector<vector<int>>& matrix) {
   for (const auto& row : matrix) {
       for (int val : row) {
           cout << val << " ";
       }
       cout << endl;
   }
}
int main() {
   vector<vector<int>> matrix = {
       {2, 3},
       {1, 2},
       {4, 5}
   };
   int M = matrix.size();  
   int N = matrix[0].size();
  
   vector<vector<int>> transpose(N, vector<int>(M));
  
   for (int i = 0; i < M; ++i) {
       for (int j = 0; j < N; ++j) {
           transpose[j][i] = matrix[i][j];
       }
   }
   cout << "Original Matrix:" << endl;
   printMatrix(matrix);
   cout << "\nTransposed Matrix:" << endl;
   printMatrix(transpose);
   return 0;
}


//problem8


void printMatrix(const vector<vector<int>>& matrix) {
   for (const auto& row : matrix) {
       for (int val : row) {
           cout << val << " ";
       }
       cout <<endl;
   }
}
int main() {
   int rows = 2;
   int cols = 2;
   vector<vector<int>> matrix1 = {
       {1, 2},
       {3, 4}
   };
   vector<vector<int>> matrix2 = {
       {5, 6},
       {7, 8}
   };
  
   vector<vector<int>> sumMatrix(rows, vector<int>(cols));
  
   for (int i = 0; i < rows; ++i) {
       for (int j = 0; j < cols; ++j) {
           sumMatrix[i][j] = matrix1[i][j] + matrix2[i][j];
       }
   }
   cout << "Sum of the two matrices:" <<endl;
   printMatrix(sumMatrix);
   return 0;
}




//problem9

vector<vector<int>> multiplyMatrices(const vector<vector<int>>& A, const vector<vector<int>>& B) {
   if (A.empty() || B.empty() || A[0].size() != B.size()) {
       return {};
   }
   int rowsA = A.size();
   int colsA = A[0].size();
   int rowsB = B.size();
   int colsB = B[0].size();
   vector<vector<int>> result(rowsA,vector<int>(colsB, 0));
}


//problem10


#include <vector>
#include <algorithm>


void rotate(std::vector<vector<int>>& matrix) {
   int n = matrix.size();
   for (int i = 0; i < n; ++i) {
       for (int j = i; j < n; ++j) {
           swap(matrix[i][j], matrix[j][i]);
       }
   }
   for (int i = 0; i < n; ++i) {
       reverse(matrix[i].begin(), matrix[i].end());
   }
}


//problem15


void removeElementByValue(std::vector<int>& nums, int val) {
   auto new_end = std::remove(nums.begin(), nums.end(), val)
   nums.erase(new_end, nums.end());
}


int main() {
   vector<int> input_vector = {6, 1, 2, 3, 2, 4, 2, 2};
   int value_to_remove = 2;
   cout << "Original vector: ";
   for (int num : input_vector) {
       cout << num << " ";
   }
   cout << endl;
   removeE(input_vector, value_to_remove);


   cout << "Vector after removing " << value_to_remove << ": ";
   for (int num : input_vector) {
       cout << num << " ";
   }
   cout << endl;
   return 0;
}




//problem19


int main() {
   vector<int> V = {5, 10, 20, 30, 40, 50};
   reverse(V.begin(), V.end());
   for (int element : V) {
       cout << element << " ";
   }
   cout << endl;
   return 0;
}
