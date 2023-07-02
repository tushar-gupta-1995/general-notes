# Vectors
Vectors are just representing direction AND magnitude and NOT position. Therefore it is possible to shift position of vector without changing the meaning of vector. As long as direction and magnitude is preserved, its the same vector regardless of position.

# Linear independence
Two or more vectors are said to be linearly independent if none of them can be written as a linear combination of the others. On the contrary, if at least one of them can be written as a linear combination of the others, then they are said to be linearly dependent.**example:** consider a x-y plane where x is the horizontal axis and y is the vertical axis.
Now a vector say 2x+3y, is not linearly independent or linearly dependent on the x-y plane.
But a third axis orthogonal to x-y plane, lets say z axis cannot be represent in any linear equation of the x-y plane.
**summary:** therefore, a set of vectors {v1, v2, v3} is linear indipendent, if v3 cannot be written as cv1 + cv2.

# basis vectors and vector space
A set of linearly independent vectors, determine how an object moves in the vector space.
vector space is the space covered by the bounds of linear combination of the vectors.

# Vector Representation
a vector is represented by a column of values.each component of vector represents a movement in a unique direction.
the magnitude of direction in each component is the {value of each component * the unit vector in that direction}
The resultant direction is the summation of vector additions of each component.

# Types of vector transformation
## Vector scaling
Scaling a vector is multiplying a vector with a scalar quantity. scaling is like stretching the vector without changing anything else.
So if a vector points in the same direction, but its magnitude increases, it is being scaled.
### Method:
Multiply the vector by scalar.

## Vector rotation
Rotating a vector is changing vector direction without changing its magnitude. So while scaling changes the magnitude but not direction,
rotation changes the direction but not magnitude.
### Method:
Convention is to multiply a vector with the below rotation matrix.
since cos^2θ + sin^2θ=1 the magnitude remains same but matrix changes direction.
| cos(θ) -sin(θ) |
| sin(θ) cos(θ) |

## Vector shearing
Shearing a vector is keeping one component constant but changing the other component's magnitude.
Example take a 2d vector, it can have a component in x-y plane. if we increase the magnitude of y, the vector's direction will change towards y, but it will have same component in x. The overall vector magnitude and direction may change but the component in x remains the same.This is shearing.
### Method
| 1 x |
| 0 1 |


# Vector Addition
Remember in a vector the position does not matter.
Assume walking 1 km in north and **THEN** 1 km in south from an **origin point** and reach a **destination point**
Draw a straight line from **origin** to **destination** and thats your summation vector or vector addition of 1km north and 1km south.
Notice the addition is commutative that is 1S + 1N = as !N + 1S.
Refer the image for more detail:
![vector addition notes](images/vector-addition.jpeg)



