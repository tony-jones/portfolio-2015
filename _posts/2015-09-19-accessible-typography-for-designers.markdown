---
layout: post
title: Accessible Typography for Designers
subtitle: Typographical considerations that designers should know and implement
author: Anthony Jones
excerpt: When designing user interfaces, you must keep things like proper readability, appropriate spacing, line heights, and users with low vision in mind. Accessible typography is one of the most crucial components of design to understand and implement correctly. A well-chosen font can give your organization credibility, users increased reading pleasure, and trigger different emotions...
thumbnail_url: 'http://appmango.net/anthonyjones/wp-content/uploads/2015/09/font_blocks_800.jpg'
caption: image is courtesy of Unsplash.com
category: Accessibility
permalink: /accessibility/accessible-typography-for-designers
---

<div class="flow-text" itemprop="articleBody">
<p>When designing user interfaces, you must keep things like proper readability, appropriate spacing, line heights, and users with low vision in mind. Accessible typography is one of the most crucial components of design to understand and implement correctly. Designers should be implementing style guides containing typography details, best practices, and standards for components to help bring accessible interfaces to organizations.</p>
<h4 class="light grey-text text-darken-1">Choosing a Typeface</h4>
<p>A well-chosen font can give your organization credibility, users increased reading pleasure, and trigger different emotions.</p>
<p><strong>Aesthetics</strong><br>
Make sure the typeface is well suited for the audience it is intended. Think about what each font says to you and make sure it aligns with the goal, organization, or overall mood of the application.</p>
<p><strong>Experiment</strong><br>
Try out the typeface on your design, so you can see it in the context of the structure of your application. Either use software like Sketch to see the changes or if you are working in the browser, create a SASS variable to easily swap out the fonts globally. I find that this is the best way for me to choose fonts.</p>
<p><strong>Read Them</strong><br>
While you are experimenting with different fonts, it is important to read them. Actually read them by spending time reading large amounts of text. You will be able to quickly eliminate fonts that don’t fit by simply doing this one thing.</p>
<p><strong>Trust Your Gut</strong><br>
Sometimes the choice of fonts doesn’t have to be a mostly technical ordeal. Many times you will just see the perfect font for your design when you see it.</p>
<p>Lastly, I suggest using sites like <a class="anchor" href="https://typ.io/">Typ.io</a> to help you find nice font combinations that others are using.</p>
<h4 class="light grey-text text-darken-1">Color &amp; Contrast</h4>
<p>Some users with low vision will adjust the contrast levels of their screens. To accommodate for this, designers should ensure that their applications meet WCAG 2.0 level AA requirements at a minimum. This requires a contrast ratio of 4.5:1 for normal text and 3:1 for large text (14 point and bold or larger, or 18 point or larger).</p>
<p>This can easily be verified by using a WebAIM’s<a class="anchor" href="http://webaim.org/resources/contrastchecker/"> Contrast Checker</a>. I also recommend that designers begin the design process by using <a class="anchor" href="http://colorsafe.co/">accessible color palettes</a>.</p>
<p>Most typefaces were designed to be printed with black ink on a light background, so you need to be careful when choosing a typeface reversed out of a dark background. Keep in mind font weight, style, and overall readability when your background is dark.</p>
<h4 class="light grey-text text-darken-1">Line Length</h4>
<p><strong>Body Text</strong><br>
The optimal line length for your body text is considered to be 50-60 characters (via <a class="anchor" href="http://baymard.com/blog/line-length-readability">Baymard</a>). I use the <a class="anchor" href="https://chrome.google.com/webstore/detail/word-character-count-tool/ibjgdahgcdkpdlbkadidojhfddflblcm?hl=en">Word &amp; Character Count</a> chrome extension to see how long lines are. Personally, I prefer the characters per line to be between 60 and 80 characters when I am reading.</p>
<p><strong>Short Lines</strong><br>
For short lines, the optimal line length is considered to be about 15-30 characters</p>
<h4 class="light grey-text text-darken-1">Text Styles</h4>
<p>Designers should limit the number of text sizes and styles to keep a clean and readable feel to their applications. Frameworks like <a class="anchor" href="http://getbootstrap.com/">Bootstrap</a>, <a class="anchor" href="http://materializecss.com/">Materialize</a>, and <a class="anchor" href="http://www.getmdl.io/">Material Design Lite</a> will have base typographic scales already built in for developers. Google recommends having a basic set of styles that are based on a typographic scale of 12, 14, 16, 20, and 34.</p>
<p>For further reading, I would recommend going through Google’s <a class="anchor" href="https://www.google.com/design/spec/style/typography.html#">Design Spec</a> and IBM’s <a class="anchor" href="https://www.ibm.com/design/language/framework/visual/typography.shtml">Design Language</a>.</p>
</div>
