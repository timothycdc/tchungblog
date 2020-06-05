+++
author = ["Timothy"]
categories = ["Further Maths"]
date = 2020-03-14T09:40:24Z
description = "This is meta description. Can you read this?"
draft = true
image = "/images/img_51d217ee2fc1-1.jpeg"
tage = ["tags"]
tags = ["Vectors", "Trigonometry", "Maths"]
title = "Draft"

+++
Last term, we learned about vectors in Core Pure Maths. I was curious on how the formula was derived, so after some experimentation, I used IGCSE-Level trigonometry to get to the answer.

\\begin{equation} 
Using\ the\ cos\ rule:\\\\\left|A\right|^{2}+\left|B\right|^{2}-2\left|A\right|\left|B\right|\cos\theta=\left(AB\right)^{2}\\\\\left|A\right|^{2}+\left|B\right|^{2}-\left(AB\right)^{2}=2\left|A\right|\left|B\right|\cos\theta\\\\w^{2}+y^{2}+x^{2}+z^{2}-\left(x+z\right)^{2}-\left(w-y\right)^{2}=2\left|A\right|\left|B\right|\cos\theta\\\\w^{2}+y^{2}+x^{2}+z^{2}-\left(x^{2}+2zx+z^{2}\right)-\left(w^{2}-2wy+z^{2}\right)=2\left|A\right|\left|B\right|\cos\theta\\\\2wy-2zx=2\left|A\right|\left|B\right|\cos\theta\\\\wy-zx=\left|A\right|\left|B\right|\cos\theta\\\\\frac{\left(wy-zx\right)}{\left|A\right|\left|B\right|}=\cos\theta\\\\\frac{A\cdot B}{\left|A\right|\left|B\right|}=\cos\theta
\\end{equation}

After finishing Core Pure 1's Trigonometry chapters, I used some new trigonometry formulas recently learned to simplify the derivation.

\\begin{equation}
\\cos\\left(a+b\\right)=\\cos a\\cos b-\\sin a\\sin b
\\\\ =\\left(\\frac{w}{\\sqrt{w^{2}+x^{2}}}\\times\\frac{y}{\\sqrt{y^{2}+z^{2}}}\\right)-\\left(\\frac{x}{\\sqrt{w^{2}+x^{2}}}\\times\\frac{z}{\\sqrt{y^{2}+z^{2}}}\\right)\\\\=\\frac{wy-xz}{\\sqrt{w^{2}+x^{2}}\\sqrt{y^{2}+z^{2}}}\\\\ =\\frac{A\\cdot B}{\\left|A\\right|\\left|B\\right|}
\\end{equation}

Well, that concludes it! A little bit of proofing for today, done. Stay tuned for more maths posts!