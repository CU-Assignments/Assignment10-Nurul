# Assignment10-Nurul
# ----------------- Question 1------------------
You are tasked with writing a program to calculate the total shipping cost based on the weight of the package and the distance it needs to travel. </br> 
The following criteria determine the shipping cost: </br> 
1. Base money: $5.00 (must be included in the shipping cost) </br> 
2. Cost per kilogram: $2.00 </br> 
3. Cost per 10 kilometers: $0.5 </br>
Input Format </br> 
•	The first line contains an integer w, representing the weight of the package.</br>
•	The second line contains an integer d, representing the distance it needs to travel.</br>
Output Format</br>
Print the total shipping cost of the package.</br>
Constraints</br>
•	1 ≤ w ≤ 10⁷</br>
•	1 ≤ d ≤ 10⁷</br>
Example</br>
Sample Input:</br>
20</br>
200</br>
Sample Output:</br>
55</br>
Explanation:</br>
The base cost is 5, which must be included.</br>
Given a weight of 20 kg and a rate of 2 per kilogram, the weight cost is calculated as 20×2=40.</br>
For a distance of 200 km, with a rate of 0.5 per 10 km, the distance cost is 200×0.5/10=10.</br>
Therefore, the total cost is 5+40+10=55.</br>
# ----------------Question2-------------------------
You are given an array 'A' of size 'N'. </br>
You can apply the following operation any number of times (possibly zero) on 'A'.</br>
1. Choose any prefix of 'A' such that the last element of </br>
the prefox is equal to the minimum element of the chosen prefix </br>
and replace all its elements with its last element. </br>
For example: A' = [3, 4, 1, 3, 0, 7] </br>
if we choose the prefix 'A[02] le ending at index 2, </br>
then the final array will be ` A' = [1, 1, 1, 3, 0, 7 ]</br>
2. Choose any contiguous segment of 'A' and cyclically shift this </br>
segment to the left, keeping the remaining elements unchanged. </br> 
For example: A^ prime =[ 3, 4, 1, 3, 0 ,7] </br>
if we choose the segment 'A[1.3]' ie starting at index 1 </br>
and ending at index 3, then the final array will be A' = [3, 1, 3, 4, 0, 7] </br>
Note: Assume 0-based indexing. </br>
Return the minimum number of operations required to make all </br>
the elements of the array equal. </br>
For example: </br>
Let " N "=5 A' = [3, 4, 2, 0, 1] We will need 2 operations. </br>
We will apply operation 2 and choose the segment A * [3 - 4]' </br>
Resultant array will be A=[3,4,2,1,0] </br>
We will apply operation 1 on the entire array ie 'A[0...4]'. </br>
Resultant array will be </br>
'A' = [0, 0, 0, 0, 0]. </br>
Therefore the answer will be 2. </br>
Input formate: /br>
1. first line number of test case </br>
2. second line n which is size of array for each test case </br>
3. third line n space seperated integer element of array </br>
Output format: </br>
Answer minimum number of operation </br>
Sample Input 1: </br>
2 </br>
4 </br>
0 1 0 1 </br>
2 </br>
1 1 </br>
Sample Output 1: </br>
2 </br>
0 </br>
Explanation of Sample Input 1: </br>
First test case:- </br>
We will need 2 operations. </br>
We will apply operation 2 and choose the segment 'A[2-3]'.</br>
Resultant array will be 'A' = [0, 1, 1, 0]. </br>
We will apply operation 1 on the entire array i.e 'A[03]'. </br>
Resultant array will be 'A' = [0, 0, 0, 0]. </br>
Therefore the answer will be 2, and it can be verified that this </br>
is the minimum possible operations required. </br>
Second test case:- </br>
We will need 0 operations as all the elements of the array are already equal. </br>
Some other test case for Question 2 </br>
Input: </br>
10 </br>
29 </br>
4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 </br>
48 </br>
56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 56 </br>
30 </br>
61 60 27 50 41 97 41 88 43 93 43 46 98 75 96 27 57 68 99 30 37 35 44 61 92 39 58 36 73 27
50 </br>
7976 4764 4836 5071 9905 7841 9677 1960 5546 5010 774 5255 3245 1203 9687 8527 649 3055 8808 6186 1360 7088 6756 9127 2068 3646 8568 9858 2337 6945 4617 5357 9914 3307 6762 5283 2109 6684 9119 7047 3206 2273 2256 3948 5008 4087 580 3015 3770 2052 </br>
31 </br>
7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 </br>
47 </br>
1604 4748 3554 204 8611 4297 5975 4844 7358 9557 6164 3957 9659 8765 4852 6851 4141 1202 4405 9737 9651 4671 2727 9748 6441 3780 346 1380 4217 8983 3676 4569 4200 8394 3983 7540 7276 1749 5543 2981 8374 1572 5300 8564 3835 979 5360 </br>
28 </br>
26 37 70 52 31 60 31 53 51 97 30 57 37 46 45 50 53 86 78 24 86 49 65 35 88 77 30 24 </br>
26 </br>
100 96 99 99 98 97 99 98 99 99 98 98 96 100 99 100 97 99 96 98 98 100 96 96 96 96 </br>
19 </br>
92 98 80 93 81 99 86 99 98 91 87 81 91 89 87 84 96 83 80 </br>
33 </br>
4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 </br>
Output: </br>
0 0 1 2 0 2 1 1 1 0





