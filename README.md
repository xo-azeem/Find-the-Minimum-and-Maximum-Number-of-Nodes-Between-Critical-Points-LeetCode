# Find the Minimum and Maximum Number of Nodes Between Critical Points

LeetCode Q # 2058.

A <b>critical point</b> in a linked list is defined as either a local maxima or a local minima.

A node is a <b>local maxima</b> if the current node has a value strictly greater than the previous node and the next node.

A node is a <b>local minima</b> if the current node has a value strictly smaller than the previous node and the next node.

> Note that a node can only be a local maxima/minima if there exists both a previous node and a next node.

Given a linked list head, return an array of length 2 containing [minDistance, maxDistance] where <b>minDistance</b> is the minimum distance between <b>any two distinct critical points</b> and <b>maxDistance</b> is the maximum distance between <b>any two distinct critical points</b>. If there are fewer than two critical points, return [-1, -1].

Example 1:

<div align = "center">

  ![image](https://github.com/xo-azeem/Find-the-Minimum-and-Maximum-Number-of-Nodes-Between-Critical-Points-LeetCode/assets/171427226/dcba9161-e4e6-490b-b939-106a514f59c3)

</div>

> Input: head = [3,1]</br>
> Output: [-1,-1]</br>
> Explanation: There are no critical points in [3,1].

>Example 2:

<div align = "center">

  ![image](https://github.com/xo-azeem/Find-the-Minimum-and-Maximum-Number-of-Nodes-Between-Critical-Points-LeetCode/assets/171427226/d9802fd1-09f7-4ec6-875e-47870d045292)

</div>

> Input: head = [5,3,1,2,5,1,2]</br>
> Output: [1,3]</br>
> Explanation: There are three critical points:</br>
> - [5,3,<b>1</b>,2,5,1,2]: The third node is a local minima because 1 is less than 3 and 2.</br>
> - [5,3,1,2,<b>5</b>,1,2]: The fifth node is a local maxima because 5 is greater than 2 and 1.</br>
> - [5,3,1,2,5,<b>1</b>,2]: The sixth node is a local minima because 1 is less than 5 and 2.</br>
> The minimum distance is between the fifth and the sixth node. minDistance = 6 - 5 = 1.</br>
> The maximum distance is between the third and the sixth node. maxDistance = 6 - 3 = 3.

Example 3:

<div align = "center">

  ![image](https://github.com/xo-azeem/Find-the-Minimum-and-Maximum-Number-of-Nodes-Between-Critical-Points-LeetCode/assets/171427226/46f4efe0-ef4a-42f8-9d3d-bf043bd9bdd1)

</div>

> Input: head = [1,3,2,2,3,2,2,2,7]</br>
> Output: [3,3]</br>
> Explanation: There are two critical points:</br>
> - [1,<b>3</b>,2,2,3,2,2,2,7]: The second node is a local maxima because 3 is greater than 1 and 2.</br>
> - [1,3,2,2,<b>3</b>,2,2,2,7]: The fifth node is a local maxima because 3 is greater than 2 and 2.</br>
> Both the minimum and maximum distances are between the second and the fifth node.</br>
> Thus, minDistance and maxDistance is 5 - 2 = 3.</br>
> Note that the last node is not considered a local maxima because it does not have a next node.

My Solution Analysis:

<div align = "center">

  ![image](https://github.com/xo-azeem/Find-the-Minimum-and-Maximum-Number-of-Nodes-Between-Critical-Points-LeetCode/assets/171427226/2579eced-5164-44ed-aa46-19141b92d87c)

  Time complexity: O(n).</br>Space complexity: O(1).
</div>
