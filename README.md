# Forged-Workshop-2

### Basic Requirements

#### Comparison Operators

1. Type the two boolean values -- `true` and `false` -- into your console.

2. Use the console to accomplish the following:

    + Write an expression using `>` that will evaluate to `false`
    + Write an expression using `>` that will evaluate to `true`
    + Write an expression using `<` that will evaluate to `false`
    + Write an expression using `<` that will evaluate to `true`
    + Write an expression using two numbers and `===` that will evaluate to `true`
    + Write an expression using two numbers and `===` that will evaluate to `false`
    + Write an expression using two strings and `===` that will evaluate to `true`
    + Write an expression using two strings and `===` that will evaluate to `false`

3. Fill in the `???` with the following operators or values to make the statements
   output the expected Boolean value.

   ```js
   12 ??? 78
   // => true

   24 ??? 16
   // => false

   45 !== ???
   // => true

   "45" ??? 45
   // => false

   "6" ??? "six"
   // => true
   ```

4. Write a function `oldEnoughToDrink` that takes an `age` as an argument and
   returns `true` if the person with that age is old enough to drink.

5. There's an easy way to figure out how long a string is by adding `.length` to
   the end of it. Try this out in the console:

  ```js
  "hello".length;
  "".length;
  "John Doe".length;
  ```

  Write a function `sameLength` that accepts two strings as arguments, and
  returns `true` if those strings have the same length, and `false` otherwise.

6. Write a function `passwordLongEnough` that accepts a "password" as a
   parameter and returns `true` if that password is *long enough* -- you get to
   decide what constitutes *long enough*.

#### Conditionals: `if`

