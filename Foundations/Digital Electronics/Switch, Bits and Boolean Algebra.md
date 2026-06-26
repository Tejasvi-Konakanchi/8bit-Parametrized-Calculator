# Switch, Bits and Boolean Algebra
Digital Electronics handle data in bits (0 or 1).

## Switch
A switch is one of the easiest ways to represent a bit.

| Switch State | Binary Bit | Meaning    |
| ------------ | ---------- | ---------- |
| OFF          | 0          | Low, False |
| ON           | 1          | High, True |

Since Switch has two states they naturally represent a boolean variable (true or false). You can use multiple switches to represent different levels (using Truth Tables) as shown below

| Switch A | Switch B | Boolean Expression | Output | Notes |
| -------- | -------- | ------------------ | ------ | ----- |
| OFF (0)  | OFF (0)  | A AND B            | 0      |position 1|
| OFF (0)  | ON (1)   | A AND B            | 0      |position 2|
| ON (1)   | OFF (0)  | A AND B            | 0      |position 3|
| ON (1)   | ON (1)   | A AND B            | 1      |position 4|

## Truth Tables
- no.of rows = 2^(no.of variables/switches).
- Allocate T/F or 0/1, with the pattern (4 0s/1s, 2 0s 1s, 1 0s 1s).

## Boolean Algebra
- It is the set of rules, used to simplify the given logic expression without changing its functionality.
- It is used when number of variables is (3-4). It gets tedious otherwise, so we use Kmap method.

<b> What is a logic expression? </b>
<br>
A logic expression is a mathematical way of describing a digital circuit. It tells you how the output depends on one or more inputs.

Y = A . b, is a logic expresion, describing the output Y. Y will be 1, if A and b are both 1. This is explained in the expression
</br>

<b> Rules: </b>
<br>
1. Compliments: A = 0, A' = 1, (A')' = 0
2. AND( Y = A . B): 
- A = A . A; 
- 0 . 0 = 0; 
- 1 . 1 = 1; 
- A . 0 = 0;
- A . 1 = A;
- A . A' = 0;

3. OR( Y = A + B): 
- 0 + 0 = 0
- 1 + 0 = 1
- A + 0 =  depends on A. (0 or 1)
- A + 1 = 1
- A + A' = 1

4. Distributive Law
- A . (B + C ) = A . B + A . C
- A + (B + C) = (A + B) . (A + C)
- A + A'B = (A + A') . (A + B) = A + B

5. Commutative Law
- A + B = B + A
- A . B = B . A

6. Associative Law
- (A . B) C = A . (B . C)

7. Priority
- NOT > AND > OR

8. De-Morgan's Law
- (A + B)' = A' . B'
- (A . B)' = A' + B'

</br>

