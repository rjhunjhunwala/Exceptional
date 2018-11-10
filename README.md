# Exceptional

This project strives to build a programming language (and software derived from it) which is truly exceptional, by ensuring an "Exception" is the only form of conditional control structure!
## Specifications

The language is a statically typed, strongly enforced, can be formally specified as follows. The reference implementation, is a transpiler, written in Python, which transpiles Exceptional code into Java. 

The bigger the tech-stack, the more exceptional the code. Using Exceptional allows you to interact with three languages at once (four, if you count JVM byte-code)
 
<hr/>

The language consists of a number of statements. Each one has a certain effect. A statement must reside on it's own line, but may be proceeded by any amount of whitespace.

<pre>
GIVE_IT_110_PERCENT!
</pre>
The first kind of statement, and arguably the most important one. We want all of our code to be written with110 percent effort, so we encourage the programmer to specify this. Any code that precedes this statement, will run, but only with a 9/10 chance (90%).

<pre>
PROCEDURE [NAME]
</pre>

This declaration, starts a procedure, and binds it to NAME in the global frame. Note names within a frame, can not be re-bound.

Identifiers may be any combination of alphabetical characters and underscores

<pre>
END
</pre>

This defines the ends of the procedure, or the end of a block. Think of it as a "}"

<pre>TRY!
</pre>

This marks the start of a TRY-FAIL block, but it gives more feelings and emotion to our code. it must be ended with an END, and fail block

<pre>
FAIL:(
</pre>
This marks the fail portion of the block essentially, it transpiles to 
<pre>}catch(Throwable t){</pre>
Be sure to end it with an END

<pre>
CALL NAME
</pre>

Calls the procedure, named "name"

<pre>
DEFINE [TYPE] [NAME]
</pre>

Creates a variable called name (in the global or local context, depending), and initializes it.
Valid types are STACK, BUFFER (array), and INTEGER. 
STACK(S), are initialized to be empty. BUFFER(S) have a default length of 65535, and INTEGER(S) have a default value of 0

<pre>
REASSIGN NAME [EXPRESSION]
</pre>
Makes an integer named "NAME" have the value of EXPRESSION. Expressions can contain integer literals, other INTEGER names, and operators (+-*/)

<pre>GET [BUFFER] [LOCATION] [NAME]</pre>
makes the integer named name, be the value of the buffer indexed to location

<pre>SET [BUFFER] [LOCATION] [NAME]</pre>
Makes the value in the buffer at the given location be the value of name, (or name itself if it is a literal).

<pre>POP [STACK] [NAME]</pre>
Reassigns the value in name to be the value popped of the stack called [STACK]

<pre>PUSH [STACK] [NAME]</pre>
Pushes the value of name, to the stack called [STACK]

<pre>print WHATEVER</pre>

prints whatever object whatever happens to be at run time, you must specify a line feed yourself...



