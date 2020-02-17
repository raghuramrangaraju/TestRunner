# TestRunner
This a test runner tool which would run the failing JUnit tests. 

<img src="https://github.com/raghuramrangaraju/TestRunner/blob/master/Test%20Runner.svg">


## Situation
Imagine you have different projects. And have many integration tests for your projects. Your Jenkins job will run the integration tests daily. I'm talking about 10000+ tests. Tests failure are normal because of recent checkins, or tests waiting for external responses, wait times, input exceptions. Jenkins job report will show you the list of failures and exceptions.

## Problem
Example: Suppose Jenkins shows 500+ failures. 
Some of the tests failed because of bad data or waiting for an external response - timeout exceptions which are not actual failures. 
So you need to validate them locally.

## Validation
1. Part of the engineer's job is to validate the test failures.
2. It will be time-consuming if you run the 500+ tests locally.
3. Really a time-consuming process. Also, you have to validate in different projects.
## Solution: Test Runner 
  The idea is to have a TestRunner tool which takes in the list of failure tests as an input and run against corresponding module. 
####  Additional tip: 
1. Setup a cron job daily to have a fresh build of the projects with recent changes before you come to the office.
2. Look at the Jenkins report, shows you lists of failures.
3. Use the TestRunner tool to run the failures locally to find the actual failures.
4. This tool makes developer life easier. Not to worry about spending more time on running tests locally.
