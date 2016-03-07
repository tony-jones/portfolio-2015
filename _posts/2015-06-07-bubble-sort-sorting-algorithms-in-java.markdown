---
layout: post
title: Bubble Sort, Sorting Algorithms in Java
subtitle: Sorting is a fundamental of computer science theory, but it is also easy to forget.
author: Anthony Jones
excerpt: The first sorting algorithm that we will discuss in this series is the bubble sort. Bubble sort is one of the simplest algorithms to understand and translate into functioning code. A basic analogy of a bubble sort would be to line up ten people all have varying heights in a...
thumbnail_url: http://appmango.net/anthonyjones/wp-content/uploads/2015/05/sublime-text-code-macbook.jpg
caption: Lazy morning programming in bed | Photo by Viktor Hanacek
category: Code
permalink: /code/bubble-sort-sorting-algorithms-in-java/
---

<div class="flow-text" itemprop="articleBody">
<div id="bubblesort" class="section scrollspy">
<h4 class="light grey-text text-darken-1">Bubble Sort: Comparing Each Adjacent Item</h4>
<p>The first sorting algorithm that we will discuss in this series is the bubble sort. Bubble sort is one of the simplest algorithms to understand and translate into functioning code.</p>
<p>A basic analogy of a bubble sort would be to line up ten people(all have varying heights) in a row. Moving from left to right, if the current person’s height is greater than the next person’s height, swap them around. Repeat until all ten people are sorted from shortest to tallest.</p>
<p>In the code, we would simply write a method for swapping two elements of an array and then with for loops, traverse the array until all items are sorted.</p>
<p>The array will need to be traversed at least n-1(n is the number of objects in the array) times to ensure that all objects are sorted. While the bubble sort is useful as a learning tool, it is not one of the most efficient sorting algorithms. It’s worst case runtime is 0(n²), because we need to make n iterations through a list checking all n elements each pass through.</p>
<p>Below is a basic example of a bubble sort in Java.</p>
</div>
{% highlight java linenos %}
/**
 * @author Anthony Jones
 * @version 1.01
 *
 * This method repeatedly steps through the list
 * and compares each adjacent item and sorts.
 * @param A
 * int array
 */
public static void bubbleSort(int[] A) {
  boolean isSwapped;
  int temp;
  for (int i = 0; i < A.length; i++) {
    isSwapped = false;
    for (int j = A.length - 1; j >= i + 1; j--) {
      if (A[j] < A[j - 1]) {
        // Lines 19-22 can be replaced with a swap method
        temp = A[j];
        A[j] = A[j - 1];
        A[j - 1] = temp;
        isSwapped = true;
      }
    }
    if (isSwapped != true)
      break;
  }
  return;
}
{% endhighlight %}
<p>This code can be further optimized. Please give it a try yourself and post a link to your solution in the comments. Here are some hints on how to improve the performance of your code.</p>
<p><strong>Method 1:</strong><br>
After one iteration through the array, we don’t need to check the rightmost element because we already know that it is sorted. After two iterations, the last two elements in the array will be sorted. If we follow this pattern, we can generalize that after k iterations through the full array, checking the last k elements is redundant.</p>
<p><strong>Method 2:</strong><br>
Check if the list is sorted after each iteration.</p>
<p>Lastly, don’t forget to test your code. Here is a JUnit test case I wrote to test if my result arrays were sorted.</p>
{% highlight java linenos %}
/**
 * The test class bubbleSort method three.
 *
 * @author Anthony Jones
 * @version 1.01
 */
@Test
public void bubbleSortTestThree_Large() {
  System.out.println();
  System.out.println("Bubble Sort Test Three");
  int[] arr = { 1, 5, 9, 2, 4, 3, 10, 20, 13, 15, 11 };
  System.out.println("intital array to be sorted");
  for (int i = 0; i < arr.length; i++) {
    System.out.print(arr[i]);
  }
  System.out.println();
  int[] expected = { 1, 2, 3, 4, 5, 9, 10, 11, 13, 15, 20 };
  System.out.println("expected array to be compared to");
  for (int i = 0; i < expected.length; i++) {
    System.out.print(expected[i]);
  }
  System.out.println();
  System.out.println("intital array after the sort");
  sortingAlgorithms.bubbleSort(arr);
  for (int i = 0; i < arr.length; i++) {
    System.out.print(arr[i]);
    assertEquals(arr[i], expected[i]);
  }
}
{% endhighlight %}
</div>
