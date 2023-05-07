Download Link: https://assignmentchef.com/product/solved-machinelearning-homework-1
<br>
1 Problem 1

Cross-validation for Polynomial Fitting: Consider the problem of fitting a polynomial function, Assume we wish to find a one dimensional function that takes a scalar input and outputs a scalar <strong><em>f </em></strong><strong>R </strong>R. The function has the form

<strong><em>Az.: 0)                  + 9<sub>1</sub> r + 9<sub>2</sub> + — + Odr<sup>d</sup></em></strong>

<strong><em>where d </em></strong>is the degree of the polynomial_ Develop code that. finds the <strong><em>0 </em></strong>which minimizes the risk <strong><em>fr 71,0)                       </em></strong><strong><em>1v–, 1</em></strong>

=l

on a data-set. To help you get started. download the Matlab code in “polyreg.m’ (on the tutorial web page) to do polynomial curve fitting. Use your code on the dataset “probleml.mat”. This should include a matrix x, corresponding to the scalar features {x<sub>i</sub>, …. <em>xN}, </em>and a matrix <strong><em>y, </em></strong>corresponding to the scalar labels { y<sub>i</sub>, yN}. Fit a polynomial model to this data for various choices for <strong><em>d, </em></strong>the degree of the polynomial.

Which value(s) of d seems somewhat more reasonable? Please justify your answer using some empirical measure.

It is easy to overfit the data when using polynomial regression. As a result, use cross-validation by randomly splitting the data-set into two halves to select the complexity of the model (in this case, the degree of the polynomial). Include a plot showing the training and testing risk across various choices of d, and plot your <strong><em>f (,r; 0) </em></strong>overlaid on the data for the best choice of d according to cross-validation .




<strong>2 Problem 2</strong>

Regularized risk minimization: Modify the Matlab code for “polyreg.m” such that it learns a multi­variate regression function <em>f : R’°° —&gt; </em>R, where the basis functions are of the form

<em>k</em>

<em>f (x; 0) </em><em>= </em>E o<sub>i</sub>x<sub>i</sub>

i=1

The data-set is available in “problem2.mat”. As before, the <em>x </em>variable contains {x<sub>1</sub>, … , <em>xN} </em>and the y variable contains their scalar labels {y<sub>1</sub>, … , y<sub>N</sub>}.

Use an /<sub>2</sub> loss function to penalize the complexity of the model, e.g. minimize the risk

<table>

 <tbody>

  <tr>

   <td width="223">R<sub>reg</sub> (0) =</td>

   <td width="353"><em>1 N</em>1                                                 <u>A </u><em><sub> N</sub></em> E  2 (y<sub>i</sub> — <em>f(x; </em>OW + <em><sub>2N</sub></em>MeVi=1</td>

  </tr>

 </tbody>

</table>




Use two-fold cross validation (as in Problem 1) to find the best value for A. Include a plot showing training and testing risk across various choices of A. A reasonable range for this data set would be from A = 0 to A = 1000. Also, mark the A which minimizes the testing error on the data set.

What do you notice about the training and testing error?

<strong>3 Problem 3 </strong>

Logistic Squashing Function. The logistic squashing function is given by <em>g(z) = 1 / (1 + </em>exp(—z)). Show that it satisfies the property <em>g(—z) = 1 — g(z). </em>Also show that its inverse is given by g<sup>-1</sup>(y) = ln(y/(1 — y).

<strong>4 Problem 4 </strong>

Logistic Regression: Implement a linear logistic regression algorithm for binary classification in Matlab using gradient descent. Your code should accept a dataset {(x<sub>i</sub>, y<sub>i</sub>), … , (x<sub>N</sub>, y<sub>N</sub>)} where x<sub>i</sub> E Rd and y<sub>i</sub> E {0,1} and find a parameter vector <em>0 </em>E R<sup>d</sup> for the classification function

<em>f (x; 0) = </em>(1 + exp(-9<sup>T</sup>x)) <sup>1</sup>

which minimizes the empirical risk with logistic loss

<em>N</em>

<em>1</em>

<em>R<sub>em</sub>p(e) = </em><em>N </em>V (y<sub>i</sub> — 1) log(1 — <em>f (x<sub>i</sub>; 0)) — </em>y<sub>i</sub> log( <em>f (x<sub>i</sub>; 0)).</em>

<em>L—<sup>,</sup></em>i=1

Since you are using gradient descent, you will have to specify the step size <em>71 </em>and the tolerance e. Pick reasonable values for <em>71 </em>and e to then use your code to learn a classification function for the dataset in “dataset4.mat”. Type “load dataset4” and you will have the variables <em>X </em>(input vectors) and Y (binary labels) in your Matlab environment which contain the dataset.

Show any derivations you need to make for this algorithm.




Use the whole data set as training. Show with figures the resulting linear decision boundary on the 2D <em>X </em>data. Show the binary classification error and the empirical risk you obtained throughout the run from random initialization until convergence. Note the number of iterations needed for your choice of ri and e.