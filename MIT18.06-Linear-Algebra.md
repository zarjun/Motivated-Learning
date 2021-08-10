- [Lecture 1](#lecture-1)
- [Lecture 2](#lecture-2)
- [Lecture 3](#lecture-3)



## Lecture 1 ##

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


## Lecture 2 ##

Test:Elimination to solve equation

* Back-Substitution
* Elimination Matrices
* Matrix multiplication

Ax=b example  

| 1 2 1 |             
| 3 8 1 | = A          
| 0 4 1 |                            
     
**Matrix operation**

| 1 2  1 |                                    
| 0 2 -2 |  
| 0 4  1 |  

**Matrix operation**

| 1 2  1 |  
| 0 2 -2 |  = U  
| 0 0  5 | 

* The purpose of elimination is to knock out ‘x’part;  
* The first number of the first row(num‘1’) we call the (first)pivot;   
* The second pivot is position(2,2)(row 2 column 2)（num'2'），2 times second row and get subtracted  from the third row;  （pivot can't be 0）
* Matrix U stand for **upper triangular**；  

* Failure ：if the first num was 0,we can exchange the row and then we make elimination（0 can't not be pivot）;    
* Augmented matrix(has column 'b')；  
* Back-Substitution：a simple step solving the equation in reverse order because the system is upper triangular；


| 1 2  1 |       
| 0 2 -2 |  = U    
| 0 0  5 |        

| 1 2  1   2|  
| 0 2 -2   6| = c  
| 0 0  5  10|  

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

Inverses  
E-1(inverse)*E=I（identity）

## Lecture 3 ##


