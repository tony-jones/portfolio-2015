---
layout: post
title: Selection Sort, Sorting Algorithms in Java
subtitle: Sorting is a fundamental of computer science theory, but it is also easy to forget.
author: Anthony Jones
excerpt: The next sorting algorithm in this series is the selection sort. Selection sort is also one of the easiest algorithms to understand and translate into functioning code. A basic example of a selection sort would be to line up ten people all having varying heights in a row. Find the shortest person...
thumbnail_url: http://appmango.net/anthonyjones/wp-content/uploads/2015/05/computer-microchip-motherboard.jpg
caption: Lazy morning programming in bed | Photo by Viktor Hanacek
category: Code
permalink: /code/selection-sort-sorting-algorithms-in-java/
---

<div class="flow-text" itemprop="articleBody">
<div id="bubblesort" class="section scrollspy">
<h4 class="light grey-text text-darken-1">Selection&nbsp;Sort: Comparing Each Adjacent Item</h4>
<p>The next sorting algorithm in this series is the selection sort. Selection sort is also one of the easiest&nbsp;algorithms to understand and translate into functioning code.</p>
<p>A basic example of a selection sort would be to line up ten people(all having varying heights) in a row. Find the shortest person in the line and switch them with the person in position one. Then, find the next shortest person and swap them with the person in position two. Repeat until all ten people are sorted from shortest to tallest.</p>
<p>If we have a list with six items, we will need to make a comparison on the first element five times, the second element four times, the third element three times, etc.(5+4+3+…) From this, we can generalize that that worst-case runtime is 0(n²). Also, we will be using two for loops which also hints to a n² runtime.</p>
<p>Here is a basic example of a selection sort in Java.</p>
</div>
{% highlight java linenos %}
/**
 * @author Anthony Jones
 * @version 1.01
 *
 * This is the selection sort method. specifically
 * an in place comparison sort
 *
 * @param A
 * int array
 */
public static void selectionSort(int[] A) {
  int temp;
  for (int i = 0; i < A.length; i++) {
    int n = i;
    for (int j = i + 1; j < A.length; j++) {
      if (A[j] < A[n])
        n = j;
    }
    temp = A[i];
    A[i] = A[n];
    A[n] = temp;
  }
}
{% endhighlight %}
<p>Lastly, don’t forget to test your code. Here is a JUnit test case I wrote to test if my result arrays were sorted.</p>

{% highlight java linenos %}
/**
* The test for selection sort method three for large array
*
* @author Anthony Jones
* @version 1.01
*/
@Test
public void selectionSortTestThree_Large() {
  System.out.println();
  System.out.println("Selection Sort Test Three");
  int[] arr = { 1, 4, 2, 9, 7, 3, 10, 20, 11, 13, 19 };
  System.out.println("intital array to be sorted");
  for (int i = 0; i < arr.length; i++) {
    System.out.print(arr[i]);
  }
  System.out.println();
  int[] expected = { 1, 2, 3, 4, 7, 9, 10, 11, 13, 19, 20 };
  System.out.println("expected array to be compared to");
  for (int i = 0; i < expected.length; i++) {
    System.out.print(expected[i]);
  }
  System.out.println();
  System.out.println("intital array after the sort");
  sortingAlgorithms.selectionSort(arr);
  for (int i = 0; i < arr.length; i++) {
    System.out.print(arr[i]);
    assertEquals(arr[i], expected[i]);
  }
}
{% endhighlight %}
</div>
