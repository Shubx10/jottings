> ## Overview
Arithmetic expressions can be written in `3 different notations` - `infix`, `prefix`, and `postfix`. In the Prefix notation, the operator is written before the operand in an expression. On the other hand, in the Postfix notation, the operator is written after the operand. The expressions are evaluated using stack.

> ## Introduction
An expression that only contains arithmetic operands and operators is called an arithmetic expression. The results of these expressions are always in numeric values. Arithmetic expressions are usually represented in something known as the `Infix Notation`. In this notation, the operator is between two operands `Example: X + Y where X and Y are arithmetic operands`. We can even use parentheses in arithmetic expressions.
Any arithmetic expression is written in the infix notation is evaluated by following operator precedence rules. However, if we want to evaluate an expression without considering operator precedence, we can use `Polish (or Prefix) notations` or `Reverse Polish (or Postfix)` notations.

> ## Polish (prefix) Notation
In the `Polish or Prefix notation`, the operator is written before the operand in an expression. This notation does not need parenthesis because the expression's evaluation is done in a stack. So, we do not need to specify the execution order to evaluate arithmetic expressions. `The compiler can process the prefix notation faster than the infix notation because it does not need to process any parentheses or follow precedence rules`. An expression in the Polish notation looks like this:
```
*XY
```
The above expression is equivalent to X * Y in the infix notation where X and Y are two arithmetic operands and * is the operator.

> ## Reverse Polish (postfix) Notation
In the `Reverse Polish or Postfix notation`, the operator is written after the operand in the expression. There is no need for parenthesis in this notation because the expression's order of execution is already defined in the stack. An expression in postfix notation looks like this:
```
XY+
```
The above expression is equivalent to X + Y, where X and Y are two arithmetic operands, and + is the operator.

> ## Summary
 - Arithmetic expressions can be written in 3 different notations - infix, prefix, and postfix.
 - In the Prefix notation, the operator is written before the operand in an expression. On the other hand, in the Postfix notation, the operator is written after the operand.
 - Prefix and Postfix notations are faster than infix notations.
 - We can convert infix notations to prefix or postfix notations and vice-versa.

