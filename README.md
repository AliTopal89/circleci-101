# circleci-101

The `- image: circleci/ruby:2.4.1` text tells CircleCI what Docker image to use when it builds your project. CircleCI will use the image to boot up a “container” — a virtual computing environment where it will install any languages, system utilities, dependencies, web browsers, and tools, that your project might need to run.

renamed the two jobs so that they have different names. In this example they are named one and two. Changed contents of the echo statements to something different.