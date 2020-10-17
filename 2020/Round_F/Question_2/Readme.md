# Concept

### Best concept
#### Sort the intervals according to their starting time

B = sorted(A, key = lambda l:l[0])

Where A is the array with intervals

#### Logical flow of deploying robots, calculate end time of previous robot, estimate number of robots needed for the current interval, repeat..

Initially, we deploy the robot j=1 at the s1 of B (si where i=1 of 1st interval). We can denote S1 = s1, where Sj is the starting time of the robot j. Now, we calculate the E1 = max end time of robot 1 = s1+K.

If E1 = s1+K < e1, then we need to deploy another robot (j=2) at s1+K. This will stay deployed until s1+2K. We repeat this process until, we have deployed m1 robots, where m1 = math.ceil((e1-s1)/K). This, will stay deployed until Em1 = s1+m1K.

If Em1 >= e1, then we finished this interval. Now, we check if this robot covers the next interval.

Overall, for interval 1, we deploy one robot at s1, and in total we deploy m1 = math.ceil((e1-s1)/K) robots for this interval 1.

Subcase1: Em1 > s2 - meaning this robot can start the next interval. Great. We deploy m2 new robots, where, m2 = math.ceil((e2-Em1)/K). Then, this will stay deployed until E(m1+m2) = Em1+K*m2.

Subcase 2: Em1 < s2 - meaning this robot can't start the next interval. Well, then we deploy another robot (m1+1) at s2. In total, we will deploy m2 = math.ceil((e2-s2)/K) robots for interval 2.

This process will repeat until we are finished with all the intervals, that is i has covered N intervals = len(A).

#### This gives us our best solution, code in Text_1.txt and also in Final Code 1 from notebook.

# Code

### Notebook folder has my colab notebook

## Correct Solution - Efficient code - with O(n) space and O(nlogn) time complexities, 

O(n) space and O(nlogn) time complexities, for each test case, where n is the number of people in each test case.

Overall, O(biggest_n) space and O(biggest_n) time complexities, for all test cases combined, where biggest_n is the largest value of number of people, out of all the test cases.

### Text_1.txt has 1st solution (= correct solution) in text format - works perfectly well
#### Time and Space complexity: O(nlogn) time and O(n) space, for each test case, where n is the number of people
##### Reason of O(nlogn) time - Sorting n elements takes O(nlogn) time, looping over n elements takes O(n) time, Overall, O(nlogn) time complexity, for each test case, where n is the number of people
##### Reason of O(n) space - B is 2D array of 2*n occupying O(n) space, A is a 1D arrays of 1*n occupying O(n) space, for each test case, where n is the number of people. Other variables occupy constant space = O(1) space.

## Other Correct Solutions

### Text_0.txt has my solution during the competition, in text format, works perfectly well
#### Time and Space complexity: O(nlogn) time and O(n) space, for each test case, where n is the number of people
##### Reason of O(nlogn) time - Sorting n elements takes O(nlogn) time, looping over n elements takes O(n) time, Overall, O(nlogn) time complexity, for each test case, where n is the number of people
##### Reason of O(n) space - B is 2D array of 2*n occupying O(n) space, A is a 1D arrays of 1*n occupying O(n) space, for each test case, where n is the number of people. Other variables occupy constant space = O(1) space.
