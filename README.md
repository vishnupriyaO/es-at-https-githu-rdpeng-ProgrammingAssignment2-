# es-at-https-githu-rdpeng-ProgrammingAssignment2-
#R programming assignment2
makeCacheMatrix <- function(x = matrix()) 
{
   inv <-NULL
   SET <-function(y){
   x <<- y
   inv <<- NULL
   }
   get <-function() {
   x
   }
   get <- function()
   {x}
   setInverse <- function(inverse)
   {
   inv <<- inverse
   }
   getInverse <- function()
   {inv}
   list(set = set, get = get, setInverse = setInverse,  getInverse = getInverse )
   
}

cacheSolve <- function(x, ...)
{
      inv <-x$get()
      if(!is.null(inv))
      {
       message("getting cached data")
       return(inv)
       }
       mat <- x$get()
       inv <- solve(mat, ...)
       x$setInverse(inv)
       inv
}
