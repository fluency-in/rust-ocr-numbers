# Rust: Ocr Numbers

Write a program that, given a 3 x 4 grid of pipes, underscores, and spaces, can determine which number is represented, or whether it is garbled.

# Step One

To begin with, convert a simple binary font to a string containing 0 or 1.

The binary font uses pipes and underscores, four rows high and three columns wide.

```
     _   #
    | |  # zero.
    |_|  #
         # the fourth row is always blank
```

Is converted to "0"

```
         #
      |  # one.
      |  #
         # (blank fourth row)
```

Is converted to "1"

If the input is the correct size, but not recognizable, your program should return '?'

If the input is the incorrect size, your program should return an error.

# Step Two

Update your program to recognize multi-character binary strings, replacing garbled numbers with ?

# Step Three

Update your program to recognize all numbers 0 through 9, both individually and as part of a larger string.

```
 _ 
 _|
|_ 
   
```

Is converted to "2"

```
      _  _     _  _  _  _  _  _  #
    | _| _||_||_ |_   ||_||_|| | # decimal numbers.
    ||_  _|  | _||_|  ||_| _||_| #
                                 # fourth line is always blank
```

Is converted to "1234567890"

# Step Four

Update your program to handle multiple numbers, one per line. When converting several lines, join the lines with commas.

```
    _  _ 
  | _| _|
  ||_  _|
         
    _  _ 
|_||_ |_ 
  | _||_|
         
 _  _  _ 
  ||_||_|
  ||_| _|
         
```

Is converted to "123,456,789"

Follow the instructions [here][rust-testing] to run the tests.

[rust-testing]: https://github.com/exercism/xrust/blob/master/docs/TESTS.md

## Source

Inspired by the Bank OCR kata [http://codingdojo.org/cgi-bin/wiki.pl?KataBankOCR](http://codingdojo.org/cgi-bin/wiki.pl?KataBankOCR)

This exercise is from the [Rust][rust] track on [Exercism][exercism]

[exercism]: http://exercism.io
[rust]: http://exercism.io/languages/rust



