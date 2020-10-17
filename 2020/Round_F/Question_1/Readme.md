# Concept

### Best concept
#### Calculate the minimum number of attemps needed by each person 
Using Money divided by Max_Amount, that is, A[i]/X.

Now, take the math.ceil of that, to get minimum number of attempts = math.ceil(A[i]/X).

Let's call this 2D array B, where B[i] = [i, math.ceil(A[i]/X)], storing the index and attempts needed for each person in A.

#### Sort the above obtained Array B, to get the order of leaving.

We need to sort using indices, then over that we sort using attempts needed. This is done because for people needing same number of attempts, we need to order them using their original order, that is indices in A. We already stored indices from A in the 1st element of every B[i] and attempts in 2nd element of every B[i].

sorted_B = sorted(sorted(B, key = lambda l:l[1]), key = lambda l:l[0])

#### This gives us our best solution, code in Text_3.txt and also in Code 3 from notebook.

# Code

### Notebook folder has my colab notebook

## Correct solution - Efficient code - with O(n) space and O(nlogn) time complexities, 

O(n) space and O(nlogn) time complexities, for each test case, where n is the number of people in each test case.

Overall, O(biggest_n) space and O((biggest_n) log(biggest_n)) time complexities, for all test cases combined, where biggest_n is the largest value of number of people, out of all the test cases.

### Text_3.txt has 3rd solution (= correct solution) in text format - works perfectly well
#### Good solution, utilizes sorting of people according to:
##### Number of attempts they need, and
##### Their initial order in queue
#### Time and Space complexity: O(nlogn) time and O(n) space, for each test case, where n is the number of people
##### Reason of O(nlogn) time - Sorting n elements takes O(nlogn) time, looping over n elements takes O(n) time, Overall, O(nlogn) time complexity, for each test case, where n is the number of people
##### Reason of O(n) space - B is 2D array of 2*n occupying O(n) space, A and P are 1D arrays of 1*n occupying O(n) space,, for each test case, where n is the number of people

## Other Solutions - Brute forced approaches - Correct on 1st case, Memory/Time Error on 2nd case:

### Text_2.txt has 2nd solution in text format - gives TLE on 2nd case
#### Time limit error - TLE
 Similar strategy as in Text_1.txt, however occupies lesser memory
 
 Since we perform append to end of queue, and then remove the initial,
 
 Overall, occupying O(n) space, for each test case, where n is the number of people
#### Reason of error - we take O(total number of attempts) time, for each test case, where n is the number of people

### Text_1.txt has 1st solution in text format - gives MLE on 2nd case
#### Memory limit error - MLE

Uses Brute Force approach, to simulate how the process happens

#### Reason of error - we take O(total number of attempts) space, for each test case

#### Reason of error - we take O(total number of attempts) time, for each test case
