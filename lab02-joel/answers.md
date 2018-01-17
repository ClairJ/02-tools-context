- When this code is run in Node, e.g. node index.js, what are the two stages of execution for this file called, and which order do they happen in?

  -The two stages of execution are compilation and execution

-Write an explanation, using as much space as you need, relating to how the first stage of execution for this file operates.

  -Node compiles javascript into pieces of instructions to be readable by our machines.

  -First is declaring variable foo in the global scope.

  -Next is the local scope of the bar function.

  -Variable foo is defined in the local scope of the bar function

  -Now entering the scope of the baz function passing in the local variable foo, foo is redefined as 'bam'

-Write an explanation, using as much space as you need, relating to how the second stage of execution for this file operates.

  -The execution phase where all the variables and functions are called.

  -Upon execution of bar foo goes from being defined as 'bar to 'baz to 'bam'

  -foo is executed still being defined as 'bam', the bam variable will throw an error for being undefined.

-During the second stage of execution how many scopes have been registered by the engine?

  -3 scopes, the global scope and the 2 scopes of functions.

-When line 13 invokes the baz function, which foo will be assigned a value of bam? More specifically, bam will be assigned to the foo in ??? scope. Give a brief description in your own words to support your conclusion.

  -foo is assigned the value 'bam' in the 3rd scope, the scope of the baz function where foo is passed through and reasigned to 'bam'.

-Which scope, if any, will the variable bam on line 11 be registered to when the first stage of execution occurs on this file? Provide a brief description in your own words to support your conclusion.

  -because of use strict the bam variable will remain undefined and throw an error. If use strict was not in place then bam would be defined in the baz scope and executed on line 18 because bar is called which bam is defined.

-For each line, 16 through 19, what is the return value for each?

  -bar() = undefined
  -foo = bam
  -bam =  undefined error
  -baz = scope error
