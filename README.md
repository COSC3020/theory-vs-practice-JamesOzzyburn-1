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

$1c)$ The third reason that asymptotic analysis can be misleading is for $\Omega$ and $O$ bounds the complexity is just less than $\Theta$ and greater than $\Theta$ repectivly. It doesnt need to be a specific value or in other words $\Omega$ and $O$ have loose bounds where as $\Theta$ has tight bounds.

$2)$ I think it would take about 6.5 seconds to do a search over 10,000 elements. I believe this because as it's a logrithmic increase every doubling of elements which is results in about 0.5 seconds per doubling of elements and if we double three times it would add about 1.5 to get us to our total of 6.5 seconds for a search in a tree with 10,000 elements.

$3a)$ It could be that the OS or other programs could have been doing alot of stuff in the background in the second run making the code have to share or wait on resources.

$3b)$ It could be that the data that was comparing was different, in the first run through we were comparing ints and in the second we were comparing strings which brings more overhead.

$3c)$ It could have been that when you were running the first tree the program was all able to be stored in ram. However when you ran the seconds tree it had to swap to disc slowing it down.