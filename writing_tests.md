_(in fact, this would be part of the new "docs" repo, not a file in this repo.)_

When implementing an exercise test suite, we want to provide a good user experience for the people writing a solution to the exercise. People should not be confused or overwhelmed.

In most Exercism language tracks, we simulate Test-Driven Development (TDD) by implementing the tests in order of increasing complexity. We try to ensure that each test either

- helps triangulate a solution to be more generic, or
- requires new functionality incrementally.

Many test frameworks will randomize the order of the tests when running them. This is an excellent practice, which helps ensure that subsequent tests are not dependent on side effects from earlier tests. However, in order to simulate TDD we want tests to run *in the order that they are defined*, and we want them to *fail fast*, that is to say, as soon as the test suite encounters a failure, we want the execution to stop. This ensures that the person implementing the solution sees only one error or failure message at a time, unless they make a change which causes prior tests to fail.

This is the same experience that they would get if they were implementing each new test themselves.

Most testing frameworks do not have the necessary configuration options to get this behavior directly, but they often do have a way of marking tests as _skipped_ or _pending_. The mechanism for this will vary from language to language and from test framework to test framework.

Whatever the mechanism—functions, methods, annotations, directives, commenting out tests, or some other approach—these are changes made directly to the test file. The person solving the exercise will need to edit the test file in order to "activate" each subsequent test.
