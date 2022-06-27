---
title: Notes on Testing
date: 05-24-2022
---

## Testing Overview

Before the 2000s testing was largely ignored, but since then automated testing started getting more attention. Having test suites (collection of hundreds and possibly thousands of tests) helps engineers make sure that their code is behaving the way they intended. Testing became part of the engineering work routine rather than an afterthought. So what needs to be tested? The answer is everything you do not want to break in your project.

#### Write, Run, React
- Run tests frequently throughout the day
- Fix broken tests quickly

#### Benefits of Testing Code
- Less debugging
- Increased confidence in changes
- Improved documentation (tests can serve as some sort of documentation)
- Simpler code reviews
- Thoughtful design (testing will reveal if your code is modular enough or too coupled)
- Fast, high-quality releases

#### Designing a test suite
##### Test size and test scope
*Size* - How many resources the test uses

- Small - tests one functionality
- Medium - can make network calls to localhost, test a combination of UI and server code
- Large - tests can run across multiple machines, slow speed

##### Test flakiness 
The probability of test flakiness should remain under 1% (calculated by determining how often you run tests and how many tests fail a day)

*Scope* - how much code is being tested by a given test

- Unit test - narrow scoped, tests individual class or method (about 80% of all tests)
- Integration test - medium scoped, test interaction between small number of components (for instance, server and its database) (about 15% of all tests)
- Functional test, End-to-end test, system test - large scoped, validate interaction between several distinct parts of the system (5% of all tests)

## Unit Testing
Explores the idea of maintainability and techniques for achieving it

- Tests shouldn't be brittle, for example they shouldn't break with the introduction of unrelated code
	- Ideal test is unchanging
		- Pure refactorings
		- New features
		- Bug fixes
		- Behavior changes
	- Test via Public APIs
	- Test State, Not Interactions
- Tests should be clear
	- Make your tests complete and concise
	- Test Behaviors, Not Methods (Given, When, Then - “_Given_ that a bank account is empty, _when_ attempting to withdraw money from it, _then_ the transaction is rejected.”). Some frameworks, like Cucumber and Spock directly bake in given, when, then.
	- Don't put logic in tests
	- Tests should be DAMP (Descriptive and Meaningful Phrases), not DRY 

### Test Doubles
A [_test double_](https://oreil.ly/vbpiU) is an object or function that can stand-in for a real implementation in a test, similar to how a stunt double can stand in for an actor in a movie.
 
 - Testability 
	 - To use test doubles, a codebase needs to be designed to be _testable_—it should be possible for tests to swap out real implementations with test doubles.
- Applicability 
	- Use of test doubles should not lead to tests that are brittle, complex, and less effective
- Fidelity
	- _Fidelity_ refers to how closely the behavior of a test double resembles the behavior of the real implementation that it’s replacing.

#### Techniques for Using Test Doubles
- Fake
	- A [_fake_](https://oreil.ly/rymnI) is a lightweight implementation of an API that behaves similar to the real implementation but isn’t suitable for production; for example, an in-memory database.
- Stubbing
	- [_Stubbing_](https://oreil.ly/gmShS) is the process of giving behavior to a function that otherwise has no behavior on its own—you specify to the function exactly what values to return (that is, you _stub_ the return values).
- Interaction testing
	- [_Interaction testing_](https://oreil.ly/zGfFn) is a way to validate _how_ a function is called without actually calling the implementation of the function.
- Mocks (Unfinished)

## Testing at Relevize: Frameworks and Libraries (Unfinished)

In our codebase, to implement unit testing, we will be using [Vite](https://vitest.dev/) and [Vue Test Utils](https://v1.test-utils.vuejs.org/). 

## *More resources*  
Winters, Titus, et al. *Software Engineering at Google: Lessons Learned from Programming over Time.* O'Reilly, 2020 (Chapters 11-14)

Riccomini, Chris, et al. *The Missing Readme: A Guide for The New Software Engineer.* No Starch Press, 2021 (Chapter 6)

Hendrickson, Elisabeth. *Explore It!*. O'Reilly, 2013

