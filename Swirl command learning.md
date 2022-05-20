# Project 1
Swirl learning


## Class 1
> Basic R

## Class 2
> Workspace and file
- getwd() --- assign the value of the current working directory to a variable
- ls() --- List all the objects in your local workspace
- list.files() --- List all the files in your working directory
- args() --- Displays the argument names and corresponding default values of a function or primitive
- dir.create("file name") -- create a directory in the current working directory called "filename",
- to make nested directories, use dir.create(file.path("a","b"), recursive = TRUE) to create b in file path a/b
- file.create("file name") -- Create a file in your working directory called "file name"
- list.files() -- produce a character vector of the names of files or directories in the named directory
- file.exist("file name") -- check if "file name" exists in the working directory
- file.info("file name") -- Access information about the file "file name"
- file.info would contain size, isdir (Is the file a directory?), mode, mtime, ctime, atime (file modification, ‘last status change’ and last access times),
- uid (the user ID of the file's owner), gid (the group ID of the file's group), uname, grname. Use $ to look at specific function
- file.rename("previous name","new name") <- rename file
- file.remove("file name") <- remove file named "filename"
- file.copy(a,b) <- make a file copy of a named b
- file.path("filename.R") <- provide relative path to file "filename.R"
- file.path("folder1","folder2",fsep = "\\") <- construct file and directory paths that are independent of the operating system your R code is running on.
- Make file path folder1/folder2

## Class 3
> Sequences of numbers
- 1:20 --> give every integer between 1 and 20; 15:1 will give integer in downward trend
- pi:10 --> vector or real number starting with pi and increase in increment of 1
- ? function_name --> give you help of particular function, however, for operators, press 'operators' (eg. ?':')
- seq(a,b by=1, length = n) --> similar to 'a:b', by= control the increment, length = control the number of numbers in vectors,
- along.with = vector_a would set a sequence with same length of vector_a
- seq_along(vector_a) <- set a sequence with same length of vector_a
- length(vector1) <- give you the length of the vector
- rep (a, times = 3) <- create a vector of a,a,a (a could be a vector itself)
- rep (a (eg c(1,2,3)), each = 3) <- create a vector of 111222333

## Class 4
> Vectors
- tf <- num_vec (vector name) < 1 -- give you a vector of 4 logical values state which elements of the vector is smaller than 1
- logical operator -- "<", ">", "<=","==","!="(check for inequality)
- A|B -- union of A and B, at least one is true
- A&B -- intersection of A and B, both A and B are true
- paste(,collapse=" ") <- join together the elements of vectors, collapse = " ", collapse by " "
- paste(,sep= " ") <- join together the elements of vectors, sep = " ", separate by " "

## Class 5
> Missing Values
- is.na() <- whether each element of a vector is NA
- NaN: not a number; NA is not a value, (NA can be >0 or <0)
- ! give us the negation of a logical expression

## Class 6
> Subsetting Vectors
- eg: x <- c(1,2,3), x[c(T,F,F)] will give you output 1
- [] -- index a vector, it will return the vector's element when the index is True
- x[is.na(x)] -- will return all missing value from x
- x[!is.na(x)] -- will capture all non-missing values from x
- In R, first element of a vector is considered as element 1, if exceed the number of elements, the output would be NA
- x[c(-2,-10)] -- will give you all values in the vector except 2 and 10. It is the same as x[-c(2,10)]
- c(foo=11, bar=2, norf=NA) -- assign each element with a name
- names(vector) -- print out the names for a vector
- identical (a,b) -- test if variable a and b is exactly same

## Class 7
> Matrices and data frames
- dim() -- tell the dimension of the objects, the number of row and column (first number row, second number column)
- Note: vector does not have dimension, can use length. However we can assign dimension to vectors
- attributes() -- look at the attributes of an object, matrix will have a dim attribute
- class() -- find object's class attributes. Without giving name, it will display implicit class (eg. Matrix)
- matrix(data, nrow, ncol) -- create matrix
- cbind() -- combine a sequence of vector/matrix/data-frame by columns
- rbind() --  combine a sequence of vector/matrix/data-frame by row
- data.frame() --make dataframe using vectors
- colnames(dataframe) <- vector containing names

## Class 8
> Logic
- AND operator: & and &&(&& version of AND only evaluates the first member of a vector)
- eg. TRUE & c(TRUE, FALSE, FALSE) -- output "TRUE, FALSE, FALSE" (Left TRUE is recycled across every element of right)
- TRUE && c(TRUE, FALSE, FALSE) -- output "TRUE" (Left TRUE is recycled only with first element of right)
- OR operator: | and || (|| only evaluates first member)
- Note: If both and either side are TRUE, output is TRUE; If neither are TRUE, then expression will be FALSE
- eg. TRUE | c(TRUE, FALSE, FALSE) -- output "TRUE, TRUE, TRUE"
- isTRUE() -- Evaluate if the augment is true
- xor() -- Exclusive OR (If one argument evaluates to TRUE and one evaluates to FALSE, then it will return TRUE; Otherwise it will return FALSE)
- sample() -- create a random sampling of integers
- which(a > 7) -- find the indices of vector a that are greater than 7
- any() -- if one or more of the elements in logical vector is true, return TRUE
- all() -- if every element in logical vector is TRUE, return TRUE

## Class 9
> Functions
