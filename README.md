# circleci-101

The `- image: circleci/ruby:2.4.1` text tells CircleCI what Docker image to use when it builds your project. CircleCI will use the image to boot up a “container” — a virtual computing environment where it will install any languages, system utilities, dependencies, web browsers, and tools, that your project might need to run.

Renamed the two jobs so that they have different names. In this example they are named one and two. Changed contents of the echo statements to something different.

---

### Using Workspaces to Share Data Among Jobs

Each workflow has an associated workspace which can be used to transfer files to downstream jobs as the workflow progresses. The workspace is an additive-only store of data. Jobs can persist data to the workspace. This configuration archives the data and creates a new layer in an off-container store.

For example, Scala projects typically require lots of CPU for compilation in the build job. In contrast, the Scala test jobs are not CPU-intensive and may be parallelised across containers well. Using a larger container for the build job and saving the compiled data into the workspace enables the test containers to use the compiled Scala from the build job.