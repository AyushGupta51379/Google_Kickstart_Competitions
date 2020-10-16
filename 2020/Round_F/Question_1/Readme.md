### Notebook folder has my colab notebook

## Correct solution - with O(n) space and O(n) time complexities, 

O(n) space and O(n) time complexities, for each test case, where n is the number of people in each test case.

Overall, O(biggest_n) space and O(biggest_n) time complexities, for all test cases combined, where biggest_n is the largest value of number of people, out of all the test cases.

### Text_3.txt has 3rd solution in text format - works perfectly well
#### Good solution, utilizes sorting of people according to:
##### Number of attempts they need, and
##### Their initial order in queue
#### Time and Space complexity: O(nlogn) time and O(n) space, for each test case, where n is the number of people
##### Reason of O(nlogn) time - Sorting n elements takes O(nlogn) time, looping over n elements takes O(n) time, Overall, O(nlogn) time complexity, for each test case, where n is the number of people
##### Reason of O(n) space - B is 2D array of 2*n occupying O(n) space, A and P are 1D arrays of 1*n occupying O(n) space,, for each test case, where n is the number of people

## Other Solutions - Correct on 1st case, Memory/Time Error on 2nd case:

### Text_2.txt has 2nd solution in text format - gives TLE on 2nd case
#### Time limit error - TLE
#### Similar strategy as in Text_1.txt, however occupies lesser memory
#### Since we perform append to end of queue, and then remove the initial,
#### Overall, occupying O(n) space, for each test case, where n is the number of people
#### Reason of error - we take O(total number of attempts) time, for each test case, where n is the number of people

### Text_1.txt has 1st solution in text format - gives MLE on 2nd case
#### Memory limit error - MLE
#### Uses Brute Force approach, to simulate how the process happens
#### Reason of error - we take O(total number of attempts) space, for each test case
#### Reason of error - we take O(total number of attempts) time, for each test case
