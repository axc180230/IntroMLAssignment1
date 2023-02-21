# IntroMLAssignment1
Introduction To Machine Learning - Assignment 1

## Software Needed
Fundamentally, you need to have python installed to run these files. you will need to use at least version 3.x. It can be downloaded from https://www.python.org/.

The following libraries need to be installed to be able to run assignment 1 files.
- numpy
- pandas
- matplotlib
- sklearn

You can install these libraries from the Command Line Interface (CLI) via the "pip install <library> command. You can find more information about this at https://packaging.python.org/en/latest/tutorials/installing-packages/.

  
## Run Programs
  To run the assignment files you will first need to navigate to the directory you have the python files saved via the CLI. Once there you simply need to enter the following commands into the CLI for the respective project part. 

### Part 1
  **Command**: `python3 part1.py`
  <br>**Note**: 
  <br>This uses custom built regression model and takes approximately 20 minutes to run with current coded iterations and learning rates. 
  <br>In addition, it provides a runtime warning in CLI about "invalid value encountered in double_scalars". This is because the largest learning rate (.3) causes an overflow of the numpy datatype. I left these values in to show that they do not converge and can be used as an upper bound. 
  
### Part 2
  **Command**: `python3 part2.py`
  <br>**Note**:
  <br>This provides a runtime convergence warning "Maximum number of iteration reached before convergence". Consider increasing max_iter to improve the fit.". However I only increased it to 10,000 at the most in order to still be directly comparable to part 1 iterations. 
  <br>This file runs much faster than part1.

## Output
  Both parts output similar files saved the same directory the files are being run from. There is no output to CLI (except previously noted warnings).
  1. assignment1_part<x>_trainingmetadata.csv
    <br>- Statistics (variables, coefficients, and rss/mse) captured from training model.
  2. assignment1_part<x>_testingmetadata.csv
    <br>- The variables and coefficents used to test model, as well as testing mean square error. 
  3. Part<x>_AverageWeightofFeatures.png
    <br>- Graph that shows with Features had the most impact on determining label (MPG).
  4. Part<x>_Testing_MSE_As_Function_of_Iterations.png
    <br>- Grapht that shows testing mean square error as a function of iterations.
  5. Part<x>_Testing_MSE_As_Function_of_LearningRate.png
    <br>- Grapht that shows testing mean square error as a function of learning rate.

## Project Questions
### Part 1: Are you satisfied that you have found the best solution? Explain.
I'm relatively certain I've found the best solutionI can reach with linear regression. Any learning rate above my upper bound doesn't converge and anything lower than my lower bound (for my optimum) doesn't decrease the mean square error on either the training or testing data. 
  
### Part 2: Are you satisfied that the package has found the best solution. How can you check. Explain
I am relatively certain that it has found a good solution, if not the best. The MSE I could acheive for testing data in part 1 was lower. However, when I increase the iterations to higher numbers (around 100,000), it starts to approach my coefficients. I can check by looping through more variables to determine if I can find an even better model but it would then not be comparable to part 1 since part 1 takes a lot longer to run depending on iterations. 
  
## References
1. https://www.youtube.com/watch?v=ZUoqJqYJnsw
2. https://scikit-learn.org/stable/
3. https://pandas.pydata.org/
4. https://www.w3schools.com/python/matplotlib_pyplot.asp
5. https://learnxinyminutes.com/docs/python/
