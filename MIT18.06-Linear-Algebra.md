- [Lecture 1  (equations/column picture/matrix)](#lecture-1)
- [Lecture 2  (back-substitution/elimination/multiplication)](#lecture-2)
- [Lecture 3		(multiple/inverse)](#lecture-3)


## Lecture 1 (equations/column picture/matrix) ##   

Teacher：Professor Gilbert Strang  
Text: Introduction to Liner Algebra  
Exercise/Matlab/syllbus/video: **[https://mitmath.github.io/1806/](https://mitmath.github.io/1806/)**

* n liner equations,n unknowns
* Column picture
* Matrix form

Example one: (two by two system)   
2x-y=0  
-x+2y=3  

* write down the Matrix form;
* To draw their Row picture;  
* We find a important point that lies on both lines(solve both equations)  
* To draw their Column picture;  
(find liner combination of columns: column one and two multiply some right number and add,to get the vector right hand of equal )  
* **[What will happen if all x and y were shown]**

Example two: (three by three system)  
2x-y+0z=0  
-x+2y-z=-1  
0x-3y+4z=4  

* write down the Matrix form;
* To draw their Row picture;
* Put all the points that satisfy that equation one and two(bunch of point become a plane\_one)  
* Again second equation meet at a plane\_two (plane\_one and plane\_two just give a line)  
* Final three thing(plane\_one two three) meet at a point;  
* To draw their Column picture;(we got three column and each one is a three dimesional vector)  
* How to combine three columns into the right-hand side;  
* **[Could solve Ax=b（any slutions） for every b == do the liner combinations of the columns fill three dimensional space]**   
(non-singular matrix,invertible matrix)  
* Ax=b mean 'A' times ‘x’,multiply a matrix by a vector,to find right-hand side 'b';  
* Each row multiply a column (dot product);  


## Lecture 2 (back-substitution/elimination(消元法)/multiplication) ##    

Test:Elimination to solve equation

* Back-Substitution
* Elimination Matrices
* Matrix multiplication

Ax=b example  
![](juzhen1.png) Matrix A                         
     
**Matrix operation**

![](juzhen2.png)

**Matrix operation**

![](juzhen3.png) Matrix U

* The purpose of elimination is to knock out ‘x’part;  
* The first number of the first row(num‘1’) we call the (first)pivot;   
* The second pivot is position(2,2)(row 2 column 2)（num'2'），2 times second row and get subtracted  from the third row;  （pivot can't be 0）
* Matrix U stand for **upper triangular**；  

* Failure ：if the first num was 0,we can exchange the row and then we make elimination（0 can't not be pivot）;    
* Augmented matrix(has column 'b')；  
* Back-Substitution（回代）：a simple step solving the equation in reverse order because the system is upper triangular；

![](juzhen3.png) Matrix U     

![](juzhen4.png) Matrix C  

**z=-2;y=1;x=2**

* Right column in the Matrix stands for the combination of column;
* Left column in the Matrix stands fof the combination of parallel thing of row;
example :

| 1 2 7 | * Matrix A（3* 3）    
= 1* row1+2* row2+7*row3 (a linear combination of rows);  

| 1 0 0 | * Matrix A（3*3）  
= we only need row1;  

| -3 1 1 | * Matrix A（3*3）  
= subtract 3 times of row1 from row2;  

* num in position(2,3) mean row2 in left one times column3 in right one;（dot product）  
* We call it E for elementary of elimination;  
* E21 mean its the matrix we needed to get 21 position to be 0;  
* **Mutiplier on left doing row operation，mutiplier on right doing column operation**  
* Can't exchange order of these (mutiplied)matrices ，but can move the parentheses；  
* Permutation：  exchange row and column；		
* Inverses：E-1(inverse)*E=I（identity）

## Lecture 3 ##

* Matrix multiplication(4 ways!?)
* Inverse of A AB AT
* Gauss-Jordan/find A-1

* The condition if two matrices can be multipled；（m x n and n x p）
* Three ways to multiple two matrices ：AB=C
	1.  C34 equal row3 of A multiple Colum4 of B;
	1.  several columns multipling by A； **[A]\*[|||]=[|||]**
		* matrix C can be regard as combinations of these columns；
	* From the row view;
	* The fourth way to multiple a two matrices as belows；（combination of vectors）	
	* The Firth Multiple by blocks；(A1/A2/A3/A4 with B1/B2/B3/B4)
- ![](juzhen5.png)  
	* all rows are in the same direction；
	* all columns are in the same direction；
* Inverses(invertible or non-singular)	
* No Inverses(or singular) 	**can find a vector X with Ax=0**	
* Gauss-Jordan（slove 2 equstion at once）
	* Gauss
	* Jordan
* EA=I tell us "E=A-1"；