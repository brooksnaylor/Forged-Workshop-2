# Forged-Workshop-2

### Comparison Operators

#### Basic Practice (5 points each)

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

   **POTENTIAL ANSWERS**:
   ```js
   12 < 78
   // => true

   24 > 16
   // => false

   45 !== 46
   // => true

   "45" === 45
   // => false

   "6" !== "six"
   // => true
   ```

4. Write a function `oldEnoughToDrink` that takes an `age` as an argument and
   returns `true` if the person with that age is old enough to drink.

   **ANSWER:**
   ```js
   function oldEnoughToDrink(age) {
     if (age >= 21) {
       return true;
     }
     return false;
   }
   ```

5. There's an easy way to figure out how long a string is by adding `.length` to
   the end of it. Try this out in the console:

  ```js
  "hello".length;
  "".length;
  "John Doe".length;
  ```

  Write a function `sameLength` that accepts two strings as arguments, and
  returns `true` if those strings have the same length, and `false` otherwise.

  **ANSWER:**
  ```js
  function sameLength(string1, string2) {
    if (string1.length === string2.length) {
      return true;
    }
    return false;
  }
  ```

6. Write a function `passwordLongEnough` that accepts a "password" as a
   parameter and returns `true` if that password is *long enough* -- you get to
   decide what constitutes *long enough*.

   **ANSWER:**
   ```js
   function passwordLongEnough(password) {
     if (password.length >= 8) {
       return true;
     }
     return false;
   }
   ```

### Conditionals: `if`

#### Basic Practice (5 points each)

