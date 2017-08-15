# numlab
From MATLAB to Scilab, from GNU Octave to Julia Lang, a numeric computing toolkit is useful for scientists, engineers and programmers. But I observed some inconsistence between different domains. Engineers and programmers are familiar with programming language with 0-based index while scientists and mathmaticians are used to 1-based index in MATLAB and Julia Lang. 2^3 is equal to 8 for mathmaticians but "^" is exclusive-OR operatior for C-like languages. Well, we need a comppromised solution.

**Swift** has been aggresively developed in the past few years. I believe it will be one of the most popular programming language in the world. So, why don't we design a numerical toolkit by extending Swift? Some guys have developed useful Swift packages such as swix, Surge, Upsurge, numsw, NumSwift...  Here I would like to take the advantage of them but redesign to get a better compromised toolkit.

# Data Type
First of all, let's overload the **^** operator. ^ is rarely used in numerical analysis. It will be the *power* operator now. Then define a new type **Complex** for complex number. The operation of Swift Array type is different from what we expect in math, so define a new type **Vector**. Finally, define a new type **Matrix** for matrix operation.

Now, I hope to achieve
````
let x = 2^3    // x = 8

let c = Complex(3, 4)  // c = 3 + 4i
let d = abs(c)   // d = 5 + 0i

let a: Vector = [1, 3, 5, 7]
let b: Vector = [2, 4, 6, 8]
let v1 = a + b    // v1 = [3.0, 7.0, 11.0, 15.0]
let v2 = a * b    // v2 = [2.0, 12.0, 30.0, 56.0]
let v3 = a • b    // v3 = 100

let A = Matrix([
      [1, 2],
      [3, 4]
    ])
let B = Matrix([
      [5, 6],
      [7, 8]
    ])
let C = A * B     // C = [[19, 22], [43, 50]]
````

#Plot

Plot is important ot observe the analyized data.

#DSP Toolkit

#Other Toolkit
