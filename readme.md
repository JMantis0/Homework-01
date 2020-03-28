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

When I took a look at the HTML code I found very few semantic elements.  It was mostly `<div>`s.  The CSS code contained many reduntant selectors.

I made the HTML more semantic by replacing `<div>`s with elements `<header>`, `<nav>`, `<main>`, `<aside>`, `<section>`>, and `<footer>`.  This makes it easier to distinguish which code is creating/modifying particular segments of the Horiseon Web Page.   


### Summary of HTML semantic improvements:

Improvement# | Old HTML | Change | New HTML
-------|-------|---------|-----------
 1 | Line 7 | Titled Site "Horiseon Solutions" | Line 8
 2 | Line  11 | Replaced `<div>` with  ``<header>`` | Line 15
 3 | Line 12 | Assigned class "logo" | Line 17
 4 | Line 13 | Replaced `<div>` with `<nav>` | Line 19
 5 | Line 13 | Assigned class "links" | Line 19
 6 | Line 27 | Assigned class and title "background-image" | Line 40
 7 | Line 28 | Replaced `<div>` with `<main>` | Line 43
 8 | Line 28 | Reassigned class to "services" | Line 43
 9 | Line 29 | Replaced `<div>` with `<section>`> | Line 46
10 | Line 29 | Reassigned class to "service-section" | Line 46
11 | Line 29 | Restored link functionality by adding id | Line 46
12 | Line 30 | Added alt attribute to `<img>` | Line 48
13 | Line 36 | Replaced `<div>` with `<section>`> | Line 58
14 | Line 36 | Reassigned class to "service-section" | Line 58
15 | Line 37 | Added alt attribute to `<img>` | Line 60
16 | Line 43 | Replaced `<div>` with `<section>`> | Line 70
17 | Line 43 | Reassigned class to "service-section" | Line 70
18 | Line 44 | Added alt attribute to `<img>` | Line 72
19 | Line 51 | Replaced `<div>` with `<aside>` | Line 84
20 | Line 52 | Replaced `<div>` with `<section>`> | Line 87
21 | Line 54 | Added alt attribute to `<img>` | Line 90
22 | Line 59 | Replaced `<div>` with `<section>`> | Line 98
23 | Line 61 | Added alt attribute to `<img>` | Line 101
24 | Line 66 | replaced `<div>` with `<section>`> | Line 109
25 | Line 68 | Added alt attribute to `<img>` | Line 112
26 | Line 74 | Replaced `<div>` with `<footer>` | Line 122

I made the CSS more semantic by changing the selectors to select the classes that I changed in the HTML.  I also consolidated several sets of redundant selectors to make the code shorter and less confusing.

### Summary of CSS semantic improvements:
Improvement# | Old CSS | Change | New CSS
-------|-------|---------|-----------
 1 | Line 19 | Replaced selector `.header h1` with `.logo` | Line 19
 2 | Line 24 | Replaced selector `.header h1 .seo` with `.logo-middle` | Line 24
 3 | Line 28 | Replaced selector `.header div` with `.links` | Line 28
 4 | Line 36 | Replaced selector `.header div u1` with `u1` | Line 36
 5 | Line 40 | Replaced selector `.header div ul li` with `li`| Line 40
 6 | Line 54 | Replaced selector `.hero` with `#background-image` | Line 51
 7 | Line 73 | Replaced selector `.content` with `.services` | Line 61
 8 | Line 138 | Replaced 3 selectors `.search-engine-optimization`, `.online-reputation-management`, and `.social-media-marketing` with 1 `.service-section` | Line 67
 9 | Line 177 | Replaced 3 selectors `.search-engine-optimization h2`, `.online-reputation-management h2`, and `.social-media-marketing h2` with 1 `h2` | Line 76
 10 | Line 165 | Replaced 3 selectors `.search-engine-optimization img`, `.online-reputation-management img`, `.social-media-marketing img` with 1 `.service-section img` | Line 81
 11 | Line 90 | Replaced 3 selectors `.benefit-lead`, `.benefit-brand`, and `.benefit-cost` with 1 `benefit-section` | Line 111
 12 | Line 105 | Replaced 3 selectors `.benefit-lead h3`, `.benefit-brand h3`, and `.benefit-cost h3` with 1 `benefit-section h3` | Line 116
 13 | Line 120 | Replaced 3 selectors `.benefit-lead img`, `.benefit-brand img`, and `.benefit-cost img` with 1 `.benefit-section img` | Line 121
 14 | Line 199 | Replaced selector `.footer h2` with `h4` | Line 35


## Overall effect of improvements

The improved semantic HTML elements assist the viewer in identifying which peices of code apply to which parts of the website.  The improved indentation and spacing reduces clutter, and the comments add more clarity to what the code is doing.

The improved semantic CSS elements assist the viewer in identifying what parts of the site are being styled by the selectors.  Also, the CSS is also free of reduntant selectors, reducing clutter and confusion for the viewer.  Finally, selectors are placed in the order in which their corresponding elements appear in the HTML, making it even easier to find which HTML elements are being selected by the CSS.

Finally, when viewing the improved HTML and CSS side by side, both files are roughly the same number of lines, which is aesthetically preferable and again helps the viewer by reducing confusion as to what particular peices of code are doing.



