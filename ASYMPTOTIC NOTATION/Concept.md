![image](https://github.com/kutluk-ken/Data-Structures-in-Python/assets/56012015/1cfd49cb-65e1-410d-8d9c-95c555830b63)

### Review
Let’s review what we learned:

- We use asymptotic notation to describe the runtime of a program. The three types of asymptotic notation are big Theta, big Omega, and big O.
- We use big Theta (Θ) to describe the runtime if the runtime of the program is the same in every case.
- The different common runtimes from fastest to slowest are: Θ(1), Θ(log N), Θ(N), Θ(N log N), Θ(N2), Θ(2N), Θ(N!).
- We use big Omega (Ω) to describe the best-case running time of a program.
- We use big O (O) to describe the worst-case running time of a program.
- We typically describe a program’s running time in terms of big O.
- When finding the runtime of a program with multiple steps, you can divide the program into different sections and add the runtimes of the various sections. You can then take the slowest runtime and use that runtime to describe the entire program.
- When analyzing the runtime of a program, we care about which part of the program is the slowest.
Now that we conceptually understand what asymptotic notation is, let’s practice analyzing and improving runtimes with real programming language examples!

##### Space Complexity
Asymptotic notation is often used to describe the runtime of a program or algorithm, but it can also be used to describe the space, or memory, that a program or algorithm will need.
Think about a simple function that takes in two numbers and returns their sum:

```
def add_numbers(a, b):
  return a + b
```
This function has a space complexity of O(1), because the amount of space it needs will not change based on the input. While this function also has a constant runtime of O(1), most functions do not have matching space and time complexities.

Let’s take a look at another function:
```
def simple_loop(input_array):
  for i in input_array:
    print(i)
```
As we know, a simple for loop that goes through every element in an array of size n has a linear runtime of O(n). However, this function takes O(1) space since no new variables are being created and therefore no more space must be allocated.

A recursive function that is passed the same array or object in each call doesn’t add to the space complexity if the array or object is passed by reference (which it is in Python).

Like with time complexity, space complexity denotes space growth in relation to the input size. It’s also important to note that space complexity usually refers to any additional space that will be needed, and doesn’t count the space of the input. So a function could have 10 arrays passed into it, but if all it does inside is print 'Hello World!', then it still takes O(1) space.
