For this assignment we will be modifying a simple image convolution program that can load an image and apply a standard filter to that image.  The program will output the results as a png image called output.png.  Available filters are: edge detection, sharpen, blur, gaussian, emboss, identity).  These are RUDIMENTARY filters, and results are very poor compared to most commercial software, but it is sufficient to play with for our purposes.  I have provided some pictures for you to work with, but you can try your own as well. 


Step 2: pthreads

Modify the program image.c to make it multi-threaded using pthreads.  You may do this any way you wish, but you must make sure you avoid race conditions, and that your choice of what to parallelize and how to parallelize it makes sense.  Compile your code with -lthread and see what the results of your parallelization.  Remember to commit and push your solution back to gitlab.

Step 3: OpenMP

Modify the program image.c again (save in a new file) to make it multi-threaded using pragmas in OpenMP.  You may do this any way you wish, but you must make sure you avoid race conditions, and that your choice of what to parallelize and how to parallelize it makes sense.  Compile your code with -fopenmp and see what the results of your parallelization.  Remember to commit and push your solution back to gitlab.

Step 4: Testing it on an HPC system

Now that you have everything working and checked into github, log into darwin.  Once there, checkout your git repository, and build both versions of your program (openmp and pthreads).  Run an interactive session with 4 cores. type script output.txt, then run both programs and quickly type exit twice (once to end your script file, and the second to close your interactive session.  Add, commit, and push the output.txt file so you can access is through github to hand it in. 

What to hand in:

You will need to hand in the two c programs (pthreads and OpenMP) as well as the script file showing you executing both of them on the Darwin system.  You should also hand in the output.png file from executing the following line (this does not have to be done on Darwin, but can be):

./image pic1.jpg edge

This will allow us to quickly assess if your program works as expected.  Use the pic1.jpg provided in the repository.