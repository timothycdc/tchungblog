+++
author = ["Timothy"]
categories = ["Further Maths"]
date = 2020-06-04T09:40:24Z
description = "This is meta description. Can you read this?"
image = "/images/image-06-07-2020-at-10-49-pm.JPG"
tage = ["tags"]
tags = ["Vectors", "Trigonometry", "Maths"]
title = "Angle Between Two Vectors Formula"

+++
Last term, we learned about vectors in Core Pure Maths. I was curious on how the formula was derived, so after some experimentation, I used IGCSE-Level trigonometry to get to the answer.

![](/images/img_5c8404ec2a3c-1.jpeg)(Swipe or click+arrow keys to scroll through the workings, it may take a few seconds to load)

\\begin{equation} Using\\ the\\ cos\\ rule\\ for\\ Figure\\ 1:\\\\\\left|OA\\right|^{2}+\\left|OB\\right|^{2}-2\\left|OA\\right|\\left|OB\\right|\\cos\\theta=\\left(AB\\right)^{2}\\\\\\left|OA\\right|^{2}+\\left|OB\\right|^{2}-\\left(AB\\right)^{2}=2\\left|OA\\right|\\left|OB\\right|\\cos\\theta\\\\w^{2}+y^{2}+x^{2}+z^{2}-\\left(x+z\\right)^{2}-\\left(w-y\\right)^{2}=2\\left|OA\\right|\\left|OB\\right|\\cos\\theta\\\\w^{2}+y^{2}+x^{2}+z^{2}-\\left(x^{2}+2zx+z^{2}\\right)-\\left(w^{2}-2wy+z^{2}\\right)=2\\left|OA\\right|\\left|OB\\right|\\cos\\theta\\\\2wy-2zx=2\\left|OA\\right|\\left|OB\\right|\\cos\\theta\\\\wy-zx=\\left|A\\right|\\left|B\\right|\\cos\\theta\\\\\\frac{\\left(wy-zx\\right)}{\\left|OA\\right|\\left|OB\\right|}=\\cos\\theta\\\\\\frac{a\\cdot b}{\\left|OA\\right|\\left|OB\\right|}=\\cos\\theta \\end{equation}

After finishing Core Pure 1's Trigonometry chapters, I used some new trigonometry formulas recently learned to simplify the derivation.

\\begin{equation} \\cos\\left(a+b\\right)=\\cos a\\cos b-\\sin a\\sin b \\\\ =\\left(\\frac{w}{\\sqrt{w^{2}+x^{2}}}\\times\\frac{y}{\\sqrt{y^{2}+z^{2}}}\\right)-\\left(\\frac{x}{\\sqrt{w^{2}+x^{2}}}\\times\\frac{z}{\\sqrt{y^{2}+z^{2}}}\\right)\\\\=\\frac{wy-xz}{\\sqrt{w^{2}+x^{2}}\\sqrt{y^{2}+z^{2}}}\\\\ =\\frac{a\\cdot b}{\\left|OA\\right|\\left|OB\\right|} \\end{equation}

It's interesting to see the cosine addition formula reduce the number of lines of the working. Also, note how the left hand side of the equation slowly takes the shape of the **dot product.**

The only issue is that using the cosine addition simplifies the formula for 2-dimensional vectors. What about 3-dimensional vectors?

Let's go back to the first equation , but now vectors a and b have a component of (g,h,i) and (j,k,l) respectively.

\\begin{equation}\\vec{a}^{\\,}=\\left(g,\\ h,\\ i\\right) \\and \\\\vec{b}^{\\,}=\\left(j,\\ k,\\ l\\right) \\\\\\\\\\\\left|OA\\right|^{2}+\\left|OB\\right|^{2}-2\\left|OA\\right|\\left|OB\\right|\\cos\\theta=\\left(AB\\right)^{2}\\\\\\left|OA\\right|^{2}+\\left|OB\\right|^{2}-\\left(AB\\right)^{2}=2\\left|OA\\right|\\left|OB\\right|\\cos\\theta\\\\w^{2}+y^{2}+x^{2}+z^{2}-\\left(x+z\\right)^{2}-\\left(w-y\\right)^{2}=2\\left|OA\\right|\\left|OB\\right|\\cos\\theta\\\\w^{2}+y^{2}+x^{2}+z^{2}-\\left(x^{2}+2zx+z^{2}\\right)-\\left(w^{2}-2wy+z^{2}\\right)=2\\left|OA\\right|\\left|OB\\right|\\cos\\theta\\\\2wy-2zx=2\\left|OA\\right|\\left|OB\\right|\\cos\\theta\\\\wy-zx=\\left|A\\right|\\left|B\\right|\\cos\\theta\\\\\\frac{\\left(wy-zx\\right)}{\\left|OA\\right|\\left|OB\\right|}=\\cos\\theta\\\\\\frac{a\\cdot b}{\\left|OA\\right|\\left|OB\\right|}=\\cos\\theta \\end{equation}

I haven't looked much into this, although 3Blue1Brown has a video about it [here](https://www.youtube.com/watch?v=LyGKycYT2v0). At 6:27, the video shows that a dot product of two vectors is simply mapping one onto the other. I will have to look further into this, and also the **cross product,** which was removed from the exam specification for some reason..

Well, that concludes a little bit of proving for today. Stay tuned for more maths posts!