+++
author = ["Timothy Chung"]
categories = ["Further Mathematics", "Mathematics"]
date = 2020-09-25T16:00:00Z
description = ""
image = "/images/tayser.jpg"
tags = ["Binomial Expansion", "Taylor Series"]
title = "Square Root Shortcuts, the Taylor Series, and Binomial Expansion"

+++
In the past few weeks I've come up with lots of new realisation of the topics thought to us in Maths.

{{< youtube "https://www.youtube.com/embed/PJHtqMjrStk" >}}

I came across this square root shortcut video a year ago. It is a simple way of estimating a square root of a non-square number using square numbers that are close in value to it. It gets more accurate for larger numbers and if the nearest square numbers are more close.

Tl;Dw : To find a square root of a number, say 87, we find a square number closest to it, 81. We know sqrt(81) = 9. We take this value, and add a fraction consisting of the difference between the two numbers 87 and 81 over two times 9.

It sounds complicated, so I'll notate it here:

\\begin{equation}\\sqrt{87}\\approx\\ \\sqrt{81}+\\frac{87-81}{2\\sqrt{81}}\\\\\\sqrt{87}\\approx\\ 9+\\frac{6}{18}\\\\ \\sqrt{87} \\approx\\ 9.333\\end{equation}

This allows for the formula:

\\begin{equation}x \\approx \\ a+\\frac{x^{2}-a^{2}}{2a} \\end{equation}

And as you can see, the estimated value is pretty close to the actual value.

\\begin{equation}\\sqrt{87}\\ = 9.32737 \\dots \\\\ \\mathrm{Estimated \\ value:\\ }9.33333 \\dots \\end{equation}

I was very curious why it worked. I derived a few methods:

### IGCSE Level Method (Basic Level Algebra)

\\begin{equation}\\mathrm{Let\\ } x\\ \\mathrm{be\\ the\\ square\\ root\\ we\\ wish\\ to\\ find\\ } \\\\ \\mathrm{Let\\ } a\\ \\mathrm{ be\\ the\\ small\\ difference\\ (fractional\\ part)}\\\\ \\mathrm{that\\ when\\ added\\ to\\ the\\ known\\ root\\ } k, \\mathrm{ their\\ sum\\ forms\\ } x\\\\x = (k+a) \\rightarrow \[1\]\\\\ \\\\x^{2} = (k+a)^{2}\\\\ \\mathrm{Consider\\ the\\ R.H.S.:}\\\\ \\\\(k+a)^{2} = k^{2} + 2ak + a^{2}\\\\(k+a)^{2} \\approx k^{2} + 2ak\\\\ \\\\ \\mathrm{Since\\ a\\ is\\ small,\\ a^{2} can\\ be\\ ignored}\\\\ \\\\ x^{2} \\approx k^{2} + \\mathrm{Rearranging\\ the\\ equation\\ for\\ a:} \\\\ x^{2} - k^{2}\\approx 2ak\\\\ \\frac{x^{2} - k^{2}}{2k}\\approx a\\\\ \\\\ \\mathrm{Plugging\\ a\\ back\\ into\\ equation\\ \[1\]:} \\\\x = k+a \\\\x \\approx k + \\frac{x^{2} - k^{2}}{2k}\\\\ \\mathrm{Plugging\\ our\\ values\\ in:} \\\\ k = 9 \\\\ x^2 = 87 \\\\x \\approx k + \\frac{x^{2} - k^{2}}{2k}\\\\ \\\\x \\approx 9 + \\frac{87 - 81}{18}\\\\ \\\\x \\approx 9.3333\\\\ \\end{equation}

### A Level Maths Method 1 (Newton-Raphson Method for estimating roots)