1. Write a function `bouncer` that accepts a person's name and age as arguments,
   and returns either "Go home, NAME.", or "Welcome, NAME!" (where NAME is the
   parameter that represents the person's name) depending on whether or not the
   person is old enough to drink.

   **ANSWER:**
   ```js
   function bouncer(name, age) {
     if (age >= 21) {
       return 'Welcome, ' + name + '!';
     }
     return 'Go home, ' + name + '.';
   }
   ```

2. Write a function `max` that takes two numbers as arguments, and returns the
   larger one.

   **ANSWER:**
   ```js
   function max(num1, num2) {
     if (num1 > num2) {
       return num1;
     }
     return num2;
   }
   ```

3. Write a function `min` that takes two numbers as arguments, and returns the
   smaller one.

   **ANSWER:**
   ```js
   function min(num1, num2) {
     if (num1 < num2) {
       return num1;
     }
     return num2;
   }
   ```

4. Write functions `larger` and `smaller` that each accept two strings as
   arguments, and return the *larger* and *smaller* strings, respectively.

   **ANSWER:**
   ```js
   function larger(string1, string2) {
     if (string1.length > string2.length) {
       return string1;
     }
     return string2;
   }

   function smaller(string1, string2) {
     if (string1.length < string2.length) {
       return string1;
     }
     return string2;
   }

#### More Practice (10 points each)

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

   **POTENTIAL ANSWERS**:
   ```js
   106 <= 12
   // => false

   "wiz" === "wiz"
   // => true

   7 * 7  === 49
   // => true

   12 !== (24 / 2)
   // => false

   (20 % 2) <= 10
   // => true

   (9 / 3) + (5 * 5) === 28
   // => true
   ```

2. Write the following functions that each accept a single number as an
   argument:

    + `even`: returns `true` if its argument is even, and `false` otherwise.

     **ANSWER:**
    ```js
    function even(num) {
      // The number is even if it can be divided by 2 with no remainder
      if (num % 2 === 0) {
        return true;
      }
      return false;
    }
    ```

    + `odd`: the opposite of the above.

     **ANSWER:**
    ```js
    function odd(num) {
      // The number is odd if it cannot be divided by 2 with no remainder
      if (num % 2 !== 0) {
        return true;
      }
      return false;
    }
    ```
    + `positive`: returns `true` if its argument is positive, and `false` otherwise.

     **ANSWER:**
    ```js
    function positive(num) {
      if (num >= 0) {
        return true;
      }
      return false;
    }
    ```

    + `negative`: the opposite of the above.

     **ANSWER:**
    ```js
    function negative(num) {
      if (num < 0) {
        return true;
      }
      return false;
    }
    ```

3. A couple of other useful built-in mathematical functions are `Math.random`,
   `Math.floor` and `Math.ceil`. Look these functions up on
   [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)
   to learn how they work, and use them to implement the following functions:

   + `randInt`: Should accept a single numeric argument (`n`), and return a
     number from `0` to `n`.

     **ANSWER:**
     ```js
     function randInt(n) {
       return Math.floor(Math.random() * (n + 1));
     }
     ```

   + `guessMyNumber`: Should accept a single numeric argument and compare it to
     a random number between `0` and `5`. It should return one of the following
     strings:

     + "You guessed my number!" if the argument matches the random number.
     + "Nope! That wasn't it!" if the argument did not match the random number.

     **ANSWER:**
     ```js
     function guessMyNumber(guess) {
        var randomNum = Math.floor(Math.random() * 6);
        if (guess === randomNum) {
          return "You guessed my number!";
        }
        return "Nope! That wasn't it!";
     }
     ```
### Logical Operators

#### Basic Practice (5 points each)

1. Is the `!` operator a *unary* operator, or *binary* operator?

   **ANSWER:** It is a unary operator, because it has only one operand.

2. Evaluate each of the following expressions first on a whiteboard, and then in
   a console:

   ```js
   !(2 >= 2)      // => false
   !(4 === 4)     // => false
   !(5 !== 5)     // => true
   ```

3. Evaluate each of the following expressions first on a whiteboard, and then in a
   console:

   ```js
   1 > 2 || 2 > 2 || 3 > 2    // => true
   5 < 5 || 75 < 74           // => false
   ```
### Conditionals: `else if` & `else`

#### Basic Practice (5 points each)

1. This guy named "Joe" keeps blacking out at the bar that your function,
   `bouncer` (from the previous module), is in charge of; thus, management has
   decided to add him to the "blacklist" -- modify the `bouncer` function from
   the previous section so that the person named "Joe" is rejected with an
   appropriate message, regardless of his age.

    **ANSWER:**
   ```js
   function bouncer(name, age) {
     if (name === 'Joe') {
       return 'Go home, ' + name + '. You are banned from the bar.';
     } else if (age >= 21) {
       return 'Welcome, ' + name + '!';
     }
     return 'Go home, ' + name + '.';
   }
   ```

2. Write a function called `scoreToGrade` that accepts a *number* as a parameter
   and returns a *string* representing a letter grade corresponding to that
   score.

   For example, the following grades should be returned given these scores:

   + 'A' >= 90
   + 'B' >= 80
   + 'C' >= 70
   + 'D' >= 60
   + 'F' < 60

   **ANSWER:**
   ```js
   function scoreToGrade(score) {
     if (score >= 90) {
       return 'A';
     } else if (score >= 80) {
       return 'B';
     } else if (score >= 70) {
       return 'C';
     } else if (score >= 60) {
       return 'D';
     } else {
       return 'F';
     }
   }
   scoreToGrade(95); // => 'A'
   scoreToGrade(72); // => 'C'
   ```

3. Modify the `scoreToGrade` function so that it returns `'INVALID SCORE'` if
   the score is greater than `100` or less than `0`.

   **ANSWER:**
   ```js
   function scoreToGrade(score) {
     if (score > 100 || score < 0) {
       return 'INVALID SCORE';
     } else if (score >= 90) {
       return 'A';
     } else if (score >= 80) {
       return 'B';
     } else if (score >= 70) {
       return 'C';
     } else if (score >= 60) {
       return 'D';
     } else {
       return 'F';
     }
   }
   ```


#### More Practice (10 points each)

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

    **ANSWER:**
   ```js
   function whatToDoOutside(temperature, condition) {
     var activity = '';

     if (temperature >= 80 && condition === 'sunny') {
       activity = 'swimming';
     } else if (temperature >= 80 && condition === 'windy') {
       activity = 'sailing';
     } else if (temperature >= 60 && condition === 'sunny') {
       activity = 'basketball';
     } else if (temperature >= 60 && condition === 'windy') {
       activity = 'hiking';
     } else if (temperature < 60 && condition === 'snowy') {
       activity = 'skiing';
     } else {
       activity = 'building a bonfire';
     }

     return 'The weather is ideal for: ' + activity + '.';
   }
   ```

2. The `guessMyNumber` function from the **Booleans & Conditionals** module
   (**More Practice** section) accepts a guess `n` and checks it against a
   random number from `0` to `5` -- if the guess `n` is greater than `5`, output
   a different message indicating that the guess is out of bounds.

   - **NOTE:** It will be helpful to *first* write a `randInt` function that
     accepts a number `n` and computes a random integer from `0` to `n`; then,
     you can use this function in `guessMyNumber`.

      **ANSWER:**
     ```js
     function randInt(n) {
       return Math.floor(Math.random() * (n + 1));
     }

     function guessMyNumber(n) {
        var randomNum = randInt(5);

        if (n > 5) {
          return "Your guess is out bounds."
        } else if (n === randomNum) {
          return "You guessed my number!";
        }
        return "Nope! That wasn't it!";
     }
     ```

3. Modify the `scoreToGrade` function so that it returns `'A+/A-'` for
   scores of 98-100/90-92 respectively. Apply the same logic for all other
   letter grades.

   **ANSWER:**
   ```js
   function scoreToGrade(score) {
     if (score > 100 || score < 0) {
       return 'INVALID SCORE';
     } else if (score >= 98) {
       return 'A+';
     } else if (score >= 93) {
       return 'A';
     } else if (score >= 90) {
       return 'A-';
     } else if (score >= 88) {
       return 'B+';
     } else if (score >= 83) {
       return 'B';
     } else if (score >= 80) {
       return 'B-';
     } else if (score >= 78) {
       return 'C+';
     } else if (score >= 73) {
       return 'C';
     } else if (score >= 70) {
       return 'C-';
     } else if (score >= 68) {
       return 'D+';
     } else if (score >= 63) {
       return 'D';
     } else if (score >= 60) {
       return 'D-';
     } else {
       return 'F';
     }
   }
   ```

#### Advanced (15 points each)

1. The bar that employs our `bouncer` function has decided to do live music on
   Friday and Saturday nights, and will be admitting those that are over 18 to
   the bar on those nights; the catch however, is that all who are 21 or older
   will need to be given a wristband to distinguish them from the minors. Modify
   your `bouncer` function to handle this situation.

   **ANSWER:**
   ```js
   function bouncer(name, age, day) {
     if (name === 'Joe') {
       return 'Go home, ' + name + '. You are banned from the bar.';
     } else if ((day === 'Friday' || day === 'Saturday') && age >= 21) {
       return 'Welcome, ' + name + '! Here is your wristband.'
     } else if ((day === 'Friday' || day === 'Saturday') && age >= 18) {
       return 'Welcome, ' + name + '! You can come in but no drinking.'
     } else if (age >= 21) {
       return 'Welcome, ' + name + '!';
     }
     return 'Go home, ' + name + '.';
   }
   ```

2. You should have noticed a large amount of repetitive code when modifying
   `scoreToGrade` to accommodate `+` or `-` grades. When we do lots of repetitive
   things, that's a clear signal that there's a better way. Write a helper function
   `letterGrade` that accepts two arguments, *letter* and *score*, and works as
   follows:

   **ANSWER:**
   ```js
   function letterGrade(letter, score) {
     if (score % 10 >= 8) {
       return letter + '+';
     } else if (score % 10 >= 3) {
       return letter;
     } else {
       return letter + '-';
     }
   }

   // These are examples of what a *working* function would output.
   letterGrade('A', 95); // => 'A'
   letterGrade('A', 91); // => 'A-'
   letterGrade('B', 88); // => 'B+'
   letterGrade('monkey', 160); // => 'monkey-'
   ```

   Finally, use `letterGrade` to remove the repetition in `scoreToGrade`.

   **ANSWER:**
   ```js
   function scoreToGrade(score) {
     if (score > 100 || score < 0) {
       return 'INVALID SCORE';
     } else if (score === 100) {
       return 'A+';
     } else if (score >= 90) {
       return letterGrade('A', score);
     } else if (score >= 80) {
       return letterGrade('B', score);
     } else if (score >= 70) {
       return letterGrade('C', score);
     } else if (score >= 60) {
       return letterGrade('D', score);
     } else {
       return 'F';
     }
   }
   ```

3. It turns out that we can write logical *and* and logical *or* in terms of each
   other and logical *not* using <a href="https://en.wikipedia.org/wiki/De_Morgan%27s_laws" target="_blank">De Morgan's Laws</a>.

     + Write a function `or` that works like `||`, but only uses `!` and `&&`.

      **ANSWER:**
     ```js
     function or(a, b) {
       return !(!a && !b);
     }

     or(true, false);    // => true
     or(true, true);     // => true
     or(false, false);   // => false
     ```

     + Write a function `and` that works like `&&`, but only uses `!` and `||`.

      **ANSWER:**
     ```js
     function and(a, b) {
       return !(!a || !b);
     }

     and(true, false);   // => false
     and(true, true);    // => true
     and(false, false);  // => false
     ```

### Variables

#### Basic Practice (5 points each)

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

   **FIXED:**
   ```js
   var animal = "monkey";
   var monkey = animal;
   var x = 15;
   var y = 10;
   var variable = "huh?";
   var truth = false;
   var isTenEven = 10 % 2 === 0;
   ```

2. Perform the following in the console:

   + Create a variable `firstName` and assign your first name to it.
   + Create another variable, `lastName`, and assign your last name to it.
   + Have a middle name? If so, repeat the process.
   + Now, create a variable `fullName` and assign your full name to it by using
     the above variables.

    **ANSWER:**
   ```js
   var firstName = 'Michael';
   var lastName = 'Jordan';
   var middleName = 'Jeffrey';
   var fullName = firstName + ' ' + middleName + ' ' + lastName;
   ```

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

   **ANSWER:**
   ```js
   x; // => 5
   ```

   ```js
   var x = 17;
   x = (x + 1) / 2;
   x * 4;
   x; // => ???
   ```

   **ANSWER:**
   ```js
   x; // => 9
   ```

   ```js
   var x = 5;
   var y = 20;
   x = y;
   y = y + 7;
   x; // => ???
   ```

   **ANSWER:**
   ```js
   x; // => 20
   ```

   ```js
   var x = 10;
   var y = 5;
   x = (x * 4) - 3;
   x + 17;
   x = x + y;
   x; // => ???
   ```

   **ANSWER:**
   ```js
   x; // => 42
   ```

4. Write a function called `counter` that, when invoked, always returns a number
   that is *one more* than the previous invocation. For instance:

   ```js
   var count = 0;

   function counter() {
     count = count + 1;
     return count;
   }
   counter(); // => 1
   counter(); // => 2
   counter(); // => 3
   // etc.
   ```

   **HINT:** You'll need a variable for this. *Where* should the variable be
   declared?

   **ANSWER:** Declaring the variable outside of the function (in global scope) allows the program to properly track how many times the counter() function has been called. The value of the count variable is persistent.
