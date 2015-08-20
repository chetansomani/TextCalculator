/* CONSTRAINTS:
 * Each input will be in the form of <alphabet> = <number>/<alphabet>/<series of numbers with alphabets and operators>.
 * Each alphabet is an ASCII characters or it can be string of characters.
 * Each number is an integer type i.e. INT32. Hence the range doesnot extend the integer type range.
 * the arithmetic operators used are +,-,*,/,^.
 * Use of increment and decrement operators as well.
 * All the inputs will be in series and the output contains the final values of all the string of characters values.
 */

/* Idea:
 * Use of Hash to store the stringofcharacters as keys and the values being computed as value. This will make sure the memory occupied will
 * be as per the number of unique keys. THe hashfunction will be the default hash function used by c#.
 * The use of infix and postfix for computing the arithmetic calculations as we need to keep the order of preferences for each arithmetic operator.
 * In order to compute infix and postfix, we will use stack data struture.
 * Once, the computation is done, we will store the final computed value for that key in the hash. If the value already exists, we will update it or add it.
 */

/* Complexities: 
 * Space Complexity: O(k) if they are k keys for hash to be stored if K is a number, the space complexity will be O(1).
 * Time Complexity: O(K*n) if they are K inputs, since K is a number. Overall Complexity - O(n).
 */

/* FOLLOWING ARE THE TEST CASES
 * NOT A VALID INPUT:
 * 9
 * 9 = 0
 * = * ()
 * = 9 0
 * = 9 I
 * ++ i j
 * ++i
 * i = j //if it is the first statament with out j being initialized
 * 9 = i j * k
 * i = j + k //if it the first statement with out j and k being initialized
 * 
 * VALID INPUT:
 * i = 0
 * j = 10
 * k = i + j
 * 
 * j = 10
 * i = j * 100 + 20 * 30 + 40
 * 
 * k = 0
 * i = 20
 * j = 120
 */