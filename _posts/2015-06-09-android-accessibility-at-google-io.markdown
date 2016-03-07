---
layout: post
title: Android Accessibility at Google IO
subtitle: A summary of Android accessibility services covered during talks at Google IO 2015
author: Anthony Jones
excerpt: Phil Weaver, Eve Andersson, Casey Burkhardt, Hugh Oh, and Mark Riccobono presented at Google IO on Android accessibility and how we can remove and replace assumptions about users and how they interact with Android apps. I will briefly cover three means of achieving this and the assumptions that come along with each technology. TalkBack...
thumbnail_url: http://appmango.net/anthonyjones/wp-content/uploads/2015/06/accessibility-blue-braille-google.jpg
caption: An illustration of Google written in braille made with iDraw.
category: Accessibility
permalink: /accessibility/android-accessibility-at-google-io
---

<div class="flow-text" itemprop="articleBody">
<p>Phil Weaver, Eve Andersson, Casey Burkhardt, Hugh Oh, and Mark Riccobono presented at Google IO on Android accessibility and how we can remove and replace assumptions about users and how they interact with Android apps.</p>
<p>I will briefly cover three means of achieving this and the assumptions that come along with each technology.</p>
<p><strong>TalkBack: </strong>this is a screen reader that adds spoken, audible, and vibration feedback to your device. It helps blind and vision-impaired users interact with their devices. It makes the assumption that users can hear but not see.<br>
<i class="mdi-av-mic" style="font-size: 16px;"></i><i><a class="anchor" href="https://support.google.com/accessibility/android/answer/6007100?hl=en">Enable TalkBack</a></i></p>
<p><strong>BrailleBack: </strong>BrailleBack allows users to connect a refreshable braille device via Bluetooth. Users can navigate using their display and input text using the braille keyboard. This tool assumes that users can’t hear or see.<br>
<i class="mdi-navigation-more-vert" style="font-size: 16px;"></i><i><a class="anchor" href="https://support.google.com/accessibility/android/answer/3535226?hl=en">Enable BrailleBack</a></i></p>
<p><strong>Switch Access: </strong>this enables users to interact with a device using one or more buttons/switches that work like keyboard keys. This removes that assumption that a user can touch and interact with a screen with their hands.<br>
<i class="mdi-image-adjust" style="font-size: 16px;"></i><i><a class="anchor" href="https://support.google.com/accessibility/android/answer/6122836?hl=en">Enable Switch Access</a></i></p>
<p>Developers have the important task of making sure application code can properly interact with these devices. Phil Weaver noted that the World Health Organization estimates 15% of people have some disability (1 billion people).</p>
<p>Catching accessibility bugs as early as possible using automated testing(Android Lint, etc.) and manually testing are essential to making sure our Android applications can be using by everyone.</p>
<p>The basic solutions making your apps accessible on Android are the following:</p>
<p><strong>1. Adding descriptions to all image that convey meaning</strong></p>
{% highlight java linenos %}
contentDescription="@string/desc"
{% endhighlight %}

<p><strong>2. Give users immediate feedback on view updates.</strong></p>
{% highlight java linenos %}
android:accessibilityLiveRegion="polite"
{% endhighlight %}
<p><strong>2. Remove redundant text</strong></p>
{% highlight java linenos %}
android:contentDescription="7 Button" // incorrect as screen reader reads "7 Button Button"
android:contentDescription="7" // correct as screen reader reads "7 Button"
{% endhighlight %}

<p><strong>4. Remove extraneous clickable views on the screen</strong></p>
{% highlight java linenos %}
android:clickable="true" // Region 1
android:clickable="true" // Region 2
android:clickable="true" // Region 3
{% endhighlight %}
<p>When using a tool such as Switch Access, users will have to scan through all regions that are clickable, so having extraneous clickable regions hinders the overall user experience.</p>
<p><strong>In comes Accessibility Checker For Android!</strong><br>
Accessibility Checker is a new Google Research project and it looks specifically for accessibility defects. It will help us automatically find issues like: missing speakable descriptions and incorrectly labeled views. This is available today in both the Espresso(2.2+) and Robolectric testing frameworks.</p>
<p><i><a class="anchor" href="https://code.google.com/p/android-test-kit/wiki/EspressoSetupInstructions">Setting up Espresso</a></i></p>
{% highlight java linenos %}
/**
 * Enable Accessibility Checker in Espresso 2.2+
 */
@Test
public void setUp() {
  AccessibilityChecks.enable(); // one extra line of code to enable accessibility checks
}
{% endhighlight %}
<p><i><a class="anchor" href="http://robolectric.org/">Getting Started with Robolectric</a></i></p>
{% highlight java linenos %}
/**
 * Enable Accessibility Checker in Robolectric
 */
@Test
@AccessibilityChecks // One line Java annotation to enable accessibility checks
public void testOneButton_shouldAddOne() {
  ...
}
{% endhighlight %}


<p><strong>Resources</strong><br>
For further reading and a more in-depth look at accessible application development in Android please visit <i><a class="anchor" href="http://developer.android.com/training/accessibility/accessible-app.html">Developing Accessible Applications</a></i></p>
<h4 class="light grey-text text-darken-1">Freebie</h4>
<p>Save 30 minutes making a braille illustration with this Sketch file</p>
<p><a href="http://appmango.net/anthonyjones/?download=1334"><img src="http://appmango.net/anthonyjones/wp-content/uploads/2015/07/Braille.jpg" sizes="(max-width: 1500px) 100vw, 1500px" srcset="http://appmango.net/anthonyjones/wp-content/uploads/2015/07/Braille-300x200.jpg 300w, http://appmango.net/anthonyjones/wp-content/uploads/2015/07/Braille-1024x683.jpg 1024w, http://appmango.net/anthonyjones/wp-content/uploads/2015/07/Braille.jpg 1500w" alt="Braille Illustration " width="1500" height="1000" class="radius-three responsive-img aligncenter size-full wp-image-1335"></a><br>
<br>
<a href="http://appmango.net/anthonyjones/?download=1334" title="Download" class="btn blue lighten-1">Download</a></p>
</div>
