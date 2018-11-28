Course Syllabus for "MA213: Numerical Analysis"
-----------------------------------------------

**Please note: this [legacy course](https://sayloracademy.zendesk.com/hc/en-us/articles/206089967) does not offer a certificate and may contain 
broken links and outdated information.** Although archived, it is open 
for learning without registration or enrollment. Please consider contributing 
updates to [this course on GitHub](https://github.com/saylordotorg/course_ma213) 
(you can also adopt, adapt, and distribute this course under the terms of 
the [Creative Commons Attribution 3.0 license](http://creativecommons.org/licenses/by/3.0/)). **To find fully-supported, current courses, [visit our 
Learn site](https://learn.saylor.org).**

Numerical analysis is the study of the methods used to solve problems
involving continuous variables.  It is a highly applied branch of
mathematics and computer science, wherein abstract ideas and theories
become the quantities describing things we can actually touch and see. 
The real number line is an abstraction where many interesting and useful
ideas live, but to actually realize these ideas, we are forced to employ
approximations of the real numbers.  For example, consider marking a
ruler at \\sqrt{2}.  We know that \\sqrt{2} \\approx 1.4142, but if we
put the mark there, we know we are in error for there is an infinite
sequence of nonzero digits following the 2.  Even more: a number doesn’t
have any width, yet any mark we make would have a width, and in that
width lives an infinite number of real numbers.  You may ask yourself:
isn’t it sufficient to represent \\sqrt{2} with 1.414?  This is the kind
of question that this course will explore.  We have been trying to
answer such questions for over 2,000 years (it is said that people have
given their lives for the idea of \\sqrt{2}, and they certainly wouldn’t
think 1.414 sufficient).  Modern computers can perform billions of
arithmetic operations per second and trying to predict the path of a
tropical storm can require many trillions of operations.  How do we
carry out such simulations and how do our approximations affect the
result?  The answer to the first question is certainly colored by the
second! Numerical analysis is a broad and growing discipline with many
open questions.  This course is designed to be a first look at the
discipline.  Over the course of this semester, we will survey some of
the basic problems and methods needed to simulate the solutions of
ordinary differential equations.  We will build the methods ourselves,
starting with computer arithmetic, so that you will understand all of
the pieces and how they fit together in state of the art algorithms. 
Along the way, we will write programs to solve equations, plot curves,
integrate functions, and solve initial value problems.  At the end of
some chapters we will suggest - in a section called “Of Things Not
Covered” - some topics that would have been included if we had more time
or other avenues to explore if you are interested in the topics
presented in the unit. The prerequisites for taking this course are
[MA211: Linear Algebra](http://www.saylor.org/courses/ma211/), [MA221:
Differential Equations](http://www.saylor.org/courses/ma221/), and
either [MA302/CS101: Introduction to Computer
Science](http://www.saylor.org/courses/ma302/) or a background in some
programming language.  Programming ideas will be illustrated in
pseudocode and implemented in the open-source high-level computing
environment.
<span style="font-family: &amp;quot;">Numerical Analysis is the field of
mathematics that applies numerical approximations in order to solve
mathematical problems of continuous variables.In most cases, numerical
analysis does not have the goal of finding exact answers to complex
problems, as most mathematical problems cannot be solved through the
application of a finite number of elementary mathematical
operations.Rather, numerical analysis focuses on the development and
study of algorithms that will quickly obtain approximate solutions.By
analyzing these algorithms, we can evaluate their errors and stability
and in turn decide when it is safe to use a particular numerical
algorithm.</span>

The first known application of the methods of numerical analysis appears
on Babylonian tablet YBC 7289, which is roughly dated between 1700-2000
BC.(Evidence suggests that the writer was a mathematics student.)The
tablet features an incised square whose sides have a length of 0.5 units
and a diagonal line that connects opposite corners of the square.The
diagonal line is labeled 0:42 25 35 (in sexagesimal notation), which
tells us that the Babylonians thought that the square root of 2 is
1.41421296 (in decimal notation).(The actual square root of 2 is
1.41421356… to 9 decimal places.)The Babylonian value is in error by
roughly 7 parts in 100,000—an accuracy that could not have been obtained
by direct measurement.As the square root of 2 is an irrational number,
it cannot be directly calculated.Although not known for sure, it is
likely that the value for the square root of two was originally
calculated by Heron’s method, a simple version of the Newton-Raphson
method for finding successively better approximations to the roots of a
function.

This course will focus on the applications of the methods of numerical
analysis.We will cover enough of the mathematical background to allow
you to intelligently discuss the convergence, error, and stability
properties of numerical analysis algorithms, but will place emphasis on
solving certain classes of problems that often arise in scientific or
engineering contexts.These include approximating functions, finding
roots of polynomial and other nonlinear functions, solving systems of
linear equations, finding eigenvalues and eigenfunctions, optimizing
constrained multi-dimensional functions, evaluating integrals, and
solving ordinary and partial differential equations.

<span style="font-size: 12pt; font-family: &amp;quot;">The prerequisites
for taking MA213 are MA211 (Linear Algebra), MA221 (Differential
Equations), and either MA302/CS101 (Introduction to Computer Science) or
a solid background in JAVA programming.While not necessary, treating
MA222 (Partial Differential Equations) as a co-requisite is advised.Many
problems and methods will be presented and used within an open-source
Java-based computing environment. </span>

### Learning Outcomes

 Upon successful completion of this course, the student will be able
to:  

-   Show how numbers are represented on the computer, and how errors
    from this representation affect arithmetic. 
-   Analyze errors and have an understanding of error estimation. 
-   Be able to use polynomials in several ways to approximate both
    functions and data, and to match the type of polynomial
    approximation to a given type of problem. 
-   Be able to solve equations in one unknown real variable using
    iterative methods and to understand how long these methods take to
    converge to a solution. 
-   Derive formulas to approximate the derivative of a function at a
    point, and formulas to compute the definite integral of a function
    of one or more variables. 
-   Choose and apply any of several modern methods for solving systems
    of initial value problems based on properties of the problem.

### Course Requirements

In order to take this course you must:  
    
 √    Have access to a computer.  
    
 √    Have continuous broadband Internet access.  
    
 √    Have the ability/permission to install plug-ins or software (e.g.,
Adobe Reader or Flash).  
    
 √    Have the ability to download and save files and documents to a
computer.  
    
 √    Have the ability to open Microsoft files and documents (.doc,
.ppt, .xls, etc.).  
    
 √    Be competent in the English language.  
        
 √    Have read the [Saylor Student
Handbook.](https://resources.saylor.org/wwwresources/archived/site/wp-content/uploads/2012/05/Saylor-StudentHandbook.pdf)

### Course Information

Welcome to MA213 Numerical Analysis.  Below, please find general
information on this course and its requirements.  
  
 **Course Designers:** [Professor
Baccouch](http://www.saylor.org/faculty-a-g/#ProfessorBaccouch)  
    
 **Primary Resources:** This course primarily relies on content from the
following resources:  
 •       University of Arkansas: Mark Arnold’s “Numerical Analysis
Pages”  
 •       University of Southern Florida: Autar Kaw’s “Numerical Methods
Lectures”  
    
 **Requirements for Completion:** Viewing videos, reading and working
through pages and exercises, and writing 5 programs in Octave.  
    
 **Time Commitment:** This course should take about 129 hours to
complete.  
    
**Table of Contents:** You can find the course's units at the links below.

- [Unit 1](https://legacy.saylor.org/ma213/Unit01/)
- [Unit 2](https://legacy.saylor.org/ma213/Unit02/)
- [Unit 3](https://legacy.saylor.org/ma213/Unit03/)
- [Unit 4](https://legacy.saylor.org/ma213/Unit04/)
- [Unit 5](https://legacy.saylor.org/ma213/Unit05/)
- [Unit 6](https://legacy.saylor.org/ma213/Unit06/)
- [Final Exam](http://saylordotorg.github.io/LegacyExams/MA/MA213/MA213-FinalExam.html), [Answers](http://saylordotorg.github.io/LegacyExams/MA/MA213/MA213-FinalExam-Answers.html)
