# Looping

## Objectives

2. Introduce the concept of a basic `loop`.
3. Introduce the `break` keyword.
4. Introduce the concept of an incrementing counter.
5. `break` out of a `loop` based on a `counter`.

## Introduction

There are a number of different ways to accomplish looping––the task of telling our program to do something a certain number of times. Here, we'll be looking at the most basic way to build a loop: using the `loop` keyword.

## The `loop` Keyword

The first looping construct that we'll discuss is `loop`. This is the simplest looping construct that we have in Ruby. It simply executes a block (the code that is between the `do` and `end` keywords). Try this in IRB in your Terminal:

```ruby
loop do
  puts "I have found the Time Machine!"
end
```

This will output `I have found the Time Machine!` an infinite number of times in your Terminal. Use `Control`+`C` to break out of the loop in your terminal (you might need to press it twice).  Worst case scenario, you can close the terminal and open a new one (in c9: Window > New Terminal).

Loops start with the `loop` keyword and are opened by the following `do` and `end` block. All the code that goes inside the `do` and `end` is considered the loop's body or block; that's the code that will execute on repeat.

## Stopping Loops with Break and Counters

Infinite loops will break our program. The `loop` keyword alone will create an infinite loop. Generally, we want to loop only a certain number of times. We can use the `break` keyword inside the body of the loop to exit or abort the loop and continue with the rest of our code. Consider:

```ruby
loop do
  puts "You'll see this exactly once."
  break # Exit the Loop
end

puts "And the Loop is Done"
```

Our loop starts, it prints our message, and then the next line of code, `break` will actually end the loop. A loop that only runs once isn't useful. Neither is a loop that runs forever. So how do we actually build a useful loop, say, that runs exactly 10 times? Well first, we need a counter. Then we need to conditionally break out of the loop when the counter reaches 10. Then we need to increment the counter at every iteration (or execution of the loop).

```ruby
counter = 0 # Start our counter at 0, we have never run the loop
loop do # Start our loop
  # increment the current value of counter by 1 and reassign that value back to counter. 
  counter + 1

  # Do Something
  puts "Iteration #{counter} of the loop"

  if counter >= 10 # If our counter is 10 or more
    break # Stop the loop
  end
end
```

If you copy this to IRB you'll see:

```
Iteration 1 of the loop
Iteration 2 of the loop
Iteration 3 of the loop
Iteration 4 of the loop
Iteration 5 of the loop
Iteration 6 of the loop
Iteration 7 of the loop
Iteration 8 of the loop
Iteration 9 of the loop
Iteration 10 of the loop
```

This is a common basic loop. With this construct we can `break` a `loop` based on any condition, but the iteration count is a very common condition for stopping the loop.