\\begin{equation}\\mathrm{We\\ want\\ to\\ find\\ the\\ square\\ root\\ value\\ } x\\ \\mathrm{such\\ that:\\ }\\\\ k^{2} + d = x^{2}\\\\\\mathrm{Where\\ } k^{2}\\ \\mathrm{is \\ the\\ square\\ number\\ with\\ the \\ known\\ root\\ } k\\ \\mathrm{ and\\ } \\\\ d\\ \\mathrm{is\\ the\\ difference\\ of\\ the\\ two\\ squares}\\\\\\mathrm{ To\\ find\\ the\\ root\\ of\\ the\\ equation:\\ }\\\\x^{2} - d - k^{2} = 0\\mathrm{Let\\ } f(x) = x^{2} - d - k^{2}\\\\ \\mathrm{We\\ could\\ solve\\ quadratically,\\ but\\ it\\ would\\ require\\ square\\ root\\ calculations\\ which\\ we\\ want\\ to\\ avoid.} \\\\ \\mathrm{We\\ can\\ instead\\ estimate\\ using\\ the\\ Newton{\\text -}Raphson\\ method:\\ }\\\\ f'(x) = 2x \\\\ x_1=x_0−\\frac{f(x\_0)}{f'(x_0)}\\\\ \\mathrm{Substitute\\ } k\\ \\mathrm{into\\ } x_0\\ \\mathrm{as\\ value\\ of\\ } k\\ \\mathrm{is\\ close\\ to\\ the\\ solution\\ (which\\ is\\ x) } \\\\ x_1 =k −\\frac{k^{2}-d-k^{2}}{2(k)}\\\\ =k +\\frac{d}{2k}\\mathrm{Plugging\\ our\\ values\\ in:} \\\\ d = 6\\\\ k^{2} = 81 \\\\ x^{2} = 87\\\\k +\\frac{d}{2k}=9 +\\frac{6}{18}= 9.333\ \end{equation}

### A Level Maths Method (Binomial Series Expansion to non-integer/negative powers)

\\begin{equation}\\mathrm{Let\\ } x\\ \\mathrm{be\\ the\\ square\\ root\\ we\\ wish\\ to\\ find\\ } \\\\ \\mathrm{Let\\ } a\\ \\mathrm{ be\\ the\\ difference\\ between\\ the\\ known\\ square\\ number\\ } k^{2} \\\\ \\mathrm{and\\ } x^{2}\\\\x^{2} = (k^{2}+a) \\rightarrow \[1\]\\\\  
\\\\ \\mathrm{Consider\\ the\\ R.H.S.:} \\\\(k^{2}+a)^\\frac{1}{2} = (k^{2}(1+\\frac{a}{k^{2}}))^{\\frac{1}{2}} \\\\= \\ k(1+ \\frac{a}{k^{2}})^{\\frac{1}{2}} \\\\\\mathrm{Using\\ the\\ Binomial\\ Series\\ Expansion: \\ } \\\\ \\approx k(1+\\frac{1}{2}\\cdot \\frac{a}{k^{2}}+\\frac{\\frac{1}{2}(\\frac{1}{2}-1)}{2!}\\cdot (\\frac{a}{k^{2}})^{2}+\\frac{\\frac{1}{2}(\\frac{1}{2}-1)(\\frac{1}{2}-2)}{3!}\\cdot (\\frac{a}{k^{2}})^{3}+ \\dots )\\\\ \\mathrm{We\\ can\\ ignore\\ terms\\ of\\ a^{2} or\\ more\\ as\\ they\\ become\\ increasingly\\ smaller.} \\\\ \\mathrm{Simplifying\\ gets\\ us:\\ }\\\\ R.H.S\\ = k(1+\\frac{a}{2k^{2}})\\\\=k+\\frac{a}{2k}\\end{equation}\\begin{equation}\\mathrm{Plugging\\ our\\ values\\ in:} \\\\ d = 6\\\\ k^{2} = 81 \\\\k=9\\\\ x^{2} = 87\\\\k +\\frac{d}{2k}=9 +\\frac{6}{18}= 9.333 \\end{equation}

### Further Pure Mathematics Method (Taylor Series Expansion)

\\begin{equation}\\mathrm{Using\\ the\\ Taylor\\ Series\\ Expansion:}\\\\ \\\\\\\\f(x) = f(a)+\\frac{f'(a)}{1!}(x-a)+\\frac{f''(a)}{2!}(x-a)^{2}+\\frac{f'''(a)}{3!}(x-a)^{3}+\\dots, \\end{equation}

