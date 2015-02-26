---
layout: default
title: "MA213: Numerical Analysis"
course_description: "An exploration of the methods used to solve problems involving continuous variables."
next: ../Unit02
previous: ../Intro
---
**Unit 1: Computer Arithmetic** <span id="1"></span> 
*We see how real numbers are represented in computers for scientific
computation.  We cannot represent all real numbers, so we must choose
which finite subset of the real numbers we will use.  Most modern
scientific computing uses a set of floating point numbers.  The
properties of floating point numbers affect arithmetic; in fact, we do
not even expect the computer to add two numbers correctly.  We will
follow these errors through simple computations and learn some basic
rules and techniques for tracking errors.  Finally, we will write a
simple program that pays careful attention to these considerations.*

**Unit1 Learning Outcomes**  
Upon successful completion of this unit, the student will be able to:   
-   Be able to represent numbers using a normalized floating point
    representation.
-   Understand the implications of this representation on arithmetic and
    the ideas of swamping and cancellation. 
-   Analyze such errors and understand the ideas of forward and backward
    error analysis. 
-    Understand how conditioning analysis and backward stability combine
    to allow an estimate of overall error in a computation.

**1.1 Finite Representations of Real Numbers** <span id="1.1"></span> 
**1.1.1 Floating-Point Numbers** <span id="1.1.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Comparing Numbers”
    and “Floating Point Numbers”**
    Link: University of Arkansas: Mark Arnold’s [“Comparing
    Numbers”](http://www.uark.edu/~arnold/4363/pages.html) (PDF) and
    [“Floating Point
    Numbers”](http://www.uark.edu/~arnold/4363/pages.html) (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading.  The “Comparing Numbers”
    reading is here to get you thinking about how we measure errors in
    computation.  Our primary tool is the absolute difference relative
    to the true answer, or the relative error.  When is the relative
    error equal to the absolute error?  The Floating Point
    Representation Theorem and the Fundamental Axiom of Floating Point
    Arithmetic are the two basic rules we will use to estimate rounding
    errors.  
        
     This resource should take approximately 2 hours to complete.  
      
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Floating Point Representation”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Floating
    Point Representation](http://numericalmethods.eng.usf.edu/videos/)”
    (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 4
    lectures that have been split into 8 videos.  These lectures will be
    useful for all of units 1.1 and 1.2.  
        
     This resource should take approximately 1 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**1.1.2 Floating-Point Representation Theorem** <span
id="1.1.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Pictures of a Toy
    Floating Point System”**
    Reading: University of Arkansas: Mark Arnold’s “Pictures of a Toy
    Floating Point System”  
        
     Link: of Arkansas: Mark Arnold’s [“Pictures of a Toy Floating Point
    System”](http://www.uark.edu/~arnold/4363/pages.html) (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. This is a plot of a 1-byte (8
    bits) floating point system.  The floats are too close to each other
    on the top plot, so the subsequent plots are zoom-ins.  We want to
    relate the machine epsilon from the previous reading to points on
    this plot.  On the plot(s) identify the floating point range, and
    the machine epsilon.   
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.2 Fundamental Axiom of Floating-Point Arithmetic** <span
id="1.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Floating Point
    Arithmetic”**
    Link: University of Arkansas: Mark Arnold’s [“Floating Point
    Arithmetic”](http://www.uark.edu/~arnold/4363/pages.html) (PDF)  
        
     Instructions:. Click on the link above, then select the appropriate
    link to download a pdf of the reading.  Pretend you are a (base-10)
    computer and add and multiply some 4-decimal digit numbers.  Prove
    the Fundamental Axiom of Floating Point Arithmetic using the
    additional hypothesis that “an arithmetic operation on two such
    floating point numbers returns the floating point number closest to
    the true value”.  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.3 Error Analysis** <span id="1.3"></span> 
**1.3.1 Forward Error Analysis** <span id="1.3.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Error Analysis”**
    Link: University of Arkansas: Mark Arnold’s “[Error
    Analysis”](http://www.uark.edu/~arnold/4363/pages.html)(PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  This
    reading exhibits both a forward rounding error analysis and a
    backward rounding error analysis.  Make sure you clearly understand
    the distinction.  For the vast majority of computations a forward
    error analysis does not provide useful error bounds (they are too
    pessimistic).  Do a forward error analysis for the product of two
    real numbers; you should be able to mimic the forward analysis for
    a+b that is in the reading.  We will use this reading for the next
    section.  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.  
      

**1.3.2 Backward Error Analysis** <span id="1.3.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “What is a
    Solution?” and “Conditioning and Stability”**
    Link: University of Arkansas: Mark Arnold’s “[What is a
    Solution?](http://www.uark.edu/~arnold/4363/pages.html)” (PDF) and
    “[Conditioning and
    Stability](http://www.uark.edu/~arnold/4363/pages.html)”(PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. In the “Error Analysis”
    reading we show that if a, b and a+b are real numbers in the
    floating point range, then fl(a+b) is the exact sum of two numbers
    relatively close to a and b.  Do the same for fl(ab).  At this point
    you have seen that (i) while an addition (or subtraction) may be
    computed with large relative error, (ii) it is also the exact sum of
    two numbers very close to a and b.  Thus (ii) does not guarantee a
    small error.  You have shown that multiplication (which doesn’t
    over/underflow) will always be computed with small relative error. 
    We perform error analysis both to gain insight into a method (where
    are its weak points?) and to predict how good our computed solution
    is.  This reading shows how the relationship between backward error
    analysis and problem conditioning can give us an error estimate.    
        
     This resource should take approximately 3 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.3.3 Swamping and Cancellation** <span id="1.3.3"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Swamping and
    Cancellation” and “Three Perspectives on Cancellation”**
    Link: University of Arkansas: Mark Arnold’s “[Swamping and
    Cancellation](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)
    and “[Three Perspectives on
    Cancellation](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Rounding errors occur for
    nearly every arithmetic operation, but sometimes circumstances
    converge to set us up for a particularly bad result: cancellation. 
    You have seen cancellation in simple examples and in your forward
    error analysis.  Show that there is a risk of cancellation any time
    we additively compute a result that is small compared to its
    addends.  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.4 Programming Case Study: The Quadratic Formula** <span
id="1.4"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Computing the
    Roots of a Quadratic Polynomial” and “Implementing the Quadratic
    Equation”**
    Link: University of Arkansas: Mark Arnold’s “[Computing the Roots of
    a Quadratic
    Polynomial](http://www.uark.edu/~arnold/4363/pages.html)[”](http://www.uark.edu/~arnold/4363/pages.html) PDF and
    “[Implementing the Quadratic
    Equation”](http://www.uark.edu/~arnold/4363/Octave/prog) (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf. 
    Write a program in Octave that computes the roots of ax^2+bx+c given
    the real numbers a, b and c.  Make sure that your program does not
    divide by 0, that it does not suffer from cancellation (except
    possibly in b^2-4ac), and all input variables (a,b,c) and all output
    variables (r1, r2 maybe others?) are described carefully.  There is
    a good tutorial on Octave at
    <http://en.wikibooks.org/wiki/Octave_Programming_Tutorial>.  Since
    you already have some experience programming, Octave should be
    relatively easy to learn (it was born as a Matlab clone, and is very
    much like fortran90.  Matlab tutorials are plentiful on the web, you
    might find them useful as well).  As with learning most new
    languages, the learning curve is steep with gross syntax; but never
    fear, Octave is quite simple.  
        
     This resource should take approximately 10 hours to complete
    (including the Octave download/install process).  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.5 Of Things Not Covered** <span id="1.5"></span> 
-   **Reading: Penn State University: David Goldberg’s “What Every
    Computer Scientist Should Know about Floating Point Arithmetic”**
    Link: Penn State University: David Goldberg’s “[What Every Computer
    Scientist Should Know about Floating Point
    Arithmetic](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.22.6768)”
    (PDF)  
        
      Instructions: Click on the link above, and download the reading
    using the “Download Links” menu in the upper right corner.  Scan the
    paper so that you know what is covered.  This paper is a very good
    resource for the IEEE 754 standard.  You will want to have it as a
    reference as you work through the material in this course.  
        
     This resource should take approximately 4 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**Unit 1 Assessment** <span id="1.6"></span> 
-   **Assessment: The Saylor Foundation's "Unit 1 Assessment"**
    Link: The Saylor Foundation's "[Unit 1
    Assessment](http://www.saylor.org/site/wp-content/uploads/2012/06/MA213-Unit-1-Assessment-FINAL.pdf)"
    (PDF) and "[Guide to
    Responding](http://www.saylor.org/site/wp-content/uploads/2012/06/MA213-Unit-1-Assessment-GTR-FINAL.pdf)”
    (PDF).  
      
     Instructions: <span
    style="font-family: arial, sans-serif; font-size: 12.727272033691406px; ">Carefully
    answer the three questions below.  You may consider them essay
    questions, but back up or explain with formulas and/or theorems as
    needed.  When you are finished, you should check yourself by looking
    at the response guide.  You may not have all of the points given in
    the response guide, or you may have noted something that was not
    included in the guide, and that may be just fine, but this is a time
    to reflect on differences between your response and the guide
    response and possibly review some material.</span> This assessment
    should take about 40 minutes to complete.


