# Atomic Testing Framework Expanded (ATFE)
Red Canary released some years ago, a framework to perform quick tests called "Atomic Red Teaming". They made a great job and you can check their stuff out  here: https://github.com/redcanaryco/atomic-red-team

## Why ATFE
When I've used the Red Canary Atomic Red Team testing framework I've had a few shortcomings making it extra challenging to do the work, despite the frameworks attempts at making it better. These shortcomings were most commonly:

- There is a general lack of easy to access knowlege of the outcomes of each test, especially in terms of impact on network and local events being triggered. 
- There is a general lack of information as to what is required for a test to run successfully, and descriptors on how we know the test worked.
- Testers have previously wanted to be able to run a series of tests which have been used in previous attacks, so the tests better "simulate" what an attacker may choose to do.

This project aims to expand upon some of these tests by providing the above information to each one as possible. The end goal is to provide information to testers about these tests so they understand not only what the test do, but may also gain insight into what events and detections may go off.

## How to use it?
There are primarily two methods of using the atomic red teaming framework.
- Using the Invoke-Atomic methods provided by Red Canary.
- Executing each test manually.
In this framework we've elected to only describe the tests manually as the method of execution using Invoke-Atomic is well defined by Red Canary.

## Release plan?
Despite being initially developed for my previous employer, this project is now a passion project which is developed in my spare time, release plans are not strict and thus updates to the project will be sporadic.