\\begin{equation} \\\\Let\\ f(x) = x^{\\frac{1}{2}}\\\\ Let\\ x = (k^{2}+d)\\\\x\\ \\mathrm{is\\ the\\ number\\ whose\\ square\\ root\\ we\\ wish\\ to\\ find\\ } \\\\ \\mathrm{Let\\ } d\\ \\mathrm{ be\\ the\\ difference\\ between\\ the\\ known\\ square\\ number\\ } k^2 \\\\ \\mathrm{and\\ } x \\\\\\\\ f(x)=(k^{2}) ^{{\\frac{1}{2}}}+\\frac{\\frac{1}{2}(k^{2})^{-\\frac{1}{2}}(d)}{1!} +\\frac{-\\frac{1}{4}(k^{2})^{-\\frac{3}{2}}(d)}{2!} +\\frac{-\\frac{3}{8}(k^{2})^{-\\frac{5}{2}}(d)}{3!} + \\cdots \\\\\\ \\mathrm{We\\ take\\ the\\ first\\ two\\ terms\\ and\\ disregard\\ the\\ other\\ smaller\\ terms:\\ }\\\\ f(x)\\approx (k^{2}) ^{{\\frac{1}{2}}}+\\frac{\\frac{1}{2}(k^{2})^{-\\frac{1}{2}}(d)}{1!}\\\\ f(x)\\approx k+\\frac{d}{2k}\\\\\\mathrm{Plugging\\ our\\ values\\ in:} \\\\ d = 6\\\\ k^{2} = 81 \\\\k=9\\\\ x^{2} = 87\\\\k +\\frac{d}{2k}=9 +\\frac{6}{18}= 9.333 \\end{equation}

At this point of research, I am intrigued by how similar the Taylor Series is similar to the binomial expansion formula (a+b)^n. Most of my understanding is credited to 3Blue1Brown, who has done an amazing video on the Taylor Series.

{{< youtube "https://www.youtube.com/embed/3d6DsjIBzJ4" >}}

Back to my point, how does the Taylor Series relate to the binomial expansion? And because the Taylor Series an infinite series, why does binomial expansion terminate for positive integer power values, and not for negative non-integer power values? (This was a question I had while doing Pure Year 2)

Well, the secret lies in differentiation.

Back to the drawing board:

\begin{equation}\\mathrm{Using\\ the\\ Taylor\\ Series\\ Expansion:}\\\\ \\\\\\\\f(x) = f(a)+\\frac{f'(a)}{1!}(x-a)+\\frac{f''(a)}{2!}(x-a)^{2}+\\frac{f'''(a)}{3!}(x-a)^{3}+\\dots, \\\\Let:\\\\ \\\\ g(x) = x^{\\frac{3}{2}}\\\\h(x) = x^{3}\\\\ x = (a+b)\\\\ \end{equation}

Here are their respective expansions:

\begin{equation}g(x) = a^{\\frac{3}{2}}+\\frac{\\frac{3}{2}a^{\\frac{1}{2}}}{1!}(b)+\\frac{\\frac{3}{4}a^{-\\frac{1}{2}}}{2!}(b^{2})+\\frac{-\\frac{3}{8}a^{-\\frac{3}{2}}}{3!}(b^{3})+\\dots,
\\\\h(x) = a^{3}+\\frac{3a^{2}}{1!}(b)+\\frac{6a^{1}}{2!}(b^{2})+\\frac{6}{3!}(b^{3})+\\dots,\end{equation}

But hold on! Shouldn't h(x) terminate?

It does: As powers of _a_ decrease by 1, they should reach a^0, which is 1. Differentiating to any higher orders will return zero, so the expression terminates.

\begin{equation}\\\\h(x) = a^{3}+\\frac{3a^{2}}{1!}(b)+\\frac{6a^{1}}{2!}(b^{2})+\\frac{6}{3!}(b^{3})+\\frac{f'(6)}{4!}(b^{4})+ \\frac{f''(6)}{5!}(b^{5})+\\dots,\\\\h(x) = a^{3}+\\frac{3a^{2}}{1!}(b)+\\frac{6a^{1}}{2!}(b^{2})+\\frac{6}{3!}(b^{3})+0(b^{4})+ 0(b^{5})+\\dots, \end{equation}

Looking at g(x), if the power is negative, it keeps on differentiating infinitely. Even though it is positive, if it is non-integer differentiating it causes it to skip past 0 from positive to negative, and it goes on forever as well.