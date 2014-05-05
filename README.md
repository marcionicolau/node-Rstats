node-Rstats
===========

An interface for node.js to statistical programming language R based on the fabulous Rcpp package

## Installation

## Getting Started

Once the package is loaded, we can create an R session by the command 

```javascript
var R  = new Rstats.session(); 
```

Evaluating R expressions is easy. If we do not expect a return object, we can use the *parseEvalQ* function as follows:

```javascript
R.parseEvalQ("cat('\n Hello World \n')");
```

## Important Functions

### assign

Numeric values can be easily assigned to variables in the current R session:

```javascript
R.assign('x', 17)
R.assign('y',3)

// calculate the sum of x+y
R.parseEvalQ("res = x + y; print(res);")
```

### parseEvalQ

### parseEval