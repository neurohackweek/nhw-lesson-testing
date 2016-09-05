---
title: "Software testing and Test driven development"
teaching: 30
exercises: 30
questions:
- "Why should we test?"
objectives:
- Learn how to integrate testing into software development **and** research
- Learn to use local and remote tests
keypoints:
- Testing is essential given the diversity of software and platforms
- Tests allow making science more structured and reproducible

---

### In the next one hour:

5 mins - Introduction
10 mins - Introduction to testing [software carpentry]
5 mins - Introduction to test driven development
10 mins - Introduction to continuous integration (travis and circle-ci)
15 mins - Writing your own pytest test
15 mins - Testing brain imaging scripts
5 mins - Questions

### Introduction to software testing?

Some resources:

[Software testing](https://en.wikipedia.org/wiki/Software_testing)
[Software carpentry introduction to testing](http://v4.software-carpentry.org/test/intro.html)
[Test Driven Development (TDD)](https://en.wikipedia.org/wiki/Test-driven_development)

### Why test?

<iframe src="http://retractionwatch.com/2016/05/19/software-glitch-not-intentional-manipulation-sunk-immunology-paper/" width="1024px"></iframe>

### Why test?

<iframe src="http://retractionwatch.com/2016/06/17/jama-authors-retract-and-replace-paper-about-moves-and-kids-mental-health/" width="1024px"></iframe>

### Why test?

<iframe src="http://krugman.blogs.nytimes.com/2013/04/16/holy-coding-error-batman/?_r=0" width="1024px"></iframe>

### Introduction to testing [software carpentry]

<iframe src="http://v4.software-carpentry.org/test/intro.html"></iframe>

### What is test driven development?

Test-driven development (TDD) is a software development process that relies on the repetition of a very short development cycle: requirements are turned into very specific test cases, then the software is improved to pass the new tests, only.

![Test Driven Development](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/TDD_Global_Lifecycle.png/800px-TDD_Global_Lifecycle.png)

### What is test driven work?

1. "Add a check" replaces "Add a test"
2. "Run all checks" replaces "Run all tests"
3. "Do the work" replaces "Write some code"
4. "Run all checks" replaces "Run tests"
5. "Clean up the work" replaces "Refactor code"
6. "Repeat"

### 	Testing levels

1. Unit testing
2. Integration testing
3. Component interface testing
4. System testing
5. Operational Acceptance testing

### Example 1: Testing code?

~~~
def add_two_positive_integers(a, b):
	pass

assert ...
~~~
{: .python}

### Example 2: Testing some imaging?

~~~
def extract_brain_mask(a):
	pass

assert ...
~~~
{: .python}

### Continuous integration

- What is continuous integration?
- How will continuous integration help me?


### Example with continuous integration

Location: https://github.com/ReproNim/simple_workflow

Let's go through the pieces
- circle.yml
- Simple_Prep.sh
- Expected output


### Let's write our own simple workflow
 
> ## Let's write our own simple workflow (click on the arrow to the right to open)
>
>  We will extract a brain mask and test that the routine is doing a good job
>    - Download a structural image
>    - Run `bet` from `FSL`
>    - Run `fslstats` to extract brain volume
>    - Check that this volume is consistent across runs
>    - Add `fslreorient2std` and `robustfov` and then run the rest
>    - Check that this volume is similar to your previous result
{: .challenge}
