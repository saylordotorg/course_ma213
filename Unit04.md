---
layout: default
title: "MA213: Numerical Analysis"
course_description: "An exploration of the methods used to solve problems involving continuous variables."
next: ../Unit05
previous: ../Unit03
---
**Unit 4: Differentiation and Integrations of Functions** <span
id="4"></span> 
*Before we talk about differential equations, we should expect some
calculus.  In this unit, we will address one of the most fundamental
challenges of floating point arithmetic: finding the slope of a tangent
line.  You will see that numerical differentiation is actually harder
than numerical integration!  That said, numerical integration is
especially interesting for all of the new ideas that we can explore.  We
will also create an algorithm (and write a program) that adapts itself
to different integration problems.*

**Unit4 Learning Outcomes**  
Upon successful completion of this unit, the student will be able to:  
-   Approximate the slope of a function at a point, and to approximate
    the definite integral of an integrable function. 
-   In addition, you will understand a fundamental difficulty of
    scientific computation: discrete calculus.

**4.1 Numerical Differentiation** <span id="4.1"></span> 
**4.1.1 Finite Difference Formulas** <span id="4.1.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Numerical
    Differentiation is Easy”**
    Link: University of Arkansas: Mark Arnold’s “[Numerical
    Differentiation is
    Easy](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  We
    will play this game again and again: If we approximate a function f
    by an interpolating polynomial P, then D(f) is approximately D(P). 
    Here D is the derivative operator, and the formulas are called
    finite difference formulas.  Every different interpolating
    polynomial gives a different finite difference formula for the slope
    of f at a point.  The formulas here are given by uniformly spaced
    nodes, but you can make up your own formulas for any set of
    (pairwise distinct) nodes.  
        
     This resource should take approximately 1 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Differentiation of Continuous Functions”**
    Link: YouTube: University of South Florida: Autar Kaw’s
    “[Differentiation of Continuous
    Functions](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 6
    lectures that have been split into 9 videos.  
        
     This resource should take approximately 1 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**4.1.2 In the Face of Rounding Errors** <span id="4.1.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Numerical
    Differentiation is Hard”**
    Link: University of Arkansas: Mark Arnold’s “[Numerical
    Differentiation is
    Hard](http://www.uark.edu/~arnold/4363/pages.html)" (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Please carefully read the
    pdf.  As easy as it was for us to find finite difference formulas,
    they depend on h being small.  In finite precision arithmetic there
    is a limit to how small h can be.  Are you clear about how
    truncation error and rounding error conspire to compromise your
    derivative estimate?  Explain why higher order formulas ameliorate
    this problem.  
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.  
      

**4.2 Quadrature** <span id="4.2"></span> 
**4.2.1 Newton-Cotes Rules** <span id="4.2.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Quadrature”**
    Link: University of Arkansas: Mark Arnold’s
    “[Quadrature](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Please carefully read the
    pdf.  Again, if P approximates f, then I(P) is approximately I(f),
    right?  Well this time the answer is… yes!  Integrating a Lagrange
    interpolating polynomial for f, can give a very good approximation
    for the integral of f, even in the face of rounding errors.  What
    degree polynomial do we need if f oscillates m times over [a,b]?   
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**4.2.2 Composite Newton-Cotes Rules** <span id="4.2.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Numerical
    Integration is Easy”**
    Link: University of Arkansas: Mark Arnold’s “[Numerical Integration
    is Easy](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  The
    composite rule rules.  The property that the integral from a to b
    can be split into the sum of the integrals from a to c and c to b is
    fundamentally what make quadrature a nice problem.  The challenge
    now is to compute I(f) quickly.  In many situations, we have values
    of f already computed on a uniform grid (x\_{i+1}-x\_i = h, for all
    i).  Composite Simpson’s rule is a very popular choice among methods
    which require uniform spacing of nodes; can you argue why?  
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Trapezoidal Rule”**
    Link: YouTube: University of South Florida: Autar Kaw’s
    “[Trapezoidal Rule](http://numericalmethods.eng.usf.edu/videos/)”
    (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 8
    lectures that have been split into 9 videos.  
        
     This resource should take approximately 1 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Simpson’s 1/3 Rule”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Simpson’s
    1/3 Rule](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 4
    lectures that have been split into 6 videos.  
        
     This resource should take approximately 1 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**4.2.3 Adaptive Quadrature** <span id="4.2.3"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Adaptive
    Quadrature” and “Adaptive Quadrature: recursive m-file”**
    Link: University of Arkansas: Mark Arnold’s “[Adaptive
    Quadrature](http://www.uark.edu/~arnold/4363/pages.html)” (PDF) and
    “[Adaptive Quadrature: recursive
    m-file](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  If
    we do have the freedom to evaluate f at arbitrary points in [a,b],
    then maybe a uniform grid is not optimum.  There may be regions
    where f varies little, while on other regions f oscillates a lot. 
    How does the adaptive quadrature idea deal with such a function? Why
    do we require the error to be halved when we branch to a lower
    level?  Do you think our (wish) is more or less likely to be true as
    we branch to lower levels?  Could we create an adaptive method
    without an error estimate?  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**4.3 Of Things Not Covered** <span id="4.3"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Monte-Carlo
    Integration”**
    Link: University of Arkansas: Mark Arnold’s “[Monte-Carlo
    Integration](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf’s. 
    There are two families of integration techniques that we have
    omitted.  One, Gaussian quadrature, requires that we can evaluate f
    at arbitrary points in [a,b], but achieves double the accuracy of
    the uniformly spaced Newton-Cotes methods.  The other type of method
    is philosophically opposite to adaptive or Gaussian quadrature: 
    evaluate f at random points (not uniform, not optimal, not smart:
    random).  As you might guess, this type of method cannot compete
    with those we have discussed… unless we are integrating a function
    of many variables over a high dimensional region.  These Monte-Carlo
    methods are methods of last resort, and as such are very important
    indeed!  
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s “Gauss
    Quadrature Rule”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Gauss
    Quadrature Rule](http://numericalmethods.eng.usf.edu/videos/)”
    (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 7
    lectures that have been split into 9 videos.  
        
     This resource should take approximately 1.25 hours to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**4.4 Programming Case Study: Recursion and Adaptive Quadrature** <span
id="4.4"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Adaptive
    Quadrature Program”**

    Link: University of Arkansas: Mark Arnold’s “[<span
    class="Hyperlink3">Adaptive Quadrature
    Program</span>](http://www.uark.edu/~arnold/4363/Octave/prog)” (PDF)

     

    Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Write a recursive adaptive
    quadrature program that meets the specifications required on the
    assignment.

     

    This resource should take approximately 4 hours to complete.

     

    Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**Unit 4 Assessment** <span id="4.5"></span> 
-   **Assessment: The Saylor Foundation's "Unit 4 Assessment"**
    Link: The Saylor Foundation's "[Unit 4
    Assessment](https://resources.saylor.org/wwwresources/archived/site/wp-content/uploads/2012/08/MA213-Assessment-Unit4-FINAL.pdf)"
    (PDF) and “[Unit 4 Guide to
    Responding](https://resources.saylor.org/wwwresources/archived/site/wp-content/uploads/2012/08/MA213-Assessment-Unit4-GTR-FINAL.pdf)”
    (PDF).  
      
     Instructions: Carefully answer the two questions in this
    assessment.  You may consider them essay questions, but back up or
    explain with formulas and/or theorems as needed.  When you are
    finished, you should check yourself by looking at the response
    guide.  You may not have all of the points given in the response
    guide, or you may have noted something that was not included in the
    guide, and that may be just fine, but this is a time to reflect on
    differences between your response and the guide response and
    possibly review some material.


