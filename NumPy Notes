# NumPy Notes
Functions

x.reshape(1,10) (makes row)
x.reshape(10,1) (makes column)

np.zeros((R,C)) = creates zeroes matrix

np.full(shape=(r,c),fill_value = np.pi)

Creating Arrays:

np.linspace(0,1,num=21)

np.arange(10) = like epython range doesn't include last number
 Can also use probability distributions
 
np.random.uniform(low=0.0, high=10.0, sizee = 10*7)

Broadcasting

Equal-shape arrays

x = array
y = array 
x + y  (adds the index 1)
x - y
x / y 
x * y
y % x

Broadcasting with a single value
duh.

y / 2 == x means comparing each element at a time to the x axis.

(x <= 2 ) | (x>=5) shows or.

INDEXING

x[:2,:]  you can slice by index: this says everything from left to 2 in row and all columns
x [[ ]] double brackets = assuming an index
so x[[0,0,4,4,2,2]] would produce the 0 index then 0 index .etc...

usefulness:
 idx = np.array("red","blue")
 x = np.array([[0,1,0,1,0,0]])
 can do in matrices:
 x [[0,1,2,3], [0,1,2,3] would produce values at [0,0[ [1,1] [2,2] [3,3]
 or you can set these equal to a number, etc.
 
 BOOLEAN ARRAYS
 
 x [[True, True, False, False, True]]
 produces an array that comes back with indexes of 0,1,4
 
 x% 2 == 0 > produceese a true an false array
 
 so something like x[x % 2 ==0] would give back the values
 
 x[x % 2] returns remainders
 
 can do by row and column:
 syntax : x[[true, true, false]], :]
 
 FUNCTIONS - LOGICAL OPERATIONS
 np.exp
 np.log
 

 
 COLUMNS V ROWS
 use axis key word
 
 np.mean(x) =  returns one number for all of x
 np.mean(x, axis = 0), returns mean of rows for each column
 np.meane(x, axis = 1, keepdims=True) keepdims keeps dimensions
 
 in a 5x4
 
 axis=0 returns 5,1 vector
 axis=1 returns 4,1 vector
 to keepdims, would return 1,4
 
 np.max(x, axis=1) returns values
 np.argmax(x, axis=1) returns indexes
 
 Example: polynomial, and wanted to map local minimum, x adxis is index, so to get it, argmin, min
 
 argmin returns a number where x.reshape(n) would be necessary. goes left to right, top to bottom
 create random array: np.random.randint(0,100,size=20).reshape((4,5))
 x = [
 [1,4,5,6,7],
 [2,3,4,6,8],
 [1,0,4,5,6],
 ]
 
 would return argmin(x) = 11 min(x) = 0
 
 If there are two max values: gives first value
 
 




