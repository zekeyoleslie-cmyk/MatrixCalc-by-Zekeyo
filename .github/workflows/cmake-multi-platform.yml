#include<iostream>  
using namespace std;  
  
int main () {  
    int rowsA,colsA,rowsB,colsB;  
      
    cout <<"============MATRIX CALCULATOR============="<< "\n\n\n";  
      
    //entering the number of rows and columns of matrices A and B  
    cout  <<  "Enter row  for MatrixA:  ";  
    cin >> rowsA;  
    cout << "Enter column for Matrix A:  ";  
    cin >> colsA;  
      
cout <<"\n";  
  
cout << "Enter rows for MatrixB:  " ;  
cin >>rowsB;  
cout <<"Enter columns for Matrix B:  ";  
cin >> colsB;  
  
cout <<"\n";  
  
int A[10][10], B[10][10];  
  
//Input elements for matrix A  
cout <<"Enter the elements for matrix A: \n";  
for(int i=0;i < rowsA; i++){  
    for(int j=0;j < colsA; j++){  
        cin >> A[i][j];  
    }  
}  
  
//Input elements for matrix B  
cout <<"Enter the elements for matrix B: \n";  
for(int i=0;i<rowsB;i++){  
    for(int j=0;j<colsB;j++){  
        cin >> B[i][j];  
    }  
}  
int choice;  
  
cout << "\nChoose Operation:\n";  
cout << "1. Addition\n";  
cout << "2. Subtraction\n";  
cout << "3. Multiplication\n";  
cout << "4. Transpose of A\n";  
cout << "5. Transpose of B\n";  
cout << "6. Det of a 3x3 matrix\n";  
cout << "7. Inverse of a 3x3 matrix\n";  
cin >> choice;  
  
cout << "You chose option " << choice << ": ";  
switch(choice){  
case 1:  
//Matrix Addition  
if(rowsA != rowsB || colsA != colsB){  
    cout << "Matrix Addition not possible";  
} else {  
   int Sum[10][10] ;  
   cout << "The Sum of the matrix addition is: \n";  
   for(int i=0;i<rowsA;i++){  
       for(int j=0;j<colsA;j++){  
           Sum[i][j]=A[i][j] + B[i][j];  
           cout << Sum[i][j] << "  ";  
       }  
       cout <<"\n";  
   }  
}  
break;  
  
case 2:  
//Matrix Subtraction  
if(rowsA != rowsB || colsA != colsB){  
    cout << "Matrix Subtraction not possible";  
} else {  
   int Difference [10][10] ;  
   cout << "The Difference of the matrix subtraction is: \n";  
   for(int i=0;i<rowsA;i++){  
       for(int j=0;j<colsA;j++){  
           Difference[i][j]=A[i][j] - B[i][j];  
           cout << Difference [i][j] << "  ";  
       }  
       cout <<"\n";  
   }  
}  
break;  
  
case 3:  
//Matrix Multiplication   
if(colsA != rowsB){  
    cout << "Matrix Multiplication not possible ";  
}else{  
    int Product[10][10];  
    cout << "The Product of the matrix multiplication is: \n";  
    for(int i=0;i<rowsA;i++){  
        for(int j=0;j<colsB;j++){  
            Product[i][j]=0;  
            for(int k=0;k<colsA;k++){  
                Product[i][j] += A[i][k] * B[k][j];  
                }  
                cout << Product[i][j] << " ";  
                }  
            cout <<"\n";  
    }  
}  
break;  
  
case 4:  
//Transpose of Matrix A  
int TransposeA[10][10];   
cout << "Transpose for Matrix A" << "\n";  
for(int i=0;i<colsA;i++){  
    for(int j=0;j<rowsA;j++){  
        TransposeA [i][j]= A[j][i];  
    cout << TransposeA[i][j] << " ";  
}  
cout <<"\n";  
}  
break;  
  
case 5:  
//Transpose of Matrix B  
int TransposeB[10][10];   
cout << "Transpose for Matrix B" << "\n";  
for(int i=0;i<colsB;i++){  
    for(int j=0;j<rowsB;j++){  
        TransposeB[i][j]= B[j][i];  
    cout << TransposeB[i][j] << " ";  
}  
cout <<"\n";  
}  
break;  
  
case 6:  
//Calculating the determinant of 3x3 matrix  
if(rowsA != 3 || colsA != 3){  
    cout << "Determinant does exit matrix must be a Square matrix";  
}else{  
    int  determinant = A[0][0]*(A[1][1]*A[2][2] - A[1][2]*A[2][1])  
            -A[0][1]*(A[1][0]*A[2][2] - A[0][2]*A[1][0])  
            +A[0][2]*(A[1][0]*A[2][1] - A[1][1]*A[2][0]);  
              
            cout << determinant << " ";  
}  
cout << "\n";  
break;  
  
  
case 7:  
{  
//Calculating the inverse of a matrix  
int determinant = A[0][0]*(A[1][1]*A[2][2] - A[1][2]*A[2][1])  
            -A[0][1]*(A[1][0]*A[2][2] - A[0][2]*A[1][0])  
            +A[0][2]*(A[1][0]*A[2][1] - A[1][1]*A[2][0]);  
            cout << determinant << " ";  
cout << "\n";  
if(determinant == 0){  
    cout << "Matrix has no inverse";  
 break;  
}  
    //Calculating the cofactor  
   float    cof [3][3];  
   cof[0][0] = (A[1][1]*A[2][2] - A[1][2]*A[2][1]);  
   cof[0][1] = - (A[1][0]*A[2][2] - A[1][2]*A[2][0]);  
   cof[0][2] = (A[1][0]*A[2][1] - A[1][1]*A[2][0]);  
     
   cof[1][0] = - (A[0][1]*A[2][2] - A[0][2]*A[2][1]);  
   cof[1][1] = (A[0][0]*A[2][2] - A[0][2]*A[2][0]);  
   cof[1][2] = - (A[0][0]*A[2][1] - A[0][1]*A[2][0]);  
     
   cof[2][0] = (A[0][1]*A[1][2] - A[0][2]*A[1][1]);  
   cof[2][1] = - (A[0][0]*A[1][2] - A[0][2]*A[1][0]);  
   cof[2][2] = (A[0][0]*A[1][1] - A[0][1]*A[1][0]);  
     
   //Calculating rhe adjugate    
   float adjugate [3][3];  
   for(int i=0;i<3;i++)  
       for(int j=0;j<3;j++)  
           adjugate[i][j] = cof[j][i];  
       // Calculating the inverse  
       cout << "Inverse of matrix is: \n";  
  for(int i=0;i<3;i++){  
      for(int j=0;j<3;j++){  
          cout << adjugate[i][j] / determinant << " ";  
      }  
      cout << "\n";  
  }  
break;  
}  
default:   
cout << "Invalid option";  
    return 0;  
}  
}  