1. Write a function `bouncer` that accepts a person's name and age as arguments,
   and returns either "Go home, NAME.", or "Welcome, NAME!" (where NAME is the
   parameter that represents the person's name) depending on whether or not the
   person is old enough to drink.

2. Write a function `max` that takes two numbers as arguments, and returns the
   larger one.

3. Write a function `min` that takes two numbers as arguments, and returns the
   smaller one.

4. Write functions `larger` and `smaller` that each accept two strings as
   arguments, and return the *larger* and *smaller* strings, respectively.

### More Practice

1. Fill in the `???` with the following operators or values to make the statements
   output the expected Boolean value.

   ```js
   106 ??? 12
   // => false

   "wiz" ??? "wiz"
   // => true

   7 * 7  ??? 49
   // => true

   12 ??? (24 / 2)
   // => false

   (20 % 2) <= ???
   // => true

   (9 / 3) + (5 * 5) === ???
   // => true
   ```

2. Write the following functions that each accept a single number as an
   argument:

    + `even`: returns `true` if its argument is even, and `false` otherwise.
    + `odd`: the opposite of the above.
    + `positive`: returns `true` if its argument is positive, and `false` otherwise.
    + `negative`: the opposite of the above.

3. A couple of other useful built-in mathematical functions are `Math.random`,
   `Math.floor` and `Math.ceil`. Look these functions up on
   [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)
   to learn how they work, and use them to implement the following functions:

   + `randInt`: Should accept a single numeric argument (`n`), and return a
     number from `0` to `n`.
   + `guessMyNumber`: Should accept a single numeric argument and compare it to
     a random number between `0` and `5`. It should return one of the following
     strings:

     - "You guessed my number!" if the argument matches the random number.
     - "Nope! That wasn't it!" if the argument did not match the random number.

#### Logical Operators

1. Is the `!` operator a *unary* operator, or *binary* operator?

2. Evaluate each of the following expressions first on a whiteboard, and then in
   a console:

   ```js
   !(2 >= 2)
   !(4 === 4)
   !(5 !== 5)
   ```

3. Evaluate each of the following expressions first on a whiteboard, and then in a
   console:

   ```js
   1 > 2 || 2 > 2 || 3 > 2
   5 < 5 || 75 < 74
   ```

#### Conditionals: `else if` & `else`

1. This guy named "Joe" keeps blacking out at the bar that your function,
   `bouncer` (from the previous module), is in charge of; thus, management has
   decided to add him to the "blacklist" -- modify the `bouncer` function from
   the previous section so that the person named "Joe" is rejected with an
   appropriate message, regardless of his age.

2. Write a function called `scoreToGrade` that accepts a *number* as a parameter
   and returns a *string* representing a letter grade corresponding to that
   score.

   For example, the following grades should be returned given these scores:

   + 'A' >= 90
   + 'B' >= 80
   + 'C' >= 70
   + 'D' >= 60
   + 'F' < 60

   ```js
   function scoreToGrade(score) {
     // TODO: your code here
   }
   scoreToGrade(95); // => 'A'
   scoreToGrade(72); // => 'C'
   ```

3. Modify the `scoreToGrade` function so that it returns `'INVALID SCORE'` if
   the score is greater than `100` or less than `0`.

### More Practice

1. Think of at least three activities that you enjoy doing outdoors and the
   range of temperatures and weather patterns (*e.g* sunny, windy, snowy, rainy,
   etc.) that are best for these activities. Write a function `whatToDoOutside`
   that accepts a *temperature* and *condition* as parameters and outputs a
   string of the format: "The weather is ideal for: ACTIVITY" (where ACTIVITY is
   an actual activity). Make sure to include an `else` that indicates what
   should be done if the conditions do not match any activities. If you're short
   on inspiration, here are some ideas:

   + **Snow Sports:** snowboarding, skiing
   + **Water Sports:** surfing, sailing, paddle boarding, swimming
   + **Team Sports:** basketball, baseball, football (American or everywhere
     else), etc.

2. The `guessMyNumber` function from the **Booleans & Conditionals** module
   (**More Practice** section) accepts a guess `n` and checks it against a
   random number from `0` to `5` -- if the guess `n` is greater than `5`, output
   a different message indicating that the guess is out of bounds.

   - **NOTE:** It will be helpful to *first* write a `randInt` function that
     accepts a number `n` and computes a random integer from `0` to `n`; then,
     you can use this function in `guessMyNumber`.

3. Modify the `scoreToGrade` function so that it returns `'A+/A-'` for
   scores of 98-100/90-92 respectively. Apply the same logic for all other
   letter grades.

### Advanced

1. The bar that employs our `bouncer` function has decided to do live music on
   Friday and Saturday nights, and will be admitting those that are over 18 to
   the bar on those nights; the catch however, is that all who are 21 or older
   will need to be given a wristband to distinguish them from the minors. Modify
   your `bouncer` function to handle this situation.

2. You should have noticed a large amount of repetitive code when modifying
   `scoreToGrade` to accommodate `+` or `-` grades. When we do lots of repetitive
   things, that's a clear signal that there's a better way. Write a helper function
   `letterGrade` that accepts two arguments, *letter* and *score*, and works as
   follows:

   ```js
   function letterGrade(letter, score) {
     // your code here
   }
   // These are examples of what a *working* function would output.
   letterGrade('A', 95); // => 'A'
   letterGrade('A', 91); // => 'A-'
   letterGrade('B', 88); // => 'B+'
   letterGrade('monkey', 160); // => 'monkey-'
   ```

   Finally, use `letterGrade` to remove the repetition in `scoreToGrade`.

3. It turns out that we can write logical *and* and logical *or* in terms of each
   other and logical *not* using <a href="https://en.wikipedia.org/wiki/De_Morgan%27s_laws" target="_blank">De Morgan's Laws</a>.

     + Write a function `or` that works like `||`, but only uses `!` and `&&`.
     + Write a function `and` that works like `&&`, but only uses `!` and `||`.

1. Fix each of the following variable declarations in a console -- some are
   syntactically invalid, some are disobey style guidelines, and some are just
   weird.

   ```js
   var "animal" = "monkey";
   var "monkey" = animal;
   var x= 15;
   var y =10;
   var var = "huh?";
   var true = false;
   var isTenEven = 10 % 2 = 0;
   ```

2. Perform the following in the console:

   + Create a variable `firstName` and assign your first name to it.
   + Create another variable, `lastName`, and assign your last name to it.
   + Have a middle name? If so, repeat the process.
   + Now, create a variable `fullName` and assign your full name to it by using
     the above variables.


3. For each of the following code blocks, **use a whiteboard (or a piece of paper)** to reason about
   what the value of `x` is supposed to be on the last line. Once you have
   arrived at a conclusion that you are comfortable with, enter the lines into a
   console and check your answer. Was your hypothesis correct? If not, ensure
   that you understand why (talk with a classmate, or ask for help).

   ```js
   var x = 5;
   x + 10;
   x; // => ???
   ```

   ```js
   var x = 17;
   x = (x + 1) / 2;
   x * 4;
   x; // => ???
   ```

   ```js
   var x = 5;
   var y = 20;
   x = y;
   y = y + 7;
   x; // => ???
   ```

   ```js
   var x = 10;
   var y = 5;
   x = (x * 4) - 3;
   x + 17;
   x = x + y;
   x; // => ???
   ```

4. Write a function called `counter` that, when invoked, always returns a number
   that is *one more* than the previous invocation. For instance:

   ```js
   function counter() {
     // TODO: your code here
   }
   counter(); // => 1
   counter(); // => 2
   counter(); // => 3
   // etc.
   ```

   **HINT:** You'll need a variable for this. *Where* should the variable be
   declared?

### More Practice

**All of the following exercises involve augmenting the `guessMyNumber` function.**

1. In a previous module you wrote a function called `guessMyNumber` that
   simulated a guessing game: the idea is that the function picks a random
   number between `0` and `5`, and you invoke the function with your guess -- if
   you and the function are thinking of the same number, you win! Otherwise, the
   function informs you that your guess was incorrect. A version of this game
   might look like this (the `randInt` function is included for convenience):

   ```js
   function guessMyNumber(n) {
     if (n > 5) {
       return "Out of bounds! Please try a number between 0 and 5.";
     } else if (n === randInt(5)) {
       return "You guessed my number!";
     }
     return "Nope! That wasn't it!";
   }

   function randInt(n) {
     return Math.floor(Math.random() * (n + 1))
   }
   ```

   Read and test both of the functions in your console and
   affirm that you understand how they work; then, answer the following
   questions:

   + At present, the guess should be between `0` and `5`. We can think of `5` as
     the *upper bound* of the guess. How many times is the *upper bound*
     repeated? What if we wanted to change the upper bound to `6`? How many
     changes would be required?
   + Create a variable called `upperBound` to hold the upper bound, and then
     reference **it** instead of the number `5`. If you were asked to change the
     upper bound to some other number (*e.g.* `7`), you should only have to make
     *one* change.
   + Modify `guessMyNumber` so that if the guess is incorrect, `guessMyNumber`
     includes the correct guess in its output, *e.g.* `"Nope! The correct number
     was: X"` (where `X` would have been the correct number).


2. At present, the guessing game picks a new random number every time it is
   "played" (invoked). Now that you know how to make information *persistent*
   between function invocations, change the guessing game so that it picks a
   random number **once** and allows you to guess until you get the correct
   answer.

3. It would be really cool if, after the answer was guessed, the message
   included the number of guesses it had taken to find the answer; for example,
   "You guessed my number in 3 guesses."

   + **Tangent Problem:** What happens if you get the number right on the
     first try? Does it say, "You guessed my number in 1 guesses."? If so,
     perhaps the wording should be different? Some better ideas are:

     + "You guessed my number in 1 guess."
     + "Congratulations! You guessed my number on the first try!"


4. Implement a way to **limit** the number of guesses that can be made so that a
   player loses after exceeding the limit.

5. Keep track of a **high score** (the lowest number of guesses) between games,
   and, when the correct number has been guessed in a record number of times,
   include in the message something that indicates that a new high score has
   been set.

6. Whenever a player wins, **increase the difficulty** by increasing the
   `upperBound`; whenever a player loses, **decrease the difficulty** by
   decreasing the `upperBound`.

7. Implement a **high/low hinting system** to tell the the user that the guess
   is either too high or too low. You may want to increase the `upperBound` on
   the guess.

### Advanced

There is an optimal way to play this game that works like this, given
*upperBound* as the upper bound, *lowerBound* as the lower bound, and *guess* as
the guess:

1. Initialize the starting values:

   - *guess* as half of the *upperBound*
   - *lowerBound* as 0


2. Execute *guessMyNumber* with *guess*:

    + If the guess was **too high**, repeat (2) where:
      - the new *guess* is half of the difference of *guess* and *lowerBound*
      - the new *upperBound* is *guess*
    + If the guess was **too low**, repeat (2) where:
      - The new *guess* is half of the difference of *upperBound* and *guess*
      - The new *lowerBound* is *guess*
    + If the guess was **correct** stop.

**Your task** is to write a function that implements the above algorithm
to play the game on your behalf. The first thing that you will need to
do is create another version of `guessMyNumber` that returns output that
will be easier for another function to work with, *e.g.* use `1` for too
high, `-1` for too low, `0` for correct.

Relative to *upperBound*, how many guesses does it take on average to
guess correctly?

Some recommendations:

  + Make use of a whiteboard.
  + Play the existing game yourself using the above steps to get an
    idea of how the algorithm works.
  + Work with a partner.
  + Read about `console.log` on
    [MDN](https://developer.mozilla.org/en-US/docs/Web/API/Console/log)
    and use it to help with debugging.