# Exercise 3 - Creating and using custom base images

## Problem
Rebuilding images takes too long
Updates have to happen in multiple places

## Principle
Custom base images

## Detail
Keeping up with dependency changes in the OS version or OS utilities, or even language versions this can mean changing many files.
These might need to be changed weekly, imagine that across 100 projects or images in an organisation!

Building these layers every time you change your project (even if they are cached) can take a while.

Build common things separately! And only on one cadence (not once per project)

N.B. In a business context this would probably involve a private conatiner image registry such as AWS ECR or GitHub packages. For this exercise, your own machine will supply the custom image

## Exercise

- Build the original images for app 1 and app 2, in their respective folders and record the time taken for each to build
- Create a custom base image in `Dockerfile.common` and build it, using a tag you will remember e.g. `docker-deep-dive/custom/app-base` and record how long it took
- For app1, create a better dockerfile using the custom base image you created
- Build the image for app1 again, and note how long it took
