---
layout: default
title: "MA213: Numerical Analysis"
course_description: "An exploration of the methods used to solve problems involving continuous variables."
next: ../Unit04
previous: ../Unit02
---
**Unit 3: Nonlinear Equations of a Single Real Variable** <span
id="3"></span> 
*From the very first algebra course you took, you have been asked to
“find x” for many different problems.  You will now learn how to pass
that task on to the computer!  You might not be surprised to know that
there are slow-and-sure methods as well as fast-and-risky methods.  We
will develop tools that allow us to measure just how fast a given method
converges to an answer.  Some methods are best only in specialized
situations, and some work well generally or in combination with others. 
Finally, we will write programs to compare both the safest and fastest
of our methods.*

**Unit3 Learning Outcomes**  
Upon successful completion of this unit, the student will be able to:  
-   Understand the method of bisection, Newton’s method and the secant
    method for solving equations in one real variable. 
-   Be able to compare and contrast these methods with respect to
    several distinctive properties, and construct a hybrid method
    possessing desirable properties of each.

**3.1 Roots of Nonlinear Equations** <span id="3.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Solving Equations
    in one Real Variable”**

    Link: University of Arkansas: Mark Arnold’s “[<span
    class="Hyperlink3">Solving Equations in one Real
    Variable</span>](http://www.uark.edu/~arnold/4363/pages.html)”
    (PDF) 

    Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.

    This resource should take approximately 1 hour to complete.

    Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**3.2 The Method of Bisection** <span id="3.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Bisection”**
    Link: University of Arkansas: Mark Arnold’s
    “[Bisection](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Although it may not be clear
    yet, the method of bisection has some exceptional properties.  The
    fact that it can give us an upper bound on the error at each
    iteration is one such property.  The price we pay is a relatively
    slow speed of convergence and the need to begin with a root
    bracketing interval.  There is not much to analyze in this method,
    our fundamental computation is to compute the sign of f(p)
    correctly, where p=(a+b)/2.  Now it turns out that it is better to
    compute p as p=a+(b-a)/2.  Why?  
        
     This resource should take approximately 1.5 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Bisection Method”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Bisection
    Method](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 4
    lectures that have been split into 4 videos.  
        
     This resource should take approximately 40 minutes to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**3.3 The Newton-Raphson Method** <span id="3.3"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Newton’s Method”**
    Link: University of Arkansas: Mark Arnold’s “[Newton’s
    Method](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. So here is a classic and very
    simple use of the idea of linearization.  At each step we replace
    f(x) with the line tangent to f at (x\_p, f(x\_p)).  The new iterate
    x\_{p+1} is simply the root of that tangent line.  This method can
    be very fast, but is can also fail.  Can you think of two ways it
    can fail?  
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Newton-Raphson Method”**
    Link: YouTube: University of South Florida: Autar Kaw’s
    “[Newton-Raphson
    Method](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 6
    lectures that have been split into 9 videos.  
        
     This resource should take approximately 1 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**3.4 The Secant Method** <span id="3.4"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “The Secant Method”
    and “Newton & Secant Example”**
    Link: University of Arkansas: Mark Arnold’s “[The Secant
    Method](http://www.uark.edu/~arnold/4363/pages.html)” (PDF) and
    “[Newton & Secant
    Example](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf’s. 
    The secant method is a Newton-like method that is general purpose. 
    It is arguably faster than Newton’s method, but like Newton’s
    method, can fail.  
        
     This resource should take approximately 1.5 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s “Secant
    Method”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Secant
    Method](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 3
    lectures that have been split into 4 videos.  
        
     This resource should take approximately 1/2 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**3.5 Order of Convergence** <span id="3.5"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Order of
    Convergence”, “Convergence of Newton’s Method” and “Convergence of
    the Secant Method”**
    Link: University of Arkansas: Mark Arnold’s “[Order of
    Convergence](http://www.uark.edu/~arnold/4363/pages.html)” (PDF),
    “[Convergence of Newton’s
    Method](http://www.uark.edu/~arnold/4363/pages.html)” (PDF) and
    “[Convergence of the Secant
    Method](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf’s. 
    There is a lot in this section.  The idea of linearization we now
    associate with a Taylor polynomial.  The definition of order of
    convergence is worth putting to memory, and it is as easy as “the
    new error is approximately a constant times the old error raised to
    the alpha”.  If we have superlinear convergence, then we also have a
    useful (but not guaranteed) error estimate.  In light of this, you
    should think about how you could determine when to stop a Newton or
    secant iteration.  If someone said that Newton’s method was faster
    than the secant method, would you agree?  How would you argue your
    point?  
        
     This resource should take approximately 4 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**3.6 Hybrid Methods** <span id="3.6"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Hybrid Methods for
    Root Finding”**
    Link: University of Arkansas: Mark Arnold’s “[Hybrid Methods for
    Root Finding](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
      
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf. 
    There are other hybrid methods for the root finding problem.   The
    reading presents a simple example.  Construct a list of what
    properties your ideal method would have.  Does bisection combined
    with secant possess all of your properties?  Where (if at all) does
    this method fall short?  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “False-Position Method”**
    Link: YouTube: University of South Florida: Autar Kaw’s
    “[False-Position
    Method](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there is 1
    lecture that has been split into 3 videos.  
        
     This resource should take approximately 45 minutes to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**3.7 Programming Case Study: Compare Bisection and Secant** <span
id="3.7"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Bisection and
    Secant”**
    Link: University of Arkansas: Mark Arnold’s “[Bisection and
    Secant](http://www.uark.edu/~arnold/4363/Octave/prog)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. So, off to write your
    programs!  Please be careful about division by “something too close
    to zero”, but keep in mind the numerator may also be small…  Does
    your output look correct?  Does your stopping criterion match what
    is documented?  Are your programs carefully documented?  
        
     This resource should take approximately 4 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**3.8 Of Things Not Covered** <span id="3.8"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Roots of a
    Polynomial” and “Example of a Bad Polynomial”**
    Link: University of Arkansas: Mark Arnold’s “[Roots of a
    Polynomial](http://www.uark.edu/~arnold/4363/pages.html)"
    (PDF) and [“](http://www.uark.edu/~arnold/4363/pages.html)[Example
    of a Bad Polynomial](http://www.uark.edu/~arnold/4363/pages.html)”
    (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Maybe you have already
    thought of alternatives to Newton’s or the secant method.  There are
    alternatives.  When higher higher order derivatives are available,
    or when we know that a function is smooth enough, we can use
    polynomials of higher order (like Mueller’s method).  We can also
    use quadratic interpolation with the roles of x and y reversed; this
    is called inverse quadratic interpolation… There are many methods,
    even for problems with only one unknown variable; imagine what’s
    waiting to be invented for f(x\_1,x\_2,…,x\_n)=0?  Even for a
    polynomial function of 1 variable, finite precision arithmetic can
    make for challenging computational problems; the example in the
    reading is an ill posed polynomial root finding problem.  
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**Unit 3 Assessment** <span id="3.9"></span> 
-   **Assessment: The Saylor Foundation’s “Unit 3 Assessment”**
    Link: The Saylor Foundation’s “[Unit 3
    Assessment](https://resources.saylor.org/archived/wp-content/uploads/2012/08/MA213-Assessment-Unit3-FINAL.pdf)”
    (PDF) and “[Unit 3 Guide to
    Responding](https://resources.saylor.org/archived/wp-content/uploads/2012/08/MA213-Assessment-Unit3-GTR-FINAL.pdf)”
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


