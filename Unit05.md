**Unit 5: Differential Equations** <span id="5"></span> 
*The subject addressed in this unit is where we have been headed from
the start of this course.  We now have the tools we need to understand
and construct methods to solve ordinary differential equations.  We will
begin by carefully defining our problem, if and when it has a solution,
and how we mean to approximate that solution.  Some methods will have
memory; some will not.  Some can adapt to the problem; some cannot. 
Some problems are particularly troublesome to some methods.  We will
develop many methods, and the art of the numerical analyst is to match a
given problem to an appropriate method.  Finally, we will implement an
adaptive hybrid method and test it on a challenging problem.*

**Unit5 Learning Outcomes**  
 Upon successful completion of this unit, the student will be able to:  
-   Define a well-posed initial value problem.
-   Convert high order initial value problems to first order initial
    value problems.
-   Have an understanding of single-step methods.
-   Have an understanding of multi-step methods.
-   Be able to identify a stiff initial value problem.
-   Be able to identify stable methods.
-   Know the shooting method for boundary value problems.

**5.1 Initial Value Problems** <span id="5.1"></span> 
**5.1.1 Definition and Slope Field** <span id="5.1.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “The IVP and
    Euler’s Method”**
    Link: University of Arkansas: Mark Arnold’s “[The IVP and Euler’s
    Method](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read first three
    paragraphs of the pdf.  If it helps, I think of an initial value
    problem as analogous to tracking the path of a leaf floating in a
    stream on a windless day.  The current of the stream is our slope
    field, f(t,y).  Can you think of other analogies.  
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**5.1.2 Well-Posed Initial Value Problems** <span id="5.1.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Can We Solve This
    IVP?”**
    Link: University of Arkansas: Mark Arnold’s “[Can We Solve This
    IVP?](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. We have talked about the
    conditioning of a problem.  In fact, the idea of conditioning is
    pre-dated by this idea of ‘wellposed-ness’.  A problem is either
    well-posed or ill-posed.  The conditioning of a problem is a finer
    measure of its difficulty.  Here is the connection: A problem is
    ill-posed if it is infinitely ill-conditioned.  Justify that
    statement.  Then explain why the existence of a bounded partial
    derivative of f with respect to y is sufficient for a continuous
    (IVP) to be well-posed.  
        
     This resource should take approximately 1 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**5.2 All Initial Value Problems Are First Order (If You Like)** <span
id="5.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Systems of
    Differential Equations” and “Example: High Order to First Order”**
    Link: University of Arkansas: Mark Arnold’s “[Systems of
    Differential
    Equations](http://www.uark.edu/~arnold/4363/pages.html)” (PDF) and
    “[Example: High Order to First
    Order](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download pdf’s of the reading. What we are working on here
    is a first order IVP.  Explain why the ability to solve first order
    systems of IVP’s essentially gives the ability to solve arbitrarily
    high order IVP’s (or systems thereof).  Remind yourself that what
    when we are developing methods for first order IVP’s, we are
    developing something much more general.  
        
     This resource should take approximately 3 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s “Higher
    Order/Coupled Differential Equations”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Higher
    Order/Coupled Differential
    Equations](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 4
    lectures that have been split into 8 videos.  
        
     This resource should take approximately 1 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**5.3 Single-Step Methods** <span id="5.3"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “The IVP and
    Euler’s Method” and “A Picture Euler’s Method”**
    Link: University of Arkansas: Mark Arnold’s “[The IVP and Euler’s
    Method](http://www.uark.edu/~arnold/4363/pages.html)” (PDF) and “[A
    Picture Euler’s
    Method](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download the pdf’s of the reading. Carefully study
    paragraphs 4 and 5 of the pdf, including the pseudocode.  The second
    reading should help you get a visual understanding.  Euler’s method,
    while not used except by people who don’t know any better (or don’t
    need to worry about execution time or accuracy), is an excellent
    method to study.  Why?  It is as simple as one can get.  Every time
    stepping method is a descendant of Euler’s method.  
        
     This resource should take approximately 3 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Euler’s Method”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Euler’s
    Method](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 4
    lectures that have been split into 4 videos.  
        
     This resource should take approximately 1/2 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**5.3.1 Taylor Methods** <span id="5.3.1"></span> 
**5.3.1.1 Euler’s Method** <span id="5.3.1.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “The IVP and
    Euler’s Method”**
    Link: University of Arkansas: Mark Arnold’s “[The IVP and Euler’s
    Method](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Finally read the remainder of
    the pdf.  Pay careful attention to the error bound.  Unfortunately,
    the error in Euler’s method could grow exponentially in time (notice
    the e^{t\_i-a} term in the formula).  In addition, when we include
    rounding errors, we see that this problem cannot be completely
    solved by making h small.  Find an optimal h for a given IVP
    assuming you know a Lipschitz constant L and an upper bound M for
    |f’’| on [a,b].  While I hope you are successful, note that we
    typically do not know L or M… A rule of thumb for Euler’s method is
    we should not take h smaller than sqrt{(machine epsilon)}, but
    taking h that small will typically require a very many time steps.  
        
     This resource should take approximately 1.5 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**5.3.1.2 Local Truncation Error** <span id="5.3.1.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Single Step
    Methods and Local Truncation Error”**
    Link: University of Arkansas: Mark Arnold’s “[Single Step Methods
    and Local Truncation
    Error](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pfd.  A
    natural approach to addressing the drawbacks of Euler’s method would
    be to construct a more accurate alternative.  We will measure
    accuracy here by local truncation error.  Find the local truncation
    error for Euler’s method.  Our first higher order method is the
    Taylor method of order 2.  The Taylor method of order n is not any
    more difficult to understand.  Explain why the Taylor methods of
    order n \> 1 are not general purpose.  As an exercise, please find a
    formula for d^3/dt^3 f(t,y) in terms of partial derivatives of f.  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.  
      

**5.3.2 Runge-Kutta Methods** <span id="5.3.2"></span> 
**5.3.2.1 Runge-Kutta Methods of Order 2** <span id="5.3.2.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Runge-Kutta
    Methods Order 2”**
    Link: Reading: University of Arkansas: Mark Arnold’s “[Runge-Kutta
    Methods Order 2](http://www.uark.edu/~arnold/4363/pages.html)”
    (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  So
    the Runge-Kutta (RK) methods that give us higher order methods
    without the need for derivatives of f.  This makes these methods
    tremendously important.  How would you describe the RK method with
    respect to the average derivative of f over the interval [t\_i,
    t\_i + h]?  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Runge-Kutta 2nd Order Method”**
    Link: YouTube: University of South Florida: Autar Kaw’s
    “[Runge-Kutta 2<sup>nd</sup> Order
    Method](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 6
    lectures that have been split into 8 videos.  
        
     This resource should take approximately 1 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**5.3.2.2 Higher Order Runge-Kutta Methods** <span id="5.3.2.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Runge-Kutta
    Methods”**
    Link: University of Arkansas: Mark Arnold’s “[Runge-Kutta
    Methods](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  Here
    we describe the RK methods as sampling f in the interval [t\_i,
    t\_i + h] in order to approximate the average value of y’ over that
    interval.  This subject is too rich to explore very deeply in this
    course, but notice that as the local truncation error becomes higher
    order, the number of function evaluations increases greater than
    linearly.  
        
     This resource should take approximately 1.5 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s “Runge
    Kutta 4th Order Methods”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Runge
    Kutta 4<sup>th</sup> Order
    Methods](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 2
    lectures that have been split into 3 videos.  
        
     This resource should take approximately 1/2 hour to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**5.3.2.3 Adaptive Runge-Kutta Methods** <span id="5.3.2.3"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Adaptive
    Runge-Kutta Methods”**
    Link: University of Arkansas: Mark Arnold’s “[Adaptive Runge-Kutta
    Methods](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  We
    saw with the adaptive quadrature method that an error estimate
    provided the opportunity to adapt.  In the quadrature method, the
    adaptation was the subdivision of an interval of integration; here
    the adaptation will be our step size, h.  The idea is very general,
    and this is an active area of research.  We estimate y(t+h) using
    two different methods, and a truncation error analysis provides a
    new suggested step size.  This reading provided the details for a
    famous method that combines a RK method of order 4 and one of order
    5.  You do the analysis for two methods of order 2 and 3.  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**5.4 Multi-Step Methods** <span id="5.4"></span> 
**5.4.1 Adams-Bashforth Methods** <span id="5.4.1"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Multi-step
    Methods”**
    Link: University of Arkansas: Mark Arnold’s “[Multi-step
    Methods](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the first 3
    paragraphs of the pdf.  The multistep methods have a memory.  This
    is what can give them high order lte with fewer function
    evaluations.  But for the first m-1 steps, the history is
    incomplete.  In this sense, the RK methods are prior to, or more
    fundamental that the multistep methods.  The notation here may be
    confusing, so compute a few steps of the explicit method of order 2
    (Adams-Bashforth 2-step) for the IVP y’(t)=t+2y,  y(0)=2, using
    h=0.1.  What order RK method should be used to generate w\_1?  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**5.4.2 Adams-Moulton Methods** <span id="5.4.2"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Multi-step
    Methods”**
    Link: University of Arkansas: Mark Arnold’s “[Multi-step
    Methods](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Read the remainder of the pdf
    carefully.  The implicit multistep methods are not explicitly solved
    for w\_{i+1} (it appears on both sides of the equation and as an
    argument to f).  This is part of the reason we investigated solving
    equations early in this course.  We could use a few iterations of
    the Newton or secant method to approximate w\_{i+1} (possibly using
    w\_i as an initial guess).  Conceptually this is not a problem, but
    it requires costly function evaluations.  Compute a few steps of the
    implicit method of order 2 (Adams-Moulton 2-step) for the IVP
    y’(t)=t+2y,  y(0)=2, using h=0.1.  Use 2 secant iterations to
    compute w\_2, using w\_1 and your w\_2 from the previous unit.  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**5.4.3 Predictor Corrector Methods** <span id="5.4.3"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Adaptive
    Multi-step Methods”**
    Link: University of Arkansas: Mark Arnold’s “[Adaptive Multi-step
    Methods](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. Carefully read the pdf.  In
    the last unit we met a fundamental difficulty associated with
    implicit methods: the need to solve an equation at each time step. 
    We will see later that implicit methods are so important that we
    should not dismiss them simply because of this complication.  One
    rather elegant approach is to use an explicit method to predict
    w\_{i+1}, and then to correct the prediction by substituting 
    w\_{i+1} in the right hand side by that prediction.  Naturally
    enough, this is called a predictor-corrector method, and since we
    are using two distinct methods to arrive at w\_{i+1}, we can
    implement a step size correction if we like.  Compute a few steps of
    a predictor-corrector method using an Adams-Bashforth 2-step and an
    Adams-Moulton 2-step  for the IVP y’(t)=t+2y,  y(0)=2, using (a
    constant) h=0.1.  Discuss the difficulties of changing step size for
    a multistep method.  
        
     This resource should take approximately 2 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**5.5 Stiff Problems** <span id="5.5"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Stiff Problems”**
    Link: University of Arkansas: Mark Arnold’s “[Stiff
    Problems](http://www.uark.edu/~arnold/4363/pages.html)” (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. We have seen that adaptive
    step sizes can lead to much greater efficiencies than uniform
    steps.  Stiff differential equations can easily fool some methods,
    forcing them to take small step sizes when there is little or no
    variation in the solution.  
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**5.6 Stability of Methods** <span id="5.6"></span> 
-   **Reading: Scholarpedia: John Butcher’s “Stability”**
    Link: Scholarpedia: John Butcher’s
    “[Stability](http://www.scholarpedia.org/article/Runge-Kutta_Methods%23Stability)”
    (HTML)  
      
     Instructions: Click on the link above and read the article.  All
    things being equal, we would like to use stable methods; but of
    course, we would also like to use the fastest most general methods. 
    Regions of stability give us a necessary condition for bounding a
    time step.  Methods with large stability regions are especially
    important in the case of stiff systems.  Methods with large
    stability regions are usually implicit methods.  
        
     This resource should take approximately 1 hour to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**5.7 Shooting Methods for Boundary Value Problems** <span
id="5.7"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s “Shooting
    Methods”**
    Link: University of Arkansas: Mark Arnold’s “[<span
    class="Hyperlink3">Shooting
    Methods</span>](http://www.uark.edu/~arnold/4363/pages.html)”
    (PDF)  
      
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading. 

    This resource should take approximately 1 hour to complete. 

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s
    “Shooting Method” (YouTube)**
    Link: University of South Florida: Autar Kaw’s “[Shooting
    Method](http://numericalmethods.eng.usf.edu/videos/)” (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 3
    lectures that have been split into 6 videos.  
        
     This resource should take approximately 50 minutes to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

-   **Lecture: YouTube: University of South Florida: Autar Kaw’s “Finite
    Difference Method”**
    Link: YouTube: University of South Florida: Autar Kaw’s “[Finite
    Difference Method](http://numericalmethods.eng.usf.edu/videos/)”
    (YouTube)  
        
     Instructions: Click on the link above, then watch the video
    lectures in the chapter listed above.  In this case there are 3
    lectures that have been split into 6 videos.  
        
     This resource should take approximately 50 minutes to complete.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpages above.

**5.8 Programming Case Study: A Predictor Corrector Implementation**
<span id="5.8"></span> 
-   **Reading: University of Arkansas: Mark Arnold’s
    “Predictor-Corrector Program”**
    Link: University of Arkansas: Mark Arnold’s [“Predictor-Corrector
    Program”](http://www.uark.edu/~arnold/4363/Octave/PredictorCorrector.pdf)
    (PDF)  
        
     Instructions: Click on the link above, then select the appropriate
    link to download a pdf of the reading.  
        
     This resource should take approximately 4 hours to complete.  
        
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**Unit 5 Assessment** <span id="5.9"></span> 
-   **Assessment: The Saylor Foundation's "Unit 5 Assessment"**
    Link: The Saylor Foundation's "[Unit 5
    Assessment](https://resources.saylor.org/wwwresources/archived/site/wp-content/uploads/2012/08/MA213-Unit-5-Assessment-FINAL.pdf)"
    (PDF) and “[Guide to
    Responding](https://resources.saylor.org/wwwresources/archived/site/wp-content/uploads/2012/08/MA213-Assessment-Unit-5-GTR-FINAL.pdf)”
    (PDF).  
      
     Instructions: Carefully answer the four questions below.  The first
    three are entirely computational, and while it may be tedious, it
    will be good for you to do them by hand.  If you keep 7 or more
    significant (decimal) digits throughout your computations, then your
    results should match the answers given in the guide.  Most mistakes
    arise from using the wrong value for the time parameter t.  Question
    4 also has an essay question asking you to reflect on the results of
    your experiment; you can then compare your conclusions with the
    guide.  Now that you have done this by hand at least once, please
    feel free to construct other similar experiments which you can
    implement with your programs.


