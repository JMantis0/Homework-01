# Horiseon Solutions Code Refactor

The goal of this project is to make the code of Horiseon Solution's website more accessible.  Specifically to make the code compliant with particular acceptance critera:

* GIVEN a webpage meets accessibility standards
 * WHEN I view the source code
  * THEN I find semantic HTML elements
 * WHEN I view the structure of the HTML elements
  * THEN I find that the elements follow a logical structure independent of styling and positioning
 * WHEN I view the image elements
  * THEN I find accessible alt attributes
 * WHEN I view the heading attributes
  * THEN they fall in sequential order
 * WHEN I view the title element
  * THEN I find a concise, descriptive title

------------------------------------------

Accomplishing this will give Horiseon Solutions a codebase that follows accessibility standards and be optimized for search engines.

The first thing I noticed about the Horiseon Site is that one of the links did not function.  

When I took a look at the HTML code I found very few semantic elements.  It was mostly <divs>.  The CSS code contained many reduntant selectors.

I made the HTML more semantic by replacing <divs> with elements <header>, <nav>, <main>, <aside>, <section>, and <footer>.  This makes it easier to distinguish which code is creating/modifying particular segments of the Horiseon Web Page.   


### Summary of HTML semantic improvements:

Improvement# | Old HTML | Change | New HTML
-------|-------|---------|-----------
 1 | Line 7 | Titled Site "Horiseon Solutions" | Line 8
 2 | Line  11 | Replaced <div> with  <header> | Line 15
 3 | Line 12 | Assigned class "logo" | Line 17
 4 | Line 13 | Replaced <div> with <nav> | Line 19
 5 | Line 13 | Assigned class "links" | Line 19
 6 | Line 27 | Assigned class and title "background-image" | Line 40
 7 | Line 28 | Replaced <div> with <main> | Line 43
 8 | Line 28 | Reassigned class to "services" | Line 43
 9 | Line 29 | Replaced <div> with <section> | Line 46
10 | Line 29 | Reassigned class to "service-section" | Line 46
11 | Line 29 | Restored link functionality by adding id | Line 46
12 | Line 30 | Added alt attribute to <img> | Line 48
13 | Line 36 | Replaced <div> with <section> | Line 58
14 | Line 36 | Reassigned class to "service-section" | Line 58
15 | Line 37 | Added alt attribute to <img> | Line 60
16 | Line 43 | Replaced <div> with <section> | Line 70
17 | Line 43 | Reassigned class to "service-section" | Line 70
18 | Line 44 | Added alt attribute to <img> | Line 72
19 | Line 51 | Replaced <div> with <aside> | Line 84
20 | Line 52 | Replaced <div> with <section> | Line 87
21 | Line 54 | Added alt attribute to <img> | Line 90
22 | Line 59 | Replaced <div> with <section> | Line 98
23 | Line 61 | Added alt attribute to <img> | Line 101
24 | Line 66 | replaced <div> with <section> | Line 109
25 | Line 68 | Added alt attribute to <img> | Line 112
26 | Line 74 | Replaced <div> with <footer> | Line 122


Summary of CSS improvements coming soon


HTML
Also on line 46 (Old 29) : Restored Link functionality by assigning id="search-engine-optimization"

HTML
Also changed class to "service-section" to reduce redunancy in the CSS.  Repeated this for sections on line 58 (Old 36) and line 70 (Old 43)

CSS
These three sections were styled exactly the same way by three different CSS Selectors (Old 138, 147, 156.)  Giving them all the same semantic class "service-section" allowed them all to be styled with one selector (New 67)



