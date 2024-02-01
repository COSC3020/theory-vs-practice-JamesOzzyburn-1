[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.


## Answer
$1a)$ The first reason asymptotic analysis may be misleading is that we get rid of all of the constants and lower ordered terms which might have a significant impact on our runtime.

$1b)$ The second reason asymptotic analysis may be misleading is that it doesnt really look at actual runtimes. For example if we have a beefy super computer that can do $100,000,000,000,000$ calculations per second and lets say just for this example that every $n$ is one calculation, you might ask does it really matter what our algorithms asymptotic runtime as if you have $n = 100$ problem every algorithm short of $n!$ is going to be completed so fast that its kinda point less to try and shave off any time.

$1c)$ The third reason aysmptotic analysis may be misleading is that we have to consider what the range for $n$ is our application. For a really trivial example lets say we have two algorithms $\Theta(n^2)$ and $\Theta(n!)$ well for $n = 1$ up to $n = 3$ our $n!$ algorithm is "faster" even though we know that anything past $n = 3$ will result in our $n!$ algorithm being much, much slower. So if we look at to small/non representative amount for $n$ we could easily implement a less optimal algorithm.

$2)$ I think it would take a little less than 8 seconds to do a search over 10,000 elements. I believe this becuase as its a logrithmic increase every doubling of elements which is a little less than a second per double of elements and if we double three-ish times it would add about three seconds to get us 8-ish seconds.

$3a)$ There could be a lower order term at play that given the input size is now significantly affecting the time.

$3b)$ There could be a constant at play that isn't shown. 

$3c)$ The algorithm could have gotten lucky and found the element really quickly in the 1,000 elemnt tree. However in the 10,000 element tree it had to traverse alot more elements until it found it.