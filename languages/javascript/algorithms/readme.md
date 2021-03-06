## Algorithms

What makes an algorithm fast? To answer this question, it tend to be grouped in two categories. With respect to input size and also assuming the worst case scenario.
- Time complexity
- Space Comlexity

## Time complexity

Here we answer the question of how many primitive **operations** are executed?

Time complexity of an algorithm signifies the total time required by the program to run to completion. The time complexity of algorithms is more commonly expressed using the big O notation.

**Big-O notation gives us an Industry-standard language** to discuss the performance of algorithms. 


Not knowing how to speak this language **can make you stand out as an inexperienced programmer.**

##### Space Complexity

Here we are answering the question of How much **memory** is Used?

### Problem to think On

Given a list of hotels return the price range of hotels in a given search result. Lets write the algorithm..

```Javascript
var hotels = [
    {price : 200, brand : "best eastern"}
    {price : 200, brand : "best eastern"}
    {price : 300, brand : "best eastern"}
    ....
]
```

### solution

We'd expect that the more data we have, the longer it will take to figure out the min and max required for the range.
However, as our dataset grows, the cost can grow really fast or slow!

##### Approch 1 : Compare all numbes to one another.

As our data grows, how much does our work increases?

| # of hotels (n) | 3   | 5   | 10  | 100  |
| --------------- | --- | --- | --- | ---- |
| #ops            | 9   | 25  | 100 | 1000 |

We can call this n^2 ,where n is the number of hotels. As n grows, the amount of work increases at that rate.

## Approach two: Trach min & max

How many comparison were made? We have to for loops each tracking the minimum and the max values.

we consider this 2\*n because as the data grows, the number of work increase by 2.
Its faster, less comparison are made for this.

## Approach 3: Sorted List

Here you know where the min and max. We get the first and the last numbers.

| # Operations Big-O | Algorithm                       |
| ------------------ | ------------------------------- |
| n^2 (quadratic)    | compares all the numbers        |
| 2n (Linear)        | Find min and and max values     |
| 2 ,constant        | Sorted list find first and last |

As the input grows.

[super fast](#)--------------------------------------------------------------------------------->[super slow](#)
|Name |constant | logarithmic |linear | quadratic | exponential|
|-------|---------|-------------|-------|-----------|------------|
|Notation|O(1) | O(logn) | O(n) | O(n^2) | O(e^n) |

check out the big o [chart](https://www.bigocheatsheet.com/)

## Native Methods & JS Expressions

### Time complexities

1. Arrays : Contant.

pop is **contant** times.

```Javascript
const arr = [1,2,3]
arr.pop() //=> {1,2}
arr[1] // dont need to start from index one, it know where the value is
```

2. Object : Contant time algorithm

```Javascript
const obj = {a: 1};
obj.a // -> 1
```

3. For loop: Linear.
4. Shift and Unshift are not contants since the but they are linear.
5. Sort.

## Calculating Time

What to we do if we have multiple expressions/loops/etc?

> #### what about o(logn)?
>
> A little better that linear.

## Complexity of Common Operations

| complexity | operation                                        |
| ---------- | ------------------------------------------------ |
| O(1)       | Running a statement                              |
| O(1)       | value look-up on array, object,variable          |
| O(logn)    | loop that cuts a problem in half every iteration |
| O(n)       | Looping through the value of an array            |
| O(n^2)     | Double nested loops                              |
| O(n^3)     | Tripple nested loops                             |

### Space Complecity

The space that it take up in the memory. Are you making a new
data structure how often are you doing that?.

#### Faster Algorithms

Optimizing by using  **hash table** is caching. A hash table i generaly an object.

#### Recursion / Fancy Loop

A function that calls itself

##### Call STack Game

1. push called fn on **stack**.
2. execute Fn body.
 until...
   - another fn is called.
       Pause the current execution and start at step 1.
   - A return is hit.
       Pop the current fn of the stack.
       Resume execuving the previous Fn.

Recurcion is **cool way** of looping.

- Identify base case(s)
- Identify recursive case(s)
- Return where appropriate
- Write Procedures for each case bring you closer to base case(s)

#### Looping

Recursion can always be implemented as a loop, in some situations, believe it or not, it is simpler to use recursion.

#### Divide and Conquer

Recursive calls to a subset of the Problem.

0. Recognize base case.
1. Divide: Break problem down during each call.
2. Conquer: Do work on each subset.
   - search for a match.
3. Combine: solution.

#### Searching Algoritms.

##### binary Search

Search for a value in a **sorted** array by cutting the side of the search area in half.
Binary search is data must be sorted.

##### Linear Search.

For unsorted. You are going to loop throug a list to find the number.

#### Sorting Algorithms

There are alot of study on how to sort.
There are two main types of sorting algoritms. All this sort are **comparison Sorts**.

##### Nalve Sort

###### Bubble Sort

Loops through an array, comparing adjacent indices and swapping the greater value to the end.

###### Insertion sort

Take another empty, Take the smallest value it the original array push it to the new array. You do that until you have a new sorted array.

###### Selection Sort


##### Divide and Conquer

Recursively divide list and sort smaller parts of list until entire list its sorted.

##### Mergesort
We take a unsorted list

/// Pseudocode.

// Merge Routine
// Merge(L,R)
[3,9,10]
//[24]    //[]
// initialize empty array.
// compare the firt index ot left array.
// to the first index of the right array.
// push the lower value to empty array
// shift the array with the lower value.
// repeate untill both arrays are empty.

mergesort(list)
 base case: if list.length \< 2, return
 break the list inot halves L and R
 Lsorted = mergesort(L)
 Rsorted = mergeSort(R)
 return merge(Lsorted, Rsorted)

[7,6,1,12]

Our **merges sort algorithm** is nlogin

#### Inteviwe Strategy

##### Quicksort

#### Dynamic Algorithms 

#### interview

Due to the time contrain of the inteview is it okay for me to implemente a naive sorted. But i could optimize it using a Divide and conqure algorithm.

 if you are asked to do a searching algorithmes. the Best is to get it sorted. and then implement a binary search.



#### Greedy Algorithms.

Greedy algoritm algorithms always make the locally optimal choice!. Without considering the big picture.

You are the banker in Monopoly with your family who has lost  many of the game piece so you only have bills in the denominations.

       $5 $10 $25

You need only pay out you family in the least number of bills possible so you don't run out befor the game is over. Write a function that calculate the least number of bills required for any given dollar amount that is divisible by 5.


#### Brute Forcee

Brute force Approach Calculates every single combination possible and keeps track of the minimum.
