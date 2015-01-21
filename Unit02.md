**Unit 2: Polynomials and Polynomial Interpolation** <span
id="2"></span> 
*Some say that 75% of applied mathematics is polynomials (the other 75%
being linear algebra!).  We will therefore use this unit to review some
things you already know about polynomials and (hopefully) introduce some
new ideas as well.  Here, we are primarily interested in using
polynomials to approximate unknown functions, more complicated
functions, or just sets of points.  Finally, we will write a program to
find a cubic polynomial that passes through two points with predefined
slopes. *

**Unit2 Learning Outcomes**  
Upon successful completion of this unit, the student will be able to:  
-   Carefully define and understand a polynomial as a vector, its power
    as an approximation tool, and several ways of representing it. 
-   Approximate functions and data sets with polynomials with an
    understanding of the errors associated with this approximation.

**2.1 Polynomial Functions** <span id="2.1"></span> 
**2.1.1 Definition of a Polynomial** <span id="2.1.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Polynomials” and
    “Polynomial Evaluation”**
    Link: University of Arkansas: Mark Arnold’s
    “[Polynomials](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)
    and “[Polynomial
    Evaluation](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf’s. 
    Refer to your linear algebra material, if needed, and determine the
    dimension of the vector space P\_n of all polynomials of degree n or
    less.  Write down two distinct bases for P\_n.  Why do you think
    Horner’s method is also called synthetic division?  
        
     This resource should take approximately 3 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.1.2 Weierstrauss Approximation Theorem** <span id="2.1.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “The Taylor
    Polynomial”**
    Link: University of Arkansas: Mark Arnold’s “[The Taylor
    Polynomial](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. The last two readings refer
    to the Weierstrauss Approximation Theorem.  In your own words,
    describe what the theorem implies about the ability of polynomials
    to approximate continuous functions.  What do you think (i) lots of
    wiggles, (ii) a sharp corner, and/or (iii) a large interval of
    approximation, means to the degree of an approximating polynomial?  
        
     This resource should take approximately 1 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.1.3 Vector Spaces of Polynomials** <span id="2.1.3"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Polynomials are
    Vectors”**
    Link: University of Arkansas: Mark Arnold’s “[Polynomials are
    Vectors](http://www.uark.edu/~arnold/4363/pages.html)" (PDF)  
      
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Notice that the definition
    for the inner product of two polynomials depends on an interval and
    a weight function.  Therefore there are many popular types of
    polynomial inner product, and we will choose an appropriate inner
    product depending on our application.  An inner product in a vector
    space defines a natural notion of length and angle.  Find a Calculus
    III formula that relates an inner product, vector lengths, and an
    angle.  How would you define the angle between two polynomials?  We
    skipped some algebra when finding the best polynomial approximation
    to a function f; fill in the gaps.  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.1.4 Fundamental Theorem of Algebra** <span id="2.1.4"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Fundamental
    Theorem of Algebra**
    Link: University of Arkansas: Mark Arnold’s “[Fundamental Theorem of
    Algebra](http://www.uark.edu/~arnold/4363/pages.html)" (PDF)  
      
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  As
    you see, the Fundamental Theorem of Algebra (FTA) is an existence
    theorem.  It does not tell us how to factor a polynomial.  We will
    discuss methods for factoring polynomials later.  The FTA does give
    us yet another way to represent a polynomial; describe how it allows
    us to represent a polynomial of degree n having real coefficients
    using n+1 real numbers (some possibly repeated).   Find a formula
    for the derivative of a polynomial p(x) in terms of its roots (hint:
    use the product rule).  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.2 Polynomial Interpolation** <span id="2.2"></span> 
**2.2.1 Taylor Polynomials** <span id="2.2.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “The Taylor
    Polynomial”, “Rate of Convergence” and “A Taylor Polynomial
    Picture”**
    University of Arkansas: Mark Arnold’s “The Taylor Polynomial”, “Rate
    of Convergence” and “A Taylor Polynomial Picture”  
        
     Link: University of Arkansas: Mark Arnold’s “[The Taylor
    Polynomial](http://www.uark.edu/~arnold/4363/pages.html)” (PDF),
    “[Rate of Convergence](http://www.uark.edu/~arnold/4363/pages.html)”
    (PDF) and “[A Taylor Polynomial
    Picture](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of each reading. In many ways the Taylor
    Polynomial is the central tool of mathematical physics, and hence
    applied mathematics, and engineering.  Find a calculus or physics
    text or website that introduces the differential equation modeling
    the simple pendulum.  It is fundamentally different than spring (or
    simple harmonic) motion.  We cannot solve the differential equation
    for the pendulum (the solution is impossible to write even as an
    integral of functions we know).  Show how the small angle
    approximation for the pendulum is a Taylor polynomial
    approximation.  You should memorize the formula for the Taylor
    polynomial P(x) of degree n about x\_0 for an arbitrary function
    f(x), including the error term.  Show that P^{(k)}(x\_0) =
    f^{(k)}(x\_0) for k=0,1,…,n.  Does this property define P?  
        
     This resource should take approximately 4 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Taylor’s Theorem Revisited”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Taylor’s
    Theorem Revisited](http://numericalmethods.eng.usf.edu/videos/)”
    (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  Here there are 4 lectures
    that have been split into 4 videos.  
        
     This resource should take approximately 1/2 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**2.2.2 Lagrange Interpolation** <span id="2.2.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Lagrange
    Interpolation” and “FFT Tease”**
    Link: University of Arkansas: Mark Arnold’s “[Lagrange
    Interpolation](http://www.uark.edu/~arnold/4363/pages.html)"
    (PDF) and "[FFT Tease](http://www.uark.edu/~arnold/4363/pages.html)"
    (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading.  Carefully read the pdf. 
    Yes, we have yet another way to represent a polynomial.  Show that
    if the nodes are distinct, then there is exactly one polynomial of
    degree \<= n passing through n+1 knots (hint: we know that there is
    at least one: the Lagrange interpolator P.  Assume there is another,
    say Q.  Think about the zeros if (P-Q)(x)…)  This existence and
    uniqueness means n+1 knots with distinct nodes represents a
    polynomial: the Lagrange interpolator.   The Vandermonde matrix is
    usually a hard matrix to work with, so the Lagrange (and other)
    pictures are applied more often.  But there is one place where the
    Vandermonde picture rules:  If the nodes are roots of unity (a set
    of n+1 points, including 1, which are equally spaced around the
    circle of radius 1 in the complex plane), then the Vandermonde
    picture is a discrete Fourier transform (DFT); we mention this
    because you may have heard of the FFT (one of the most important
    algorithms ever discovered).  The FFT is simply a fast way to solve
    this special Vandermonde system.  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Lagrangian Interpolation”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Lagrangian
    Interpolation](http://numericalmethods.eng.usf.edu/videos/)”
    (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 4
    lectures that have been split into 6 videos.  
        
     This resource should take approximately 50 minutes to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

-   **Lecture: YouTube: University of South Florida: Duc Nguyen’s
    “Discrete Fourier Transform”**
    Link: YouTube: University of South Florida: Duc Nguyen’s “[Discrete
    Fourier Transform](http://numericalmethods.eng.usf.edu/videos/)”
    (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 3
    lectures that have been split into 7 videos.  
        
     This resource should take approximately 1.6 hours to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**2.2.3 Hermite Interpolation** <span id="2.2.3"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Hermite
    Interpolation”**
    Link: University of Arkansas: Mark Arnold’s “[Hermite
    Interpolation](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.   The
    Hermite interpolator really shines when we know not only the knots,
    but also the slopes of the curve at each knot (for example, when
    solving an initial value problem).  What degree Hermite interpolator
    is required if there are two nodes?  Go ahead and work out the
    formula for the Hermite interpolator for (x\_0,y\_0), (x\_0,y’\_0),
    (x\_1,y\_1) and (x\_1,y’\_1).  This little polynomial is a real
    workhorse in computer aided design and manufacturing and
    differential equations!  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.2.4 General Polynomial Interpolation** <span id="2.2.4"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Kissing
    Polynomials”**
    Link: University of Arkansas: Mark Arnold’s “[Kissing
    Polynomials](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  It
    may be that we include this section for aesthetic (or theoretical)
    reasons.  Well, communicating an aesthetic is an important component
    of a mathematics course and we don’t want you underserved!   Explain
    how the Taylor polynomial, the Lagrange polynomial, and the Hermite
    polynomial are all special cases of the osculating polynomial
    (precisely what are the interpolation conditions for each?).  
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.3 Programming Case Study: A 2-Node Hermite Interpolator** <span
id="2.3"></span> 
**2.3.1 Principles of Good Programming** <span id="2.3.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Some Programming
    Principles”**
    Link: University of Arkansas: Mark Arnold’s “[Some Programming
    Principles](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
      
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. The reading describes several
    generally agreed upon principles of good code.  How you balance
    these is up to you, but they are all worth considering when writing
    any program.  
      
     This resource should take approximately 1 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.3.2 The Interpolator** <span id="2.3.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Constructing a
    Hermite Cubic Interpolator”**
    Link: University of Arkansas: Mark Arnold’s “[Constructing a Hermite
    Cubic Interpolator](http://www.uark.edu/~arnold/4363/Octave/prog)”
    (PDF)  
      
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. The reading describes the
    2-node Hermite interpolator in both the Lagrange and Vandermonde
    picture.  Write a program in Octave to compute either form of the
    Hermite cubic h(x) (you choose). Input will be the nodes, x\_0 and
    x\_1, the function values y\_0 and y\_1, and the slopes y’\_0 and
    y’\_1, and output will be either the coefficients of h in the
    standard ordered basis (Vandermonde picture), or the polynomials
    H\_{10}, H\_{11}, hat{H)\_{10} and hat{H}\_{11} in standard form. 
    Use your program to plot h, and by all means: play with your
    program!  What shapes can it make?  Can you break it?  What shapes
    are sensitive to small changes, etc.  
      
     This resource should take approximately 4 hours to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.4 Of Things Not Covered** <span id="2.4"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Interpolating
    Splines”, “Least Squares Approximation”, “Polynomial Least Squares
    Example”, and “Lagrange Interpolation Example”**
    Link: University of Arkansas: Mark Arnold’s “[Interpolating
    Splines](http://www.uark.edu/~arnold/4363/pages.html)” (PDF),
    “[Least Squares
    Approximation](http://www.uark.edu/~arnold/4363/pages.html)” (PDF),
    “[Polynomial Least Squares
    Example](http://www.uark.edu/~arnold/4363/pages.html)” (PDF), and
    “[Lagrange Interpolation
    Example](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    links to download the PDFs of the reading.  A drawback of working
    with polynomials is that they naturally oscillate, especially for
    high degree (a polynomial of degree n has n-1 critical points). 
    Furthermore, polynomials cannot form true corners, and require very
    high degree to approximate a corner well.  Polynomial spline
    functions are simply piecewise polynomial functions.  Polynomials
    can be pieced together smoothly or to form corners.  
        
     On the other hand, one might ask if interpolation is always the
    best approach to representing data.  For example, if one suspects
    that there may be errors in the knot values, then a useful
    alternative to interpolation is least squares approximation.  
        
     This resource should take approximately 5 hours to complete.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s “Spline
    Interpolation”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Spline
    Interpolation](http://numericalmethods.eng.usf.edu/videos/)”
    (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 4
    lectures that have been split into 6 videos.  
        
     This resource should take approximately 50 minutes to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**Unit 2 Assessment** <span id="2.5"></span> 
-   **Assessment: The Saylor Foundation's "Unit 2 Assessment"**
    Link: The Saylor Foundation's "[Unit 2
    Assessment](http://www.saylor.org/site/wp-content/uploads/2012/06/MA213-Unit-2-Assessment-FINAL.pdf)"
    (PDF) and  “[Guide to
    Responding](http://www.saylor.org/site/wp-content/uploads/2012/06/MA213-Unit-2-Assessment-GTR-FINAL.pdf)”
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
    response and possibly review some material. </span>This assessment
    should take about 30 minutes to complete.


