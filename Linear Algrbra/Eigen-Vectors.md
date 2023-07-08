# Pre-Requisites
Refer [vector transformations](https://github.com/tushar-gupta-1995/general-notes/blob/main/Linear%20Algrbra/Vector-Transformations.md) for covering the pre-requisites.


# Definition
If on applying a vector transformation (multiplication of matrix), the vector span changes it is not an eigenvector.
**Remember** span is either same direction or exact opposite direction
## Refer:

![eigen vector example](images/eigen_vector_example.JPG)


# Here is a neat idea called Diagonalization
Imagine a particle which changes its position by a given 2d matrix---------------Lets call this T
the given 2d matrix here is the basis which when applied gives the new position of the particle.
now imagine we are also given the rate of this change, say the position changes every 2 seconds.
Now we are to find the position of particle at 100th second...this implies transforming the current position by T to the power 100.
this will be a tricky calculation.

## Lets try to find a general simplification to this solution 
Imagine finding the `eigenvector` of the transformation matrix.
Remember `eigenvector` is that vector which when transformed by a matrix, lies in its span.
Thus the multiplication of `eigenvector` by transformation matrix is just a scaled version of the `eigenvector` and the magnitude(lambda) of the scale is `eigenvalue`.
### Example
Now imagine the transformation matrix being a 3d matrix, so its composed of 3 vectors( the columns of the matrix), lets call it `T`
we find an eigenvector corresponding to each of the 3 vectors and get a new 3d matrix, lets call it the `eigenmatrix`, lets call it `C`
NOW when we apply the transformation to the `eigenmatrix`, we get 3 vectors with only non zero elements on the diagonal, representing each vector from the original `eigenmatrix` being scaled, lets call it `D`
Now when we multiply transformation matrix by eigenmatrix that is `TC`, we just get `D`.
ONly one thing is left, `D` is just `C` being scaled, but `C` itself needs to be braught back to the original basis, which can be done by multiplying by `C inverse`.
Thus D=`C inverse`* `T` * `C`



Now this simplifies the problem a lot, 

we first find 